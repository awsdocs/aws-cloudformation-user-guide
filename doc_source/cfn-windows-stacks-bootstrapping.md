# Bootstrapping AWS CloudFormation Windows stacks<a name="cfn-windows-stacks-bootstrapping"></a>

This topic describes how to bootstrap a Windows stack and troubleshoot stack creation issues\. If you will be creating your own Windows image for use with CloudFormation, see the information at [Configuring a Windows instance using EC2ConfigService](http://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/UsingConfig_WinAMI.html) in the *Amazon EC2 Microsoft Windows Guide* for instructions\. You must set up a Windows instance with EC2ConfigService for it to work with the AWS CloudFormation bootstrapping tools\.

## Example of bootstrapping a Windows stack<a name="cfn-windows-bootstrapping-example"></a>

For the purposes of illustration, we'll examine a AWS CloudFormation single\-instance Sharepoint server template\.

The template can be viewed in its entirety at the following URL:
+  [ https://s3\.amazonaws\.com/cloudformation\-templates\-us\-east\-1/Windows\_Single\_Server\_SharePoint\_Foundation\.template ](https://s3.amazonaws.com/cloudformation-templates-us-east-1/Windows_Single_Server_SharePoint_Foundation.template) 

This example demonstrates how to:
+ Create an IAM User and Security Group for access to the instance
+ Configure initialization files: `cfn-credentials`, `cfn-hup.conf`, and `cfn-auto-reloader.conf`
+ Download and install a package such as Sharepoint Foundation 2010 on the server instance\.
+ Use a WaitCondition to ensure resources are ready 
+ Retrieve an IP for the instance with Amazon Elastic IP \(EIP\)\.

The AWS CloudFormation helper script `cfn-init` is used to perform each of these actions, based on information in the `AWS::CloudFormation::Init` resource in the Windows Single Server Sharepoint Foundation template\.

The AWS::CloudFormation::Init section is named "SharePointFoundation", and begins with a standard declaration:

```
"SharePointFoundation": {
   "Type" : "AWS::EC2::Instance",
   "Metadata" : {
     "AWS::CloudFormation::Init" : {
       "config" : {
```

After this, the **files** section of AWS::CloudFormation::Init is declared:

```
"files" : {
  "c:\\cfn\\cfn-hup.conf" : {
    "content" : { "Fn::Join" : ["", [
      "[main]\n",
      "stack=", { "Ref" : "AWS::StackName" }, "\n",
      "region=", { "Ref" : "AWS::Region" }, "\n"
      ]]}
  },
  "c:\\cfn\\hooks.d\\cfn-auto-reloader.conf" : {
    "content": { "Fn::Join" : ["", [
      "[cfn-auto-reloader-hook]\n",
      "triggers=post.update\n",
      "path=Resources.SharePointFoundation.Metadata.AWS::CloudFormation::Init\n",
      "action=cfn-init.exe -v -s ", { "Ref" : "AWS::StackName" },
                                     " -r SharePointFoundation",
                                     " --region ", { "Ref" : "AWS::Region" }, "\n"
    ]]}
  },
  "C:\\SharePoint\\SharePointFoundation2010.exe" : {
    "source" : "http://d3adzpja92utk0.cloudfront.net/SharePointFoundation.exe"
  }
},
```

Three files are created here and placed in the `C:\cfn` directory on the server instance\. They are:
+ `cfn-hup.conf`, the configuration file for cfn\-hup\.
+ `cfn-auto-reloader.conf`, the configuration file for the hook used by cfn\-hup to initiate an update \(calling cfn\-init\) when the metadata in AWS::CloudFormation::Init changes\.

There is also a file that is downloaded to the server: `SharePointFoundation.exe`\. This file is used to install SharePoint on the server instance\.

**Important**  
Since paths on Windows use a backslash \('\\'\) character, you must always remember to properly escape all backslashes by prepending another backslash whenever you refer to a Windows path in the AWS CloudFormation template\.

Next is the **commands** section, which are `cmd.exe` commands\.

```
"commands" : {
  "1-extract" : {
    "command" : "C:\\SharePoint\\SharePointFoundation2010.exe /extract:C:\\SharePoint\\SPF2010 /quiet /log:C:\\SharePoint\\SharePointFoundation2010-extract.log"
  },
  "2-prereq" : {
    "command" : "C:\\SharePoint\\SPF2010\\PrerequisiteInstaller.exe /unattended"
  },
  "3-install" : {
    "command" : "C:\\SharePoint\\SPF2010\\setup.exe /config C:\\SharePoint\\SPF2010\\Files\\SetupSilent\\config.xml"
  }
```

Because commands in the instance are processed in *alphabetical order by name*, each command has been prepended with a number indicating its desired execution order\. Thus, we can make sure that the installation package is first extracted, all prerequisites are then installed, and finally, installation of SharePoint is started\.

Next is the **Properties** section:

```
"Properties": {
  "InstanceType" : { "Ref" : "InstanceType" },
  "ImageId" : { "Fn::FindInMap" : [ "AWSRegionArch2AMI", { "Ref" : "AWS::Region" },
                { "Fn::FindInMap" : [ "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch" ] } ] },
  "SecurityGroups" : [ {"Ref" : "SharePointFoundationSecurityGroup"} ],
  "KeyName" : { "Ref" : "KeyPairName" },
  "UserData" : { "Fn::Base64" : { "Fn::Join" : ["", [
    "<script>\n",

    "cfn-init.exe -v -s ", { "Ref" : "AWS::StackName" },
    " -r SharePointFoundation",
    " --region ", { "Ref" : "AWS::Region" }, "\n",

    "cfn-signal.exe -e %ERRORLEVEL% ", { "Fn::Base64" : { "Ref" : "SharePointFoundationWaitHandle" }}, "\n",

    "</script>"
    ]]}}
  }
```

In this section, the `UserData` property contains a `cmd.exe` script that will be executed by `cfn-init`, surrounded by <script> tags\. You can use a Windows Powershell script here instead by surrounding your script with <powershell> tags\. For Windows stacks, you must base64 encode the wait condition handle URL again\.

SharePointFoundationWaitHandle is referenced here and run with `cfn-signal`\. The **WaitConditionHandle** and associated **WaitCondition** are declared next in the template:

```
"SharePointFoundationWaitHandle" : {
   "Type" : "AWS::CloudFormation::WaitConditionHandle"
},

"SharePointFoundationWaitCondition" : {
   "Type" : "AWS::CloudFormation::WaitCondition",
   "DependsOn" : "SharePointFoundation",
   "Properties" : {
     "Handle" : {"Ref" : "SharePointFoundationWaitHandle"},
     "Timeout" : "3600"
   }
}
```

Since executing all of the steps and installing SharePoint might take a while, but not an entire hour, the WaitCondition waits an hour \(3600 seconds\) before timing out\.

If all goes well, an Elastic IP is used to provide access to the SharePoint instance:

```
"Outputs" : {
 "SharePointFoundationURL" : {
   "Value" : { "Fn::Join" : ["", ["http://", { "Ref" : "SharePointFoundationEIP" } ]] },
   "Description" : "SharePoint Team Site URL. Please retrieve Administrator password of the instance and use it to access the URL"
 }
```

Once stack creation is complete, the IP address supplied by EIP will be displayed in the **Outputs** tab of the AWS CloudFormation console\. However, before you can access the instance you will need to retrieve the auto\-generated temporary Administrator password for the instance\. For more information, see [Connecting to your Windows instance using RDP](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/connecting_to_windows_instance.html) in the *Amazon EC2 User Guide for Windows Instances*\.

## How to manage Windows services<a name="w7739ab1c23c34c15c11"></a>

You manage Windows services in the same way as Linux services, except that you use a `windows` key instead of `sysvinit`\. The following example starts the `cfn-hup` service, sets it to Automatic, and restarts the service if cfn\-init modifies the `c:\cfn\cfn-hup.conf` or `c:\cfn\hooks.d\cfn-auto-reloader.conf` configuration files\. 

```
"services" : {
  "windows" : {
    "cfn-hup" : {
      "enabled" : "true",
      "ensureRunning" : "true",
      "files" : ["c:\\cfn\\cfn-hup.conf", "c:\\cfn\\hooks.d\\cfn-auto-reloader.conf"]
    }
  }
}
```

You can manage other Windows services in the same way by using the name—not the display name—to reference the service\.

## How to troubleshoot stack creation issues<a name="cfn-windows-stacks-troubleshooting"></a>

If your stack fails during creation, the default behavior is to Rollback on failure\. While this is normally a good default because it avoids unnecessary charges, it makes it difficult to debug why your stack creation is failing\.

To turn this behavior off, click **Show Advanced Options** when creating your stack with the AWS CloudFormation console, and click the **No** selector next to **Rollback on failure**\. This will allow you to log into your instance and view the logfiles to pinpoint issues encountered when running your startup scripts\.

Important logs to look at are:
+ The EC2 configuration log at `C:\Program Files\Amazon\Ec2ConfigService\Logs\Ec2ConfigLog.txt`
+ The cfn\-init log at ` C:\cfn\log\cfn-init.log`
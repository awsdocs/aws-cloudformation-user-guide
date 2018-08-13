# CloudFormation Helper Scripts Reference<a name="cfn-helper-scripts-reference"></a>

AWS CloudFormation provides the following Python helper scripts that you can use to install software and start services on an Amazon EC2 instance that you create as part of your stack:
+  [cfn\-init](cfn-init.md): Use to retrieve and interpret resource metadata, install packages, create files, and start services\.
+  [cfn\-signal](cfn-signal.md): Use to signal with a CreationPolicy or WaitCondition, so you can synchronize other resources in the stack when the prerequisite resource or application is ready\.
+  [cfn\-get\-metadata](cfn-get-metadata.md): Use to retrieve metadata for a resource or path to a specific key\.
+  [cfn\-hup](cfn-hup.md): Use to check for updates to metadata and execute custom hooks when changes are detected\.

You call the scripts directly from your template\. The scripts work in conjunction with resource metadata that's defined in the same template\. The scripts run on the Amazon EC2 instance during the stack creation process\.

**Note**  
The scripts are not executed by default\. You must include calls in your template to execute specific helper scripts\.

## Amazon Linux AMI Images<a name="cfn-helper-scripts-reference-amazon-amis"></a>

The AWS CloudFormation helper scripts are preinstalled on Amazon Linux AMI images\.
+ On the latest Amazon Linux AMI version, the scripts are installed in `/opt/aws/bin`\.
+ On previous Amazon Linux AMI versions, the aws\-cfn\-bootstrap package that contains the scripts is located in the Yum repository\.

## Downloading Packages for Other Platforms<a name="cfn-helper-scripts-reference-downloads"></a>

<a name="cfn-helper-scripts-reference-downloads"></a>For Linux/Unix distributions other than Amazon Linux AMI images and for Microsoft Windows \(2008 or later\), you can download the aws\-cfn\-bootstrap package\.


| File Format | Download URL | 
| --- | --- | 
|  RPM  |  [ https://s3\.amazonaws\.com/cloudformation\-examples/aws\-cfn\-bootstrap\-latest\.amzn1\.noarch\.rpm](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-latest.amzn1.noarch.rpm) Source files: [ https://s3\.amazonaws\.com/cloudformation\-examples/aws\-cfn\-bootstrap\-latest\.src\.rpm](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-latest.src.rpm)  | 
|  TAR\.GZ  |  [ https://s3\.amazonaws\.com/cloudformation\-examples/aws\-cfn\-bootstrap\-latest\.tar\.gz](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-latest.tar.gz) Uses the Python easy\-install tools\. To complete the installation for Ubuntu, you must create a symlink: `ln -s /root/aws-cfn-bootstrap-latest/init/ubuntu/cfn-hup /etc/init.d/cfn-hup`  | 
|  ZIP  |  [ https://s3\.amazonaws\.com/cloudformation\-examples/aws\-cfn\-bootstrap\-latest\.zip](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-latest.zip)  | 
|  MSI  |  32\-bit Windows: [ https://s3\.amazonaws\.com/cloudformation\-examples/aws\-cfn\-bootstrap\-latest\.msi](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-latest.msi)  64\-bit Windows: [ https://s3\.amazonaws\.com/cloudformation\-examples/aws\-cfn\-bootstrap\-win64\-latest\.msi](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-win64-latest.msi)  | 

## Permissions for helper scripts<a name="cfn-helper-scripts-reference-permissions"></a>

By default, helper scripts do not require credentials, so you do not need to use the `--access-key`, `--secret-key`, `--role`, or `--credential-file` options\. However, if no credentials are specified, AWS CloudFormation checks for stack membership and limits the scope of the call to the stack that the instance belongs to\.

If you choose to specify an option, we recommend that you specify only one of the following:
+ `--role`
+ `--credential-file`
+ `--access-key` together with `--secret-key`

If you do specify an option, keep in mind which permissions the various helper scripts require: 
+ `cfn-signal` requires [ `cloudformation:SignalResource`](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_SignalResource.html)
+ All other helper scripts require [ `cloudformation:DescribeStackResource`](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeStackResources.html)

For more information on using AWS CloudFormation\-specific actions and condition context keys in IAM policies, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.

## Using the Latest Version<a name="cfn-helper-scripts-reference-latest-version"></a>

The helper scripts are updated periodically\. If you use the helper scripts, ensure that your launched instances are using the latest version of the scripts:
+ Include the following command in the `UserData` property of your template before you call the scripts\. This command ensures that you get the latest version:

  `yum install -y aws-cfn-bootstrap`
+ If you don't include the `yum install` command and you use the `cfn-init`, `cfn-signal`, or `cfn-get-metadata` scripts, then you'll need to manually update the scripts in each Amazon EC2 Linux instance using this command:

  `sudo yum install -y aws-cfn-bootstrap`
+ If you don't include the `yum install` command and you use the `cfn-hup` script, then you'll need to manually update the script in each Amazon EC2 Linux instance using these commands:

  `sudo yum install -y aws-cfn-bootstrap`

  `sudo /sbin/service cfn-hup restart`
+ If you use the source code for the scripts to work with another version of Linux or a different platform, and you have created your own certificate trust store, you'll also need to keep the trust store updated\.

For the version history of the aws\-cfn\-bootstrap package, see [Release History for AWS CloudFormation Helper Scripts](releasehistory-aws-cfn-bootstrap.md)\.

**Topics**
+ [Amazon Linux AMI Images](#cfn-helper-scripts-reference-amazon-amis)
+ [Downloading Packages for Other Platforms](#cfn-helper-scripts-reference-downloads)
+ [Permissions for helper scripts](#cfn-helper-scripts-reference-permissions)
+ [Using the Latest Version](#cfn-helper-scripts-reference-latest-version)
+ [cfn\-init](cfn-init.md)
+ [cfn\-signal](cfn-signal.md)
+ [cfn\-get\-metadata](cfn-get-metadata.md)
+ [cfn\-hup](cfn-hup.md)
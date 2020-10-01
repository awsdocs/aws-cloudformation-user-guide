# Get started<a name="GettingStarted.Walkthrough"></a>

With the right template, you can deploy at once all the AWS resources you need for an application\. In this section, you'll examine a template that declares the resources for a WordPress blog, creates a WordPress blog as a stack, monitors the stack creation process, examines the resources on the stack, and then deletes the stack\. You use the AWS Management Console to complete these tasks\. 

## Step 1: Pick a template<a name="GettingStarted.Walkthrough.PickTemplate"></a>

First, you'll need a template that specifies the resources that you want in your stack\. For this step, you use a sample template that is already prepared\. The sample template creates a basic WordPress blog that uses a single Amazon EC2 instance with a local MySQL database for storage\. The template also creates an Amazon EC2 security group to control firewall settings for the Amazon EC2 instance\.

**Important**  
AWS CloudFormation is free, but the AWS resources that AWS CloudFormation creates are live \(and not running in a sandbox\)\. You will incur the standard usage fees for these resources until you terminate them in the last task in this tutorial\. The total charges will be minimal\. For information about how you might minimize any charges, go to [http://aws\.amazon\.com/free/](http://aws.amazon.com/free/)\.

**To view the template**
+ You can view the [JSON](https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/WordPress_Single_Instance.template) or [YAML](https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/WordPress_Single_Instance.yaml) WordPress sample template\. You don't need to download it because you will use the template URL later in this guide\. For more information about the template formats, see [AWS CloudFormation template formats](template-formats.md)\.

A template is a JSON or YAML text file that contains the configuration information about the AWS resources you want to create in the stack\. For this walkthrough, the sample template includes six top\-level sections: `AWSTemplateFormatVersion`, `Description`, `Parameters`, `Mappings`, `Resources`, and `Outputs`; however, only the `Resources` section is required\.

The Resources section contains the definitions of the AWS resources you want to create with the template\. Each resource is listed separately and specifies the properties that are necessary for creating that particular resource\. The following resource declaration is the configuration for the EC2 instance, which in this example has the logical name `WebServer`: 

**Example JSON**  

```
 1. "Resources" : {
 2.   ...    
 3.   "WebServer": {
 4.     "Type" : "AWS::EC2::Instance",
 5.     "Properties": {
 6.       "ImageId" : { "Fn::FindInMap" : [ "AWSRegionArch2AMI", { "Ref" : "AWS::Region" },
 7.                         { "Fn::FindInMap" : [ "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch" ] } ] },
 8.       "InstanceType"   : { "Ref" : "InstanceType" },
 9.       "SecurityGroups" : [ {"Ref" : "WebServerSecurityGroup"} ],
10.       "KeyName"        : { "Ref" : "KeyName" },
11.       "UserData" : { "Fn::Base64" : { "Fn::Join" : ["", [
12.                      "#!/bin/bash -xe\n",
13.                      "yum update -y aws-cfn-bootstrap\n",
14. 
15.                      "/opt/aws/bin/cfn-init -v ",
16.                      "         --stack ", { "Ref" : "AWS::StackName" },
17.                      "         --resource WebServer ",
18.                      "         --configsets wordpress_install ",
19.                      "         --region ", { "Ref" : "AWS::Region" }, "\n",
20. 
21.                      "/opt/aws/bin/cfn-signal -e $? ",
22.                      "         --stack ", { "Ref" : "AWS::StackName" },
23.                      "         --resource WebServer ",
24.                      "         --region ", { "Ref" : "AWS::Region" }, "\n"
25.       ]]}}
26.     },
27.     ...
28.   },
29.   ...  
30.   "WebServerSecurityGroup" : {
31.     "Type" : "AWS::EC2::SecurityGroup",
32.     "Properties" : {
33.       "GroupDescription" : "Enable HTTP access via port 80 locked down to the load balancer + SSH access",
34.       "SecurityGroupIngress" : [
35.         {"IpProtocol" : "tcp", "FromPort" : "80", "ToPort" : "80", "CidrIp" : "0.0.0.0/0"},
36.         {"IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : { "Ref" : "SSHLocation"}}
37.       ]
38.     }
39.   },
40.   ...    
41. },
```

**Example YAML**  

```
 1. Resources: 
 2.   ...    
 3.   WebServer:
 4.     Type: AWS::EC2::Instance
 5.     Properties:
 6.       ImageId: !FindInMap [AWSRegionArch2AMI, !Ref 'AWS::Region', !FindInMap [AWSInstanceType2Arch, !Ref InstanceType, Arch]]      
 7.       InstanceType:
 8.         Ref: InstanceType
 9.       KeyName:
10.         Ref: KeyName
11.       SecurityGroups:
12.       - Ref: WebServerSecurityGroup
13.       UserData:
14.         Fn::Base64: !Sub |
15.            #!/bin/bash -xe
16.            yum update -y aws-cfn-bootstrap
17.            /opt/aws/bin/cfn-init -v --stack ${AWS::StackId} --resource WebServer --configsets wordpress_install --region ${AWS::Region}
18.            /opt/aws/bin/cfn-signal -e $? --stack ${AWS::StackId} --resource WebServer --region ${AWS::Region}
19.     ...
20.   ...
21.   
22.   WebServerSecurityGroup:
23.     Type: AWS::EC2::SecurityGroup
24.     Properties:
25.       GroupDescription: "Enable HTTP access via port 80 locked down to the load balancer + SSH access"
26.       SecurityGroupIngress:
27.       - CidrIp: 0.0.0.0/0
28.         FromPort: '80'
29.         IpProtocol: tcp
30.         ToPort: '80'
31.       - CidrIp: !Ref SSHLocation
32.         FromPort: '22'
33.         IpProtocol: tcp
34.         ToPort: '22'
35. 
36.   ...
```

If you have created EC2 instances before, you can recognize properties, such as `ImageId`, `InstanceType`, and `KeyName`, that determine the configuration of the instance\. Resource declarations are an efficient way to specify all these configuration settings at once\. When you put resource declarations in a template, you can create and configure all the declared resources easily by using the template to create a stack\. To launch the same configuration of resources, all you have to do is create a new stack that uses the same template\.

The resource declaration begins with a string that specifies the logical name for the resource\. As you'll see, the logical name can be used to refer to resources within the template\.

You use the *Parameters* section to declare values that can be passed to the template when you create the stack\. A parameter is an effective way to specify sensitive information, such as user names and passwords, that you don't want to store in the template itself\. It is also a way to specify information that might be unique to the specific application or configuration you are deploying, for example, a domain name or instance type\. When you create the WordPress stack later in this section, you'll see the set of parameters declared in the template appear on the **Specify Details** page of the **Create Stack** wizard, where you can specify the parameters before you create the stack\.

The following parameters are used in the template to specify values that are used in properties of the EC2 instance:

**Example JSON**  

```
 1. "Parameters" : {
 2.   ...      
 3.   "KeyName": {
 4.     "Description" : "Name of an existing EC2 KeyPair to enable SSH access to the instances",
 5.     "Type": "AWS::EC2::KeyPair::KeyName",
 6.     "ConstraintDescription" : "must be the name of an existing EC2 KeyPair."
 7.   },
 8. 
 9.   "InstanceType" : {
10.     "Description" : "WebServer EC2 instance type",
11.     "Type" : "String",
12.     "Default" : "t2.small",
13.     "AllowedValues" : [ "t1.micro", "t2.nano", "t2.micro", "t2.small", "t2.medium", "t2.large", "m1.small", "m1.medium", "m1.large", "m1.xlarge", "m2.xlarge", "m2.2xlarge", "m2.4xlarge", "m3.medium", "m3.large", "m3.xlarge", "m3.2xlarge", "m4.large", "m4.xlarge", "m4.2xlarge", "m4.4xlarge", "m4.10xlarge", "c1.medium", "c1.xlarge", "c3.large", "c3.xlarge", "c3.2xlarge", "c3.4xlarge", "c3.8xlarge", "c4.large", "c4.xlarge", "c4.2xlarge", "c4.4xlarge", "c4.8xlarge", "g2.2xlarge", "g2.8xlarge", "r3.large", "r3.xlarge", "r3.2xlarge", "r3.4xlarge", "r3.8xlarge", "i2.xlarge", "i2.2xlarge", "i2.4xlarge", "i2.8xlarge", "d2.xlarge", "d2.2xlarge", "d2.4xlarge", "d2.8xlarge", "hi1.4xlarge", "hs1.8xlarge", "cr1.8xlarge", "cc2.8xlarge", "cg1.4xlarge"],
14.     "ConstraintDescription" : "must be a valid EC2 instance type."
15.   },
16. ...
```

**Example YAML**  

```
 1. Parameters:
 2.   ...      
 3.   KeyName:
 4.     ConstraintDescription: must be the name of an existing EC2 KeyPair.
 5.     Description: Name of an existing EC2 KeyPair to enable SSH access to the instances
 6.     Type: AWS::EC2::KeyPair::KeyName
 7.   InstanceType:
 8.     AllowedValues:
 9.     - t1.micro
10.     - t2.nano
11.     - t2.micro
12.     - t2.small
13.     - t2.medium
14.     - t2.large
15.     - m1.small
16.     - m1.medium
17.     - m1.large
18.     - m1.xlarge
19.     - m2.xlarge
20.     - m2.2xlarge
21.     - m2.4xlarge
22.     - m3.medium
23.     - m3.large
24.     - m3.xlarge
25.     - m3.2xlarge
26.     - m4.large
27.     - m4.xlarge
28.     - m4.2xlarge
29.     - m4.4xlarge
30.     - m4.10xlarge
31.     - c1.medium
32.     - c1.xlarge
33.     - c3.large
34.     - c3.xlarge
35.     - c3.2xlarge
36.     - c3.4xlarge
37.     - c3.8xlarge
38.     - c4.large
39.     - c4.xlarge
40.     - c4.2xlarge
41.     - c4.4xlarge
42.     - c4.8xlarge
43.     - g2.2xlarge
44.     - g2.8xlarge
45.     - r3.large
46.     - r3.xlarge
47.     - r3.2xlarge
48.     - r3.4xlarge
49.     - r3.8xlarge
50.     - i2.xlarge
51.     - i2.2xlarge
52.     - i2.4xlarge
53.     - i2.8xlarge
54.     - d2.xlarge
55.     - d2.2xlarge
56.     - d2.4xlarge
57.     - d2.8xlarge
58.     - hi1.4xlarge
59.     - hs1.8xlarge
60.     - cr1.8xlarge
61.     - cc2.8xlarge
62.     - cg1.4xlarge
63.     ConstraintDescription: must be a valid EC2 instance type.
64.     Default: t2.small
65.     Description: WebServer EC2 instance type
66.     Type: String
67. ...
```

In the `WebServer` resource declaration, you see the `KeyName` property specified with the `KeyName` parameter:

**Example JSON**  

```
1. "WebServer" : {
2.   "Type": "AWS::EC2::Instance",
3.   "Properties": {
4.     "KeyName" : { "Ref" : "KeyName" },
5.     ...
6.   }
7. },
```

**Example YAML**  

```
1. WebServer:
2.   Type: AWS::EC2::Instance
3.   Properties:
4.     KeyName:
5.       Ref: KeyName
6.     ...
```

The braces contain a call to the [Ref](intrinsic-function-reference-ref.md) function with `KeyName` as its input\. The Ref function returns the value of the object it refers to\. In this case, the Ref function sets the `KeyName` property to the value that was specified for `KeyName` when the stack was created\.

The Ref function can also set a resource's property to the value of another resource\. For example, the resource declaration `WebServer` contains the following property declaration:

**Example JSON**  

```
1. "WebServer" : {
2.   "Type": "AWS::EC2::Instance",
3.   "Properties": {
4.     ...
5.     "SecurityGroups" : [ {"Ref" : "WebServerSecurityGroup"} ],
6.     ...
7.   }
8. },
```

**Example YAML**  

```
1. WebServer:
2.   Type: AWS::EC2::Instance
3.   Properties:
4.     SecurityGroups:
5.     - Ref: WebServerSecurityGroup
6.     ...
```

The `SecurityGroups` property takes a list of EC2 security groups\. The Ref function has an input of `WebServerSecurityGroup`, which is the logical name of a security group in the template, and adds the name of `WebServerSecurityGroup` to the `SecurityGroups` property\.

In the template, you'll also find a *Mappings* section\. You use mappings to declare conditional values that are evaluated in a similar manner as a lookup table statement\. The template uses mappings to select the correct Amazon machine image \(AMI\) for the region and the architecture type for the instance type\. *Outputs* define custom values that are returned by the `aws cloudformation describe-stacks` command and in the AWS CloudFormation console **Outputs** tab after the stack is created\. You can use output values to return information from the resources in the stack, such as the URL for a website that was created in the template\. We cover mappings, outputs, and other things about templates in more detail in [Learn template basics](gettingstarted.templatebasics.md)\.

That's enough about templates for now\. Let's start creating a stack\.

## Step 2: Make sure you have prepared any required items for the stack<a name="GettingStarted.Walkthrough.prep"></a>

Before you create a stack from a template, you must ensure that all dependent resources that the template requires are available\. A template can use or refer to both existing AWS resources and resources declared in the template itself\. AWS CloudFormation takes care of checking references to resources in the template and also checks references to existing resources to ensure that they exist in the region where you are creating the stack\. If your template refers to a dependent resource that does not exist, stack creation fails\.

The example WordPress template contains an input parameter, `KeyName`, that specifies the key pair used for the Amazon EC2 instance that is declared in the template\. The template depends on the user who creates a stack from the template to supply a valid Amazon EC2 key pair for the `KeyName` parameter\. If you supply a valid key pair name, the stack creates successfully\. If you don't supply a valid key pair name, the stack is rolled back\.

Make sure you have a valid Amazon EC2 key pair and record the key pair name before you create the stack\.

To see your key pairs, open the Amazon EC2 console, then click **Key Pairs** in the navigation pane\. 

**Note**  
If you don't have an Amazon EC2 key pair, you must create the key pair in the same region where you are creating the stack\. For information about creating a key pair, see [Getting an SSH key pair](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair) in the *Amazon EC2 User Guide for Linux Instances*\.

Now that you have a valid key pair, let's use the WordPress template to create a stack\.

## Step 3: Create the stack<a name="GettingStarted.Walkthrough.createstack"></a>

You will create your stack based on the *WordPress\-1\.0\.0* file discussed earlier\. The template contains several AWS resources, such as an EC2 instance\.

**To create the WordPress stack**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. If this is a new AWS CloudFormation account, click **Create New Stack**\. Otherwise, click **Create Stack**\.

1. In the **Template** section, select **Specify an Amazon S3 Template URL** to type or paste the URL for the sample WordPress template, and then click **Next**:

   `https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/WordPress_Single_Instance.template`
**Note**  
AWS CloudFormation templates that are stored in an S3 bucket must be accessible to the user who is creating the stack, and must be located in the *same region* as the stack that is being created\. Therefore, if the S3 bucket is located in the `us-east-2` Region, the stack must also be created in `us-east-2`\.

1. In the **Specify Details** section, enter a stack name in the **Name** field\. For this example, use **MyWPTestStack**\. The stack name cannot contain spaces\.

1. On the **Specify Parameters** page, you'll recognize the parameters from the Parameters section of the template\. You must provide values for all parameters that do not have default values, including **DBUser**, **DBPassword**, **DBRootPassword**, and **KeyName**\. In the **KeyName** field, enter the name of a valid Amazon EC2 pair in the same region you are creating the stack\.

1. Click **Next**\.

1. In this scenario, we won't add any tags\. Click **Next**\. Tags, which are key\-value pairs, can help you identify your stacks\. For more information, see [ Adding tags to your AWS CloudFormation stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html)\. 

1. Review the information for the stack\. When you're satisfied with the settings, click **Create**\.

Your stack might take several minutes to create—but you probably don't want to just sit around waiting\. If you're like us, you'll want to know how the stack creation is going\.

## Step 4: Monitor the progress of stack creation<a name="GettingStarted.Walkthrough.monitor"></a>

After you complete the **Create Stack** wizard, AWS CloudFormation begins creating the resources that are specified in the template\. Your new stack, `MyWPTestStack`, appears in the list at the top portion of the **CloudFormation** console\. Its status should be CREATE\_IN\_PROGRESS\. You can see detailed status for a stack by viewing its events\.

**To view the events for the stack**

1. On the AWS CloudFormation console, select the stack `MyWPTestStack` in the list\.

1. In the stack details pane, click the **Events** tab\.

   The console automatically refreshes the event list with the most recent events every 60 seconds\.

The **Events** tab displays each major step in the creation of the stack sorted by the time of each event, with latest events on top\.

The first event \(at the bottom of the event list\) is the start of the stack creation process:

`2013-04-24 18:54 UTC-7 CREATE_IN_PROGRESS AWS::CloudFormation::Stack MyWPTestStack User initiated`

Next are events that mark the beginning and completion of the creation of each resource\. For example, creation of the EC2 instance results in the following entries:

`2013-04-24 18:59 UTC-7 CREATE_COMPLETE AWS::EC2::Instance...`

`2013-04-24 18:54 UTC-7 CREATE_IN_PROGRESS AWS::EC2::Instance...`

The `CREATE_IN_PROGRESS` event is logged when AWS CloudFormation reports that it has begun to create the resource\. The `CREATE_COMPLETE` event is logged when the resource is successfully created\.

When AWS CloudFormation has successfully created the stack, you will see the following event at the top of the **Events** tab:

`2013-04-24 19:17 UTC-7 CREATE_COMPLETE AWS::CloudFormation::Stack MyWPTestStack`

If AWS CloudFormation cannot create a resource, it reports a `CREATE_FAILED` event and, by default, rolls back the stack and deletes any resources that have been created\. The **Status Reason** column displays the issue that caused the failure\.

## Step 5: Use your stack resources<a name="GettingStarted.Walkthrough.viewapp"></a>

When the stack `MyWPTestStack` has a status of `CREATE_COMPLETE`, AWS CloudFormation has finished creating the stack, and you can start using its resources\.

The sample WordPress stack creates a WordPress website\. You can continue with the WordPress setup by running the WordPress installation script\.

**To complete the WordPress installation**

1. On the **Outputs** tab, in the **WebsiteURL** row, click the link in the **Value** column\.

   The `WebsiteURL` output value is the URL of the installation script for the WordPress website that you created with the stack\.

1. On the web page for the WordPress installation, follow the on\-screen instructions to complete the WordPress installation\. For more information about installing WordPress, see [https://wordpress\.org/support/article/how\-to\-install\-wordpress/](https://wordpress.org/support/article/how-to-install-wordpress/)\.

   After you complete the installation and log in, you are directed to the dashboard where you can set additional options for your WordPress blog\. Then, you can start writing posts for your blog that you successfully created by using a AWS CloudFormation template\.

## Step 6: Clean up<a name="GettingStarted.Walkthrough.cleanup"></a>

You have completed the AWS CloudFormation getting started tasks\. To make sure you are not charged for any unwanted services, you can clean up by deleting the stack and its resources\.

**To delete the stack and its resources**

1. From the AWS CloudFormation console, select the `MyWPTestStack` stack\.

1. Click **Delete Stack**\.

1. In the confirmation message that appears, click **Yes, Delete**\.

The status for `MyWPTestStack` changes to `DELETE_IN_PROGRESS`\. In the same way you monitored the creation of the stack, you can monitor its deletion by using the **Event** tab\. When AWS CloudFormation completes the deletion of the stack, it removes the stack from the list\.

Congratulations\! You successfully picked a template, created a stack, viewed and used its resources, and deleted the stack and its resources\. Not only that, you were able to set up a WordPress blog using a AWS CloudFormation template\. You can find other templates in the [AWS CloudFormation sample template library](http://aws.amazon.com/cloudformation/aws-cloudformation-templates/)\.

Now it's time to learn more about templates so that you can easily modify existing templates or create your own: [Learn template basics](gettingstarted.templatebasics.md)\.
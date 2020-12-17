# AWS::OpsWorks::Stack<a name="aws-resource-opsworks-stack"></a>

Creates a new stack\. For more information, see [Create a New Stack](https://docs.aws.amazon.com/opsworks/latest/userguide/workingstacks-edit.html)\.

 **Required Permissions**: To use this action, an IAM user must have an attached policy that explicitly grants permissions\. For more information about user permissions, see [Managing User Permissions](https://docs.aws.amazon.com/opsworks/latest/userguide/opsworks-security-users.html)\.

## Syntax<a name="aws-resource-opsworks-stack-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-stack-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorks::Stack",
  "Properties" : {
      "[AgentVersion](#cfn-opsworks-stack-agentversion)" : String,
      "[Attributes](#cfn-opsworks-stack-attributes)" : {Key : Value, ...},
      "[ChefConfiguration](#cfn-opsworks-stack-chefconfiguration)" : ChefConfiguration,
      "[CloneAppIds](#cfn-opsworks-stack-cloneappids)" : [ String, ... ],
      "[ClonePermissions](#cfn-opsworks-stack-clonepermissions)" : Boolean,
      "[ConfigurationManager](#cfn-opsworks-stack-configmanager)" : StackConfigurationManager,
      "[CustomCookbooksSource](#cfn-opsworks-stack-custcookbooksource)" : Source,
      "[CustomJson](#cfn-opsworks-stack-custjson)" : Json,
      "[DefaultAvailabilityZone](#cfn-opsworks-stack-defaultaz)" : String,
      "[DefaultInstanceProfileArn](#cfn-opsworks-stack-defaultinstanceprof)" : String,
      "[DefaultOs](#cfn-opsworks-stack-defaultos)" : String,
      "[DefaultRootDeviceType](#cfn-opsworks-stack-defaultrootdevicetype)" : String,
      "[DefaultSshKeyName](#cfn-opsworks-stack-defaultsshkeyname)" : String,
      "[DefaultSubnetId](#defaultsubnet)" : String,
      "[EcsClusterArn](#cfn-opsworks-stack-ecsclusterarn)" : String,
      "[ElasticIps](#cfn-opsworks-stack-elasticips)" : [ ElasticIp, ... ],
      "[HostnameTheme](#cfn-opsworks-stack-hostnametheme)" : String,
      "[Name](#cfn-opsworks-stack-name)" : String,
      "[RdsDbInstances](#cfn-opsworks-stack-rdsdbinstances)" : [ RdsDbInstance, ... ],
      "[ServiceRoleArn](#cfn-opsworks-stack-servicerolearn)" : String,
      "[SourceStackId](#cfn-opsworks-stack-sourcestackid)" : String,
      "[Tags](#cfn-opsworks-stack-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UseCustomCookbooks](#usecustcookbooks)" : Boolean,
      "[UseOpsworksSecurityGroups](#cfn-opsworks-stack-useopsworkssecuritygroups)" : Boolean,
      "[VpcId](#cfn-opsworks-stack-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-opsworks-stack-syntax.yaml"></a>

```
Type: AWS::OpsWorks::Stack
Properties: 
  [AgentVersion](#cfn-opsworks-stack-agentversion): String
  [Attributes](#cfn-opsworks-stack-attributes): 
    Key : Value
  [ChefConfiguration](#cfn-opsworks-stack-chefconfiguration): 
    ChefConfiguration
  [CloneAppIds](#cfn-opsworks-stack-cloneappids): 
    - String
  [ClonePermissions](#cfn-opsworks-stack-clonepermissions): Boolean
  [ConfigurationManager](#cfn-opsworks-stack-configmanager): 
    StackConfigurationManager
  [CustomCookbooksSource](#cfn-opsworks-stack-custcookbooksource): 
    Source
  [CustomJson](#cfn-opsworks-stack-custjson): 
    Json
  [DefaultAvailabilityZone](#cfn-opsworks-stack-defaultaz): String
  [DefaultInstanceProfileArn](#cfn-opsworks-stack-defaultinstanceprof): String
  [DefaultOs](#cfn-opsworks-stack-defaultos): String
  [DefaultRootDeviceType](#cfn-opsworks-stack-defaultrootdevicetype): String
  [DefaultSshKeyName](#cfn-opsworks-stack-defaultsshkeyname): String
  [DefaultSubnetId](#defaultsubnet): String
  [EcsClusterArn](#cfn-opsworks-stack-ecsclusterarn): String
  [ElasticIps](#cfn-opsworks-stack-elasticips): 
    - ElasticIp
  [HostnameTheme](#cfn-opsworks-stack-hostnametheme): String
  [Name](#cfn-opsworks-stack-name): String
  [RdsDbInstances](#cfn-opsworks-stack-rdsdbinstances): 
    - RdsDbInstance
  [ServiceRoleArn](#cfn-opsworks-stack-servicerolearn): String
  [SourceStackId](#cfn-opsworks-stack-sourcestackid): String
  [Tags](#cfn-opsworks-stack-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UseCustomCookbooks](#usecustcookbooks): Boolean
  [UseOpsworksSecurityGroups](#cfn-opsworks-stack-useopsworkssecuritygroups): Boolean
  [VpcId](#cfn-opsworks-stack-vpcid): String
```

## Properties<a name="aws-resource-opsworks-stack-properties"></a>

`AgentVersion`  <a name="cfn-opsworks-stack-agentversion"></a>
The default AWS OpsWorks Stacks agent version\. You have the following options:  
+ Auto\-update \- Set this parameter to `LATEST`\. AWS OpsWorks Stacks automatically installs new agent versions on the stack's instances as soon as they are available\.
+ Fixed version \- Set this parameter to your preferred agent version\. To update the agent version, you must edit the stack configuration and specify a new version\. AWS OpsWorks Stacks then automatically installs that version on the stack's instances\.
The default setting is the most recent release of the agent\. To specify an agent version, you must use the complete version number, not the abbreviated number shown on the console\. For a list of available agent version numbers, call [DescribeAgentVersions](https://docs.aws.amazon.com/goto/WebAPI/opsworks-2013-02-18/DescribeAgentVersions)\. AgentVersion cannot be set to Chef 12\.2\.  
You can also specify an agent version when you create or update an instance, which overrides the stack's default setting\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Attributes`  <a name="cfn-opsworks-stack-attributes"></a>
One or more user\-defined key\-value pairs to be added to the stack attributes\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChefConfiguration`  <a name="cfn-opsworks-stack-chefconfiguration"></a>
A `ChefConfiguration` object that specifies whether to enable Berkshelf and the Berkshelf version on Chef 11\.10 stacks\. For more information, see [Create a New Stack](https://docs.aws.amazon.com/opsworks/latest/userguide/workingstacks-creating.html)\.  
*Required*: No  
*Type*: [ChefConfiguration](aws-properties-opsworks-stack-chefconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloneAppIds`  <a name="cfn-opsworks-stack-cloneappids"></a>
If you're cloning an AWS OpsWorks stack, a list of AWS OpsWorks application stack IDs from the source stack to include in the cloned stack\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClonePermissions`  <a name="cfn-opsworks-stack-clonepermissions"></a>
If you're cloning an AWS OpsWorks stack, indicates whether to clone the source stack's permissions\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationManager`  <a name="cfn-opsworks-stack-configmanager"></a>
The configuration manager\. When you create a stack we recommend that you use the configuration manager to specify the Chef version: 12, 11\.10, or 11\.4 for Linux stacks, or 12\.2 for Windows stacks\. The default value for Linux stacks is currently 12\.  
*Required*: No  
*Type*: [StackConfigurationManager](aws-properties-opsworks-stack-stackconfigmanager.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomCookbooksSource`  <a name="cfn-opsworks-stack-custcookbooksource"></a>
Contains the information required to retrieve an app or cookbook from a repository\. For more information, see [Adding Apps](https://docs.aws.amazon.com/opsworks/latest/userguide/workingapps-creating.html) or [Cookbooks and Recipes](https://docs.aws.amazon.com/opsworks/latest/userguide/workingcookbook.html)\.  
*Required*: No  
*Type*: [Source](aws-properties-opsworks-stack-source.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomJson`  <a name="cfn-opsworks-stack-custjson"></a>
A string that contains user\-defined, custom JSON\. It can be used to override the corresponding default stack configuration attribute values or to pass data to recipes\. The string should be in the following format:  
 `"{\"key1\": \"value1\", \"key2\": \"value2\",...}"`   
For more information about custom JSON, see [Use Custom JSON to Modify the Stack Configuration Attributes](https://docs.aws.amazon.com/opsworks/latest/userguide/workingstacks-json.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultAvailabilityZone`  <a name="cfn-opsworks-stack-defaultaz"></a>
The stack's default Availability Zone, which must be in the specified region\. For more information, see [Regions and Endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html)\. If you also specify a value for `DefaultSubnetId`, the subnet must be in the same zone\. For more information, see the `VpcId` parameter description\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultInstanceProfileArn`  <a name="cfn-opsworks-stack-defaultinstanceprof"></a>
The Amazon Resource Name \(ARN\) of an IAM profile that is the default profile for all of the stack's EC2 instances\. For more information about IAM ARNs, see [Using Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultOs`  <a name="cfn-opsworks-stack-defaultos"></a>
The stack's default operating system, which is installed on every instance unless you specify a different operating system when you create the instance\. You can specify one of the following\.  
+ A supported Linux operating system: An Amazon Linux version, such as `Amazon Linux 2018.03`, `Amazon Linux 2017.09`, `Amazon Linux 2017.03`, `Amazon Linux 2016.09`, `Amazon Linux 2016.03`, `Amazon Linux 2015.09`, or `Amazon Linux 2015.03`\.
+ A supported Ubuntu operating system, such as `Ubuntu 16.04 LTS`, `Ubuntu 14.04 LTS`, or `Ubuntu 12.04 LTS`\.
+  `CentOS Linux 7` 
+  `Red Hat Enterprise Linux 7` 
+ A supported Windows operating system, such as `Microsoft Windows Server 2012 R2 Base`, `Microsoft Windows Server 2012 R2 with SQL Server Express`, `Microsoft Windows Server 2012 R2 with SQL Server Standard`, or `Microsoft Windows Server 2012 R2 with SQL Server Web`\.
+ A custom AMI: `Custom`\. You specify the custom AMI you want to use when you create instances\. For more information, see [ Using Custom AMIs](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-custom-ami.html)\.
The default option is the current Amazon Linux version\. For more information about supported operating systems, see [AWS OpsWorks Stacks Operating Systems](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-os.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultRootDeviceType`  <a name="cfn-opsworks-stack-defaultrootdevicetype"></a>
The default root device type\. This value is the default for all instances in the stack, but you can override it when you create an instance\. The default option is `instance-store`\. For more information, see [Storage for the Root Device](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ComponentsAMIs.html#storage-for-the-root-device)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ebs | instance-store`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultSshKeyName`  <a name="cfn-opsworks-stack-defaultsshkeyname"></a>
A default Amazon EC2 key pair name\. The default value is none\. If you specify a key pair name, AWS OpsWorks installs the public key on the instance and you can use the private key with an SSH client to log in to the instance\. For more information, see [ Using SSH to Communicate with an Instance](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-ssh.html) and [ Managing SSH Access](https://docs.aws.amazon.com/opsworks/latest/userguide/security-ssh-access.html)\. You can override this setting by specifying a different key pair, or no key pair, when you [ create an instance](https://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-add.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultSubnetId`  <a name="defaultsubnet"></a>
The stack's default subnet ID\. All instances are launched into this subnet unless you specify another subnet ID when you create the instance\. This parameter is required if you specify a value for the `VpcId` parameter\. If you also specify a value for `DefaultAvailabilityZone`, the subnet must be in that zone\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcsClusterArn`  <a name="cfn-opsworks-stack-ecsclusterarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Elastic Container Service \(Amazon ECS\) cluster to register with the AWS OpsWorks stack\.  
If you specify a cluster that's registered with another AWS OpsWorks stack, AWS CloudFormation deregisters the existing association before registering the cluster\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticIps`  <a name="cfn-opsworks-stack-elasticips"></a>
A list of Elastic IP addresses to register with the AWS OpsWorks stack\.  
If you specify an IP address that's registered with another AWS OpsWorks stack, AWS CloudFormation deregisters the existing association before registering the IP address\.
*Required*: No  
*Type*: List of [ElasticIp](aws-properties-opsworks-stack-elasticip.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostnameTheme`  <a name="cfn-opsworks-stack-hostnametheme"></a>
The stack's host name theme, with spaces replaced by underscores\. The theme is used to generate host names for the stack's instances\. By default, `HostnameTheme` is set to `Layer_Dependent`, which creates host names by appending integers to the layer's short name\. The other themes are:  
+  `Baked_Goods` 
+  `Clouds` 
+  `Europe_Cities` 
+  `Fruits` 
+  `Greek_Deities_and_Titans` 
+  `Legendary_creatures_from_Japan` 
+  `Planets_and_Moons` 
+  `Roman_Deities` 
+  `Scottish_Islands` 
+  `US_Cities` 
+  `Wild_Cats` 
To obtain a generated host name, call `GetHostNameSuggestion`, which returns a host name based on the current theme\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-opsworks-stack-name"></a>
The stack name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RdsDbInstances`  <a name="cfn-opsworks-stack-rdsdbinstances"></a>
The Amazon Relational Database Service \(Amazon RDS\) DB instance to register with the AWS OpsWorks stack\.  
If you specify a DB instance that's registered with another AWS OpsWorks stack, AWS CloudFormation deregisters the existing association before registering the DB instance\.
*Required*: No  
*Type*: List of [RdsDbInstance](aws-properties-opsworks-stack-rdsdbinstance.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRoleArn`  <a name="cfn-opsworks-stack-servicerolearn"></a>
The stack's AWS Identity and Access Management \(IAM\) role, which allows AWS OpsWorks Stacks to work with AWS resources on your behalf\. You must set this parameter to the Amazon Resource Name \(ARN\) for an existing IAM role\. For more information about IAM ARNs, see [Using Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceStackId`  <a name="cfn-opsworks-stack-sourcestackid"></a>
If you're cloning an AWS OpsWorks stack, the stack ID of the source AWS OpsWorks stack to clone\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-opsworks-stack-tags"></a>
A map that contains tag keys and tag values that are attached to a stack or layer\.  
+ The key cannot be empty\.
+ The key can be a maximum of 127 characters, and can contain only Unicode letters, numbers, or separators, or the following special characters: `+ - = . _ : /` 
+ The value can be a maximum 255 characters, and contain only Unicode letters, numbers, or separators, or the following special characters: `+ - = . _ : /` 
+ Leading and trailing white spaces are trimmed from both the key and value\.
+ A maximum of 40 tags is allowed for any resource\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseCustomCookbooks`  <a name="usecustcookbooks"></a>
Whether the stack uses custom cookbooks\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseOpsworksSecurityGroups`  <a name="cfn-opsworks-stack-useopsworkssecuritygroups"></a>
Whether to associate the AWS OpsWorks Stacks built\-in security groups with the stack's layers\.  
AWS OpsWorks Stacks provides a standard set of built\-in security groups, one for each layer, which are associated with layers by default\. With `UseOpsworksSecurityGroups` you can instead provide your own custom security groups\. `UseOpsworksSecurityGroups` has the following settings:   
+ True \- AWS OpsWorks Stacks automatically associates the appropriate built\-in security group with each layer \(default setting\)\. You can associate additional security groups with a layer after you create it, but you cannot delete the built\-in security group\.
+ False \- AWS OpsWorks Stacks does not associate built\-in security groups with layers\. You must create appropriate EC2 security groups and associate a security group with each layer that you create\. However, you can still manually associate a built\-in security group with a layer on creation; custom security groups are required only for those layers that need custom settings\.
For more information, see [Create a New Stack](https://docs.aws.amazon.com/opsworks/latest/userguide/workingstacks-creating.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-opsworks-stack-vpcid"></a>
The ID of the VPC that the stack is to be launched into\. The VPC must be in the stack's region\. All instances are launched into this VPC\. You cannot change the ID later\.  
+ If your account supports EC2\-Classic, the default value is `no VPC`\.
+ If your account does not support EC2\-Classic, the default value is the default VPC for the specified region\.
If the VPC ID corresponds to a default VPC and you have specified either the `DefaultAvailabilityZone` or the `DefaultSubnetId` parameter only, AWS OpsWorks Stacks infers the value of the other parameter\. If you specify neither parameter, AWS OpsWorks Stacks sets these parameters to the first valid Availability Zone for the specified region and the corresponding default VPC subnet ID, respectively\.  
If you specify a nondefault VPC ID, note the following:  
+ It must belong to a VPC in your account that is in the specified region\.
+ You must specify a value for `DefaultSubnetId`\.
For more information about how to use AWS OpsWorks Stacks with a VPC, see [Running a Stack in a VPC](https://docs.aws.amazon.com/opsworks/latest/userguide/workingstacks-vpc.html)\. For more information about default VPC and EC2\-Classic, see [Supported Platforms](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-supported-platforms.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-opsworks-stack-return-values"></a>

### Ref<a name="aws-resource-opsworks-stack-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myStack" }` 

For the AWS OpsWorks stack *myStack*, `Ref` returns the AWS OpsWorks stack ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-opsworks-stack--examples"></a>

### Template Snippet<a name="aws-resource-opsworks-stack--examples--Template_Snippet"></a>

The following snippet creates an AWS OpsWorks stack that uses the default service role and Amazon EC2 role, which are created after you use AWS OpsWorks for the first time:

#### JSON<a name="aws-resource-opsworks-stack--examples--Template_Snippet--json"></a>

```
"myStack" : {
  "Type" : "AWS::OpsWorks::Stack",
  "Properties" : {
    "Name" : {"Ref":"OpsWorksStackName"},
    "ServiceRoleArn" : { "Fn::Join": ["", ["arn:aws:iam::", {"Ref":"AWS::AccountId"}, ":role/aws-opsworks-service-role"]] },
    "DefaultInstanceProfileArn" : { "Fn::Join": ["", ["arn:aws:iam::", {"Ref":"AWS::AccountId"}, ":instance-profile/aws-opsworks-ec2-role"]] },
    "DefaultSshKeyName" : {"Ref":"KeyName"}
  }
}
```

#### YAML<a name="aws-resource-opsworks-stack--examples--Template_Snippet--yaml"></a>

```
myStack: 
  Type: "AWS::OpsWorks::Stack"
  Properties: 
    Name: 
      Ref: "OpsWorksStackName"
    ServiceRoleArn: 
      Fn::Join: 
        - ""
        - 
          - "arn:aws:iam::"
          - 
            Ref: "AWS::AccountId"
          - ":role/aws-opsworks-service-role"
    DefaultInstanceProfileArn: 
      Fn::Join: 
        - ""
        - 
          - "arn:aws:iam::"
          - 
            Ref: "AWS::AccountId"
          - ":instance-profile/aws-opsworks-ec2-role"
    DefaultSshKeyName: 
      Ref: "KeyName"
```

### Specify tags for layers and stacks<a name="aws-resource-opsworks-stack--examples--Specify_tags_for_layers_and_stacks"></a>

The following complete template example specifies tags for an AWS OpsWorks layer and stack that reference parameter values\.

#### JSON<a name="aws-resource-opsworks-stack--examples--Specify_tags_for_layers_and_stacks--json"></a>

```
{
    "Resources": {
        "ServiceRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    {
                                        "Ref": "OpsServicePrincipal"
                                    }
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "Path": "/",
                "Policies": [
                    {
                        "PolicyName": "opsworks-service",
                        "PolicyDocument": {
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": [
                                        "ec2:*",
                                        "iam:PassRole",
                                        "cloudwatch:GetMetricStatistics",
                                        "elasticloadbalancing:*"
                                    ],
                                    "Resource": "*"
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "OpsWorksEC2Role": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    {
                                        "Ref": "Ec2ServicePrincipal"
                                    }
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "Path": "/"
            }
        },
        "InstanceRole": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "Path": "/",
                "Roles": [
                    {
                        "Ref": "OpsWorksEC2Role"
                    }
                ]
            }
        },
        "myStack": {
            "Type": "AWS::OpsWorks::Stack",
            "Properties": {
                "Name": "TestStack",
                "ServiceRoleArn": {
                    "Fn::GetAtt": [
                        "ServiceRole",
                        "Arn"
                    ]
                },
                "DefaultInstanceProfileArn": {
                    "Fn::GetAtt": [
                        "InstanceRole",
                        "Arn"
                    ]
                },
                "Tags": [
                    {
                        "Key": {
                            "Ref": "StackKey"
                        },
                        "Value": {
                            "Ref": "StackValue"
                        }
                    }
                ]
            }
        },
        "myLayer": {
            "Type": "AWS::OpsWorks::Layer",
            "Properties": {
                "EnableAutoHealing": "true",
                "AutoAssignElasticIps": "false",
                "AutoAssignPublicIps": "true",
                "StackId": {
                    "Ref": "myStack"
                },
                "Type": "custom",
                "Shortname": "shortname",
                "Name": "name",
                "Tags": [
                    {
                        "Key": {
                            "Ref": "LayerKey"
                        },
                        "Value": {
                            "Ref": "LayerValue"
                        }
                    }
                ]
            }
        }
    },
    "Parameters": {
        "StackKey": {
            "Type": "String"
        },
        "LayerKey": {
            "Type": "String"
        },
        "StackValue": {
            "Type": "String"
        },
        "LayerValue": {
            "Type": "String"
        },
        "OpsServicePrincipal": {
            "Type": "String"
        },
        "Ec2ServicePrincipal": {
            "Type": "String"
        }
    }
}
```

#### YAML<a name="aws-resource-opsworks-stack--examples--Specify_tags_for_layers_and_stacks--yaml"></a>

```
Resources:
  ServiceRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - !Ref OpsServicePrincipal
            Action:
              - 'sts:AssumeRole'
      Path: /
      Policies:
        - PolicyName: opsworks-service
          PolicyDocument:
            Statement:
              - Effect: Allow
                Action:
                  - 'ec2:*'
                  - 'iam:PassRole'
                  - 'cloudwatch:GetMetricStatistics'
                  - 'elasticloadbalancing:*'
                Resource: '*'
  OpsWorksEC2Role:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - !Ref Ec2ServicePrincipal
            Action:
              - 'sts:AssumeRole'
      Path: /
  InstanceRole:
    Type: AWS::IAM::InstanceProfile
    Properties:
      Path: /
      Roles:
        - !Ref OpsWorksEC2Role
  myStack:
    Type: AWS::OpsWorks::Stack
    Properties:
      Name: TestStack
      ServiceRoleArn: !GetAtt 
        - ServiceRole
        - Arn
      DefaultInstanceProfileArn: !GetAtt 
        - InstanceRole
        - Arn
      Tags:
        - Key: !Ref StackKey
          Value: !Ref StackValue
  myLayer:
    Type: AWS::OpsWorks::Layer
    Properties:
      EnableAutoHealing: 'true'
      AutoAssignElasticIps: 'false'
      AutoAssignPublicIps: 'true'
      StackId: !Ref myStack
      Type: custom
      Shortname: shortname
      Name: name
      Tags:
        - Key: !Ref LayerKey
          Value: !Ref LayerValue
Parameters:
  StackKey:
    Type: String
  LayerKey:
    Type: String
  StackValue:
    Type: String
  LayerValue:
    Type: String
  OpsServicePrincipal:
    Type: String
  Ec2ServicePrincipal:
    Type: String
```

## See also<a name="aws-resource-opsworks-stack--seealso"></a>
+  [CreateStack](https://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html) in the *AWS OpsWorks API Reference*\.
+  [Create a New Stack](https://docs.aws.amazon.com/opsworks/latest/userguide/workingstacks-creating.html) in the *AWS OpsWorks User Guide*\.


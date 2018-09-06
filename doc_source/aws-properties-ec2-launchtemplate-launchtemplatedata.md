# Amazon EC2 LaunchTemplate LaunchTemplateData<a name="aws-properties-ec2-launchtemplate-launchtemplatedata"></a>

<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-description"></a>The `LaunchTemplateData` property type specifies the information to include the launch template for an Amazon EC2 instance\.

<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-inheritance"></a> `LaunchTemplateData` is a property of the [AWS::EC2::LaunchTemplate](aws-resource-ec2-launchtemplate.md) resource\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax.json"></a>

```
{
  "[SecurityGroups](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroups)" : [ String, ... ],
  "[TagSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications)" : [ [*TagSpecification*](aws-properties-ec2-launchtemplate-tagspecification.md), ... ],
  "[UserData](#cfn-ec2-launchtemplate-launchtemplatedata-userdata)" : String,
  "[InstanceInitiatedShutdownBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior)" : String,
  "[BlockDeviceMappings](#cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings)" : [ [*BlockDeviceMapping*](aws-properties-ec2-launchtemplate-blockdevicemapping.md), ... ],
  "[IamInstanceProfile](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile)" : [*IamInstanceProfile*](aws-properties-ec2-launchtemplate-iaminstanceprofile.md),
  "[KernelId](#cfn-ec2-launchtemplate-launchtemplatedata-kernelid)" : String,
  "[SecurityGroupIds](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids)" : [ String, ... ],
  "[EbsOptimized](#cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized)" : Boolean,
  "[KeyName](#cfn-ec2-launchtemplate-launchtemplatedata-keyname)" : String,
  "[DisableApiTermination](#cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination)" : Boolean,
  "[ElasticGpuSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications)" : [ [*ElasticGpuSpecification*](aws-properties-ec2-launchtemplate-elasticgpuspecification.md), ... ],
  "[Placement](#cfn-ec2-launchtemplate-launchtemplatedata-placement)" : [*Placement*](aws-properties-ec2-launchtemplate-placement.md),
  "[InstanceMarketOptions](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions)" : [*InstanceMarketOptions*](aws-properties-ec2-launchtemplate-instancemarketoptions.md),
  "[NetworkInterfaces](#cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces)" : [ [*NetworkInterface*](aws-properties-ec2-launchtemplate-networkinterface.md), ... ],
  "[ImageId](#cfn-ec2-launchtemplate-launchtemplatedata-imageid)" : String,
  "[InstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancetype)" : String,
  "[RamDiskId](#cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid)" : String,
  "[Monitoring](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring)" : [*Monitoring*](aws-properties-ec2-launchtemplate-monitoring.md),
  "[CreditSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification)" : [*CreditSpecification*](aws-properties-ec2-launchtemplate-creditspecification.md)
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax.yaml"></a>

```
[SecurityGroups](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroups): 
  - String
[TagSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications): 
  - [*TagSpecification*](aws-properties-ec2-launchtemplate-tagspecification.md)
[UserData](#cfn-ec2-launchtemplate-launchtemplatedata-userdata): String
[InstanceInitiatedShutdownBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior): String
[BlockDeviceMappings](#cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings): 
  - [*BlockDeviceMapping*](aws-properties-ec2-launchtemplate-blockdevicemapping.md)
[IamInstanceProfile](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile): [*IamInstanceProfile*](aws-properties-ec2-launchtemplate-iaminstanceprofile.md)
[KernelId](#cfn-ec2-launchtemplate-launchtemplatedata-kernelid): String
[SecurityGroupIds](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids): 
  - String
[EbsOptimized](#cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized): Boolean
[KeyName](#cfn-ec2-launchtemplate-launchtemplatedata-keyname): String
[DisableApiTermination](#cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination): Boolean
[ElasticGpuSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications): 
  - [*ElasticGpuSpecification*](aws-properties-ec2-launchtemplate-elasticgpuspecification.md)
[Placement](#cfn-ec2-launchtemplate-launchtemplatedata-placement): [*Placement*](aws-properties-ec2-launchtemplate-placement.md)
[InstanceMarketOptions](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions): [*InstanceMarketOptions*](aws-properties-ec2-launchtemplate-instancemarketoptions.md)
[NetworkInterfaces](#cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces): 
  - [*NetworkInterface*](aws-properties-ec2-launchtemplate-networkinterface.md)
[ImageId](#cfn-ec2-launchtemplate-launchtemplatedata-imageid): String
[InstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancetype): String
[RamDiskId](#cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid): String
[Monitoring](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring): [*Monitoring*](aws-properties-ec2-launchtemplate-monitoring.md)
[CreditSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification): [*CreditSpecification*](aws-properties-ec2-launchtemplate-creditspecification.md)
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-properties"></a>

`BlockDeviceMappings`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings"></a>
The block device mapping\.  
 *Required*: No  
 *Type*: List of [Amazon EC2 LaunchTemplate BlockDeviceMapping](aws-properties-ec2-launchtemplate-blockdevicemapping.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CreditSpecification`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-creditspecification"></a>
The credit option for CPU usage of the instance\. Valid for T2 instances only\.  
 *Required*: No  
 *Type*: [Amazon EC2 LaunchTemplate CreditSpecification](aws-properties-ec2-launchtemplate-creditspecification.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DisableApiTermination`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination"></a>
If set to `true`, you can't terminate the instance using the Amazon EC2 console, CLI, or API\.   
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`EbsOptimized`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized"></a>
Indicates whether the instance is optimized for Amazon EBS I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal Amazon EBS I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when using an EBS\-optimized instance\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ElasticGpuSpecifications`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications"></a>
An elastic GPU to associate with the instance\.  
 *Required*: No  
 *Type*: List of [Amazon EC2 LaunchTemplate ElasticGpuSpecification](aws-properties-ec2-launchtemplate-elasticgpuspecification.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`IamInstanceProfile`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile"></a>
The IAM instance profile\.  
 *Required*: No  
 *Type*: [Amazon EC2 LaunchTemplate IamInstanceProfile](aws-properties-ec2-launchtemplate-iaminstanceprofile.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ImageId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-imageid"></a>
The ID of the AMI\. For more information, see [DescribeImages](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeImages.html) in the *Amazon EC2 API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstanceInitiatedShutdownBehavior`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior"></a>
Indicates whether an instance stops or terminates when you initiate shutdown from the instance \(using the operating system command for system shutdown\)\.  
Valid values include `stop` and `terminate`\. The default is `stop`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstanceMarketOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions"></a>
The market \(purchasing\) option for the instances\.  
 *Required*: No  
 *Type*: [Amazon EC2 LaunchTemplate InstanceMarketOptions](aws-properties-ec2-launchtemplate-instancemarketoptions.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstanceType`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancetype"></a>
The instance type\. For a list of valid values, see [RequestLaunchTemplateData](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RequestLaunchTemplateData.html) in the *Amazon EC2 API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KernelId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-kernelid"></a>
The ID of the kernel\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User Provided Kernels](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KeyName`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-keyname"></a>
The name of the key pair\. For information on creating a key pair, see [CreateKeyPair](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateKeyPair.html) or [ImportKeyPair](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportKeyPair.html) in the *Amazon EC2 API Reference*\.  
If you do not specify a key pair, you can't connect to the instance unless you choose an AMI that is configured to allow users another way to log in\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Monitoring`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-monitoring"></a>
The monitoring for the instance\.  
 *Required*: No  
 *Type*: [Amazon EC2 LaunchTemplate Monitoring](aws-properties-ec2-launchtemplate-monitoring.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NetworkInterfaces`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces"></a>
One or more network interfaces\.  
 *Required*: No  
 *Type*: List of [Amazon EC2 LaunchTemplate NetworkInterface](aws-properties-ec2-launchtemplate-networkinterface.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Placement`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement"></a>
The placement for the instance\.  
 *Required*: No  
 *Type*: [Amazon EC2 LaunchTemplate Placement](aws-properties-ec2-launchtemplate-placement.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RamDiskId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid"></a>
The ID of the RAM disk\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User Provided Kernels](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecurityGroups`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-securitygroups"></a>
\[EC2\-Classic, default VPC\] One or more security group names\. For a nondefault VPC, you must use security group IDs instead\. You cannot specify both a security group ID and security name in the same request\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecurityGroupIds`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids"></a>
One or more security group IDs\. You cannot specify both a security group ID and security name in the same request\. For information on creating a security group, see [CreateSecurityGroup](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSecurityGroup.html) in the *Amazon EC2 API Reference*\.   
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TagSpecifications`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications"></a>
The tags to apply to the resources during launch\. You can tag instances and volumes\. The specified tags are applied to all instances or volumes that are created during launch\.  
 *Required*: No  
 *Type*: List of [Amazon EC2 LaunchTemplate TagSpecification](aws-properties-ec2-launchtemplate-tagspecification.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`UserData`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-userdata"></a>
The Base64\-encoded user data to make available to the instance\. For more information, see [Running Commands on Your Linux Instance at Launch](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html) in the *Amazon EC2 User Guide for Linux Instances* and [Adding User Data](http://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/ec2-instance-metadata.html#instancedata-add-user-data) in the *Amazon EC2 User Guide for Windows Instances*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-seealso"></a>
+ [RequestLaunchTemplateData](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RequestLaunchTemplateData.html) in the *Amazon EC2 API Reference*
# AWS::EC2::LaunchTemplate LaunchTemplateData<a name="aws-properties-ec2-launchtemplate-launchtemplatedata"></a>

The information to include in the launch template\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax.json"></a>

```
{
  "[BlockDeviceMappings](#cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings)" : [ [BlockDeviceMapping](aws-properties-ec2-launchtemplate-blockdevicemapping.md), ... ],
  "[CapacityReservationSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification)" : [CapacityReservationSpecification](aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification.md),
  "[CpuOptions](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions)" : [CpuOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions.md),
  "[CreditSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification)" : [CreditSpecification](aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification.md),
  "[DisableApiTermination](#cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination)" : Boolean,
  "[EbsOptimized](#cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized)" : Boolean,
  "[ElasticGpuSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications)" : [ [ElasticGpuSpecification](aws-properties-ec2-launchtemplate-elasticgpuspecification.md), ... ],
  "[ElasticInferenceAccelerators](#cfn-ec2-launchtemplate-launchtemplatedata-elasticinferenceaccelerators)" : [ [LaunchTemplateElasticInferenceAccelerator](aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator.md), ... ],
  "[HibernationOptions](#cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions)" : [HibernationOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions.md),
  "[IamInstanceProfile](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile)" : [IamInstanceProfile](aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile.md),
  "[ImageId](#cfn-ec2-launchtemplate-launchtemplatedata-imageid)" : String,
  "[InstanceInitiatedShutdownBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior)" : String,
  "[InstanceMarketOptions](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions)" : [InstanceMarketOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions.md),
  "[InstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancetype)" : String,
  "[KernelId](#cfn-ec2-launchtemplate-launchtemplatedata-kernelid)" : String,
  "[KeyName](#cfn-ec2-launchtemplate-launchtemplatedata-keyname)" : String,
  "[LicenseSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-licensespecifications)" : [ [LicenseSpecification](aws-properties-ec2-launchtemplate-licensespecification.md), ... ],
  "[Monitoring](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring)" : [Monitoring](aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring.md),
  "[NetworkInterfaces](#cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces)" : [ [NetworkInterface](aws-properties-ec2-launchtemplate-networkinterface.md), ... ],
  "[Placement](#cfn-ec2-launchtemplate-launchtemplatedata-placement)" : [Placement](aws-properties-ec2-launchtemplate-launchtemplatedata-placement.md),
  "[RamDiskId](#cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid)" : String,
  "[SecurityGroupIds](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids)" : [ String, ... ],
  "[SecurityGroups](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroups)" : [ String, ... ],
  "[TagSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications)" : [ [TagSpecification](aws-properties-ec2-launchtemplate-tagspecification.md), ... ],
  "[UserData](#cfn-ec2-launchtemplate-launchtemplatedata-userdata)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax.yaml"></a>

```
  [BlockDeviceMappings](#cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings): 
    - [BlockDeviceMapping](aws-properties-ec2-launchtemplate-blockdevicemapping.md)
  [CapacityReservationSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification): 
    [CapacityReservationSpecification](aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification.md)
  [CpuOptions](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions): 
    [CpuOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions.md)
  [CreditSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification): 
    [CreditSpecification](aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification.md)
  [DisableApiTermination](#cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination): Boolean
  [EbsOptimized](#cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized): Boolean
  [ElasticGpuSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications): 
    - [ElasticGpuSpecification](aws-properties-ec2-launchtemplate-elasticgpuspecification.md)
  [ElasticInferenceAccelerators](#cfn-ec2-launchtemplate-launchtemplatedata-elasticinferenceaccelerators): 
    - [LaunchTemplateElasticInferenceAccelerator](aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator.md)
  [HibernationOptions](#cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions): 
    [HibernationOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions.md)
  [IamInstanceProfile](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile): 
    [IamInstanceProfile](aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile.md)
  [ImageId](#cfn-ec2-launchtemplate-launchtemplatedata-imageid): String
  [InstanceInitiatedShutdownBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior): String
  [InstanceMarketOptions](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions): 
    [InstanceMarketOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions.md)
  [InstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancetype): String
  [KernelId](#cfn-ec2-launchtemplate-launchtemplatedata-kernelid): String
  [KeyName](#cfn-ec2-launchtemplate-launchtemplatedata-keyname): String
  [LicenseSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-licensespecifications): 
    - [LicenseSpecification](aws-properties-ec2-launchtemplate-licensespecification.md)
  [Monitoring](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring): 
    [Monitoring](aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring.md)
  [NetworkInterfaces](#cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces): 
    - [NetworkInterface](aws-properties-ec2-launchtemplate-networkinterface.md)
  [Placement](#cfn-ec2-launchtemplate-launchtemplatedata-placement): 
    [Placement](aws-properties-ec2-launchtemplate-launchtemplatedata-placement.md)
  [RamDiskId](#cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid): String
  [SecurityGroupIds](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids): 
    - String
  [SecurityGroups](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroups): 
    - String
  [TagSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications): 
    - [TagSpecification](aws-properties-ec2-launchtemplate-tagspecification.md)
  [UserData](#cfn-ec2-launchtemplate-launchtemplatedata-userdata): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-properties"></a>

`BlockDeviceMappings`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings"></a>
The block device mapping\.  
*Required*: No  
*Type*: List of [BlockDeviceMapping](aws-properties-ec2-launchtemplate-blockdevicemapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityReservationSpecification`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification"></a>
The Capacity Reservation targeting option\. If you do not specify this parameter, the instance's Capacity Reservation preference defaults to `open`, which enables it to run in any open Capacity Reservation that has matching attributes \(instance type, platform, Availability Zone\)\.  
*Required*: No  
*Type*: [CapacityReservationSpecification](aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CpuOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions"></a>
The CPU options for the instance\. For more information, see [Optimizing CPU Options](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-optimize-cpu.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: [CpuOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreditSpecification`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-creditspecification"></a>
The credit option for CPU usage of the instance\. Valid for T2 or T3 instances only\.  
*Required*: No  
*Type*: [CreditSpecification](aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableApiTermination`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination"></a>
If you set this parameter to `true`, you can't terminate the instance using the Amazon EC2 console, CLI, or API; otherwise, you can\. To change this attribute after launch, use [ModifyInstanceAttribute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyInstanceAttribute.html)\. Alternatively, if you set `InstanceInitiatedShutdownBehavior` to `terminate`, you can terminate the instance by running the shutdown command from the instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbsOptimized`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized"></a>
Indicates whether the instance is optimized for Amazon EBS I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal Amazon EBS I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when using an EBS\-optimized instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticGpuSpecifications`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications"></a>
An elastic GPU to associate with the instance\.  
*Required*: No  
*Type*: List of [ElasticGpuSpecification](aws-properties-ec2-launchtemplate-elasticgpuspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticInferenceAccelerators`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-elasticinferenceaccelerators"></a>
 The elastic inference accelerator for the instance\.   
*Required*: No  
*Type*: List of [LaunchTemplateElasticInferenceAccelerator](aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HibernationOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions"></a>
Indicates whether an instance is enabled for hibernation\. This parameter is valid only if the instance meets the [hibernation prerequisites](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html#hibernating-prerequisites)\. Hibernation is currently supported only for Amazon Linux\. For more information, see [Hibernate Your Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: [HibernationOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamInstanceProfile`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile"></a>
The IAM instance profile\.  
*Required*: No  
*Type*: [IamInstanceProfile](aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-imageid"></a>
The ID of the AMI\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceInitiatedShutdownBehavior`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior"></a>
Indicates whether an instance stops or terminates when you initiate shutdown from the instance \(using the operating system command for system shutdown\)\.  
Default: `stop`   
*Required*: No  
*Type*: String  
*Allowed Values*: `stop | terminate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceMarketOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions"></a>
The market \(purchasing\) option for the instances\.  
*Required*: No  
*Type*: [InstanceMarketOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancetype"></a>
The instance type\. For more information, see [Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `a1.2xlarge | a1.4xlarge | a1.large | a1.medium | a1.xlarge | c1.medium | c1.xlarge | c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.18xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.xlarge | c5d.18xlarge | c5d.2xlarge | c5d.4xlarge | c5d.9xlarge | c5d.large | c5d.xlarge | c5n.18xlarge | c5n.2xlarge | c5n.4xlarge | c5n.9xlarge | c5n.large | c5n.xlarge | cc1.4xlarge | cc2.8xlarge | cg1.4xlarge | cr1.8xlarge | d2.2xlarge | d2.4xlarge | d2.8xlarge | d2.xlarge | f1.16xlarge | f1.2xlarge | f1.4xlarge | g2.2xlarge | g2.8xlarge | g3.16xlarge | g3.4xlarge | g3.8xlarge | g3s.xlarge | h1.16xlarge | h1.2xlarge | h1.4xlarge | h1.8xlarge | hi1.4xlarge | hs1.8xlarge | i2.2xlarge | i2.4xlarge | i2.8xlarge | i2.xlarge | i3.16xlarge | i3.2xlarge | i3.4xlarge | i3.8xlarge | i3.large | i3.metal | i3.xlarge | m1.large | m1.medium | m1.small | m1.xlarge | m2.2xlarge | m2.4xlarge | m2.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.16xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.large | m5.metal | m5.xlarge | m5a.12xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.large | m5a.xlarge | m5ad.12xlarge | m5ad.16xlarge | m5ad.24xlarge | m5ad.2xlarge | m5ad.4xlarge | m5ad.8xlarge | m5ad.large | m5ad.xlarge | m5d.12xlarge | m5d.24xlarge | m5d.2xlarge | m5d.4xlarge | m5d.large | m5d.metal | m5d.xlarge | p2.16xlarge | p2.8xlarge | p2.xlarge | p3.16xlarge | p3.2xlarge | p3.8xlarge | p3dn.24xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.large | r5.metal | r5.xlarge | r5a.12xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.large | r5a.xlarge | r5ad.12xlarge | r5ad.16xlarge | r5ad.24xlarge | r5ad.2xlarge | r5ad.4xlarge | r5ad.8xlarge | r5ad.large | r5ad.xlarge | r5d.12xlarge | r5d.24xlarge | r5d.2xlarge | r5d.4xlarge | r5d.large | r5d.metal | r5d.xlarge | t1.micro | t2.2xlarge | t2.large | t2.medium | t2.micro | t2.nano | t2.small | t2.xlarge | t3.2xlarge | t3.large | t3.medium | t3.micro | t3.nano | t3.small | t3.xlarge | t3a.2xlarge | t3a.large | t3a.medium | t3a.micro | t3a.nano | t3a.small | t3a.xlarge | u-12tb1.metal | u-6tb1.metal | u-9tb1.metal | x1.16xlarge | x1.32xlarge | x1e.16xlarge | x1e.2xlarge | x1e.32xlarge | x1e.4xlarge | x1e.8xlarge | x1e.xlarge | z1d.12xlarge | z1d.2xlarge | z1d.3xlarge | z1d.6xlarge | z1d.large | z1d.metal | z1d.xlarge`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KernelId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-kernelid"></a>
The ID of the kernel\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User Provided Kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyName`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-keyname"></a>
The name of the key pair\. You can create a key pair using [CreateKeyPair](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateKeyPair.html) or [ImportKeyPair](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportKeyPair.html)\.  
If you do not specify a key pair, you can't connect to the instance unless you choose an AMI that is configured to allow users another way to log in\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseSpecifications`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-licensespecifications"></a>
The license configurations\.  
*Required*: No  
*Type*: List of [LicenseSpecification](aws-properties-ec2-launchtemplate-licensespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Monitoring`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-monitoring"></a>
The monitoring for the instance\.  
*Required*: No  
*Type*: [Monitoring](aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaces`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces"></a>
One or more network interfaces\. If you specify a network interface, you must specify any security groups as part of the network interface\.  
*Required*: No  
*Type*: List of [NetworkInterface](aws-properties-ec2-launchtemplate-networkinterface.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Placement`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement"></a>
The placement for the instance\.  
*Required*: No  
*Type*: [Placement](aws-properties-ec2-launchtemplate-launchtemplatedata-placement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RamDiskId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid"></a>
The ID of the RAM disk\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User Provided Kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon Elastic Compute Cloud User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids"></a>
One or more security group IDs\. You can create a security group using [CreateSecurityGroup](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSecurityGroup.html)\. You cannot specify both a security group ID and security name in the same request\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroups`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-securitygroups"></a>
\[EC2\-Classic, default VPC\] One or more security group names\. For a nondefault VPC, you must use security group IDs instead\. You cannot specify both a security group ID and security name in the same request\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagSpecifications`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications"></a>
The tags to apply to the resources during launch\. You can only tag instances and volumes on launch\. The specified tags are applied to all instances or volumes that are created during launch\. To tag a resource after it has been created, see [CreateTags](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTags.html)\.  
*Required*: No  
*Type*: List of [TagSpecification](aws-properties-ec2-launchtemplate-tagspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserData`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-userdata"></a>
The Base64\-encoded user data to make available to the instance\. For more information, see [Running Commands on Your Linux Instance at Launch](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html) \(Linux\) and [Adding User Data](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/ec2-instance-metadata.html#instancedata-add-user-data) \(Windows\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata--seealso"></a>
+  [RequestLaunchTemplateData](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RequestLaunchTemplateData.html) in the *Amazon Elastic Compute Cloud API Reference* 
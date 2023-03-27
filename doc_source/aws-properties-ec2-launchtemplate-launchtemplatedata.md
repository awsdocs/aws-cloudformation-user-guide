# AWS::EC2::LaunchTemplate LaunchTemplateData<a name="aws-properties-ec2-launchtemplate-launchtemplatedata"></a>

The information to include in the launch template\.

**Note**  
You must specify at least one parameter for the launch template data\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax.json"></a>

```
{
  "[BlockDeviceMappings](#cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
  "[CapacityReservationSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification)" : CapacityReservationSpecification,
  "[CpuOptions](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions)" : CpuOptions,
  "[CreditSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification)" : CreditSpecification,
  "[DisableApiStop](#cfn-ec2-launchtemplate-launchtemplatedata-disableapistop)" : Boolean,
  "[DisableApiTermination](#cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination)" : Boolean,
  "[EbsOptimized](#cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized)" : Boolean,
  "[ElasticGpuSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications)" : [ ElasticGpuSpecification, ... ],
  "[ElasticInferenceAccelerators](#cfn-ec2-launchtemplate-launchtemplatedata-elasticinferenceaccelerators)" : [ LaunchTemplateElasticInferenceAccelerator, ... ],
  "[EnclaveOptions](#cfn-ec2-launchtemplate-launchtemplatedata-enclaveoptions)" : EnclaveOptions,
  "[HibernationOptions](#cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions)" : HibernationOptions,
  "[IamInstanceProfile](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile)" : IamInstanceProfile,
  "[ImageId](#cfn-ec2-launchtemplate-launchtemplatedata-imageid)" : String,
  "[InstanceInitiatedShutdownBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior)" : String,
  "[InstanceMarketOptions](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions)" : InstanceMarketOptions,
  "[InstanceRequirements](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements)" : InstanceRequirements,
  "[InstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancetype)" : String,
  "[KernelId](#cfn-ec2-launchtemplate-launchtemplatedata-kernelid)" : String,
  "[KeyName](#cfn-ec2-launchtemplate-launchtemplatedata-keyname)" : String,
  "[LicenseSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-licensespecifications)" : [ LicenseSpecification, ... ],
  "[MaintenanceOptions](#cfn-ec2-launchtemplate-launchtemplatedata-maintenanceoptions)" : MaintenanceOptions,
  "[MetadataOptions](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions)" : MetadataOptions,
  "[Monitoring](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring)" : Monitoring,
  "[NetworkInterfaces](#cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces)" : [ NetworkInterface, ... ],
  "[Placement](#cfn-ec2-launchtemplate-launchtemplatedata-placement)" : Placement,
  "[PrivateDnsNameOptions](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions)" : PrivateDnsNameOptions,
  "[RamDiskId](#cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid)" : String,
  "[SecurityGroupIds](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids)" : [ String, ... ],
  "[SecurityGroups](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroups)" : [ String, ... ],
  "[TagSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications)" : [ TagSpecification, ... ],
  "[UserData](#cfn-ec2-launchtemplate-launchtemplatedata-userdata)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-syntax.yaml"></a>

```
  [BlockDeviceMappings](#cfn-ec2-launchtemplate-launchtemplatedata-blockdevicemappings): 
    - BlockDeviceMapping
  [CapacityReservationSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification): 
    CapacityReservationSpecification
  [CpuOptions](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions): 
    CpuOptions
  [CreditSpecification](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification): 
    CreditSpecification
  [DisableApiStop](#cfn-ec2-launchtemplate-launchtemplatedata-disableapistop): Boolean
  [DisableApiTermination](#cfn-ec2-launchtemplate-launchtemplatedata-disableapitermination): Boolean
  [EbsOptimized](#cfn-ec2-launchtemplate-launchtemplatedata-ebsoptimized): Boolean
  [ElasticGpuSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-elasticgpuspecifications): 
    - ElasticGpuSpecification
  [ElasticInferenceAccelerators](#cfn-ec2-launchtemplate-launchtemplatedata-elasticinferenceaccelerators): 
    - LaunchTemplateElasticInferenceAccelerator
  [EnclaveOptions](#cfn-ec2-launchtemplate-launchtemplatedata-enclaveoptions): 
    EnclaveOptions
  [HibernationOptions](#cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions): 
    HibernationOptions
  [IamInstanceProfile](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile): 
    IamInstanceProfile
  [ImageId](#cfn-ec2-launchtemplate-launchtemplatedata-imageid): String
  [InstanceInitiatedShutdownBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior): String
  [InstanceMarketOptions](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions): 
    InstanceMarketOptions
  [InstanceRequirements](#cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements): 
    InstanceRequirements
  [InstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancetype): String
  [KernelId](#cfn-ec2-launchtemplate-launchtemplatedata-kernelid): String
  [KeyName](#cfn-ec2-launchtemplate-launchtemplatedata-keyname): String
  [LicenseSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-licensespecifications): 
    - LicenseSpecification
  [MaintenanceOptions](#cfn-ec2-launchtemplate-launchtemplatedata-maintenanceoptions): 
    MaintenanceOptions
  [MetadataOptions](#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions): 
    MetadataOptions
  [Monitoring](#cfn-ec2-launchtemplate-launchtemplatedata-monitoring): 
    Monitoring
  [NetworkInterfaces](#cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces): 
    - NetworkInterface
  [Placement](#cfn-ec2-launchtemplate-launchtemplatedata-placement): 
    Placement
  [PrivateDnsNameOptions](#cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions): 
    PrivateDnsNameOptions
  [RamDiskId](#cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid): String
  [SecurityGroupIds](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids): 
    - String
  [SecurityGroups](#cfn-ec2-launchtemplate-launchtemplatedata-securitygroups): 
    - String
  [TagSpecifications](#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications): 
    - TagSpecification
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
The credit option for CPU usage of the instance\. Valid only for T instances\.  
*Required*: No  
*Type*: [CreditSpecification](aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableApiStop`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-disableapistop"></a>
Indicates whether to enable the instance for stop protection\. For more information, see [Stop protection](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Stop_Start.html#Using_StopProtection) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: Boolean  
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

`EnclaveOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-enclaveoptions"></a>
Indicates whether the instance is enabled for AWS Nitro Enclaves\. For more information, see [ What is AWS Nitro Enclaves?](https://docs.aws.amazon.com/enclaves/latest/user/nitro-enclave.html) in the * AWS Nitro Enclaves User Guide*\.  
You can't enable AWS Nitro Enclaves and hibernation on the same instance\.  
*Required*: No  
*Type*: [EnclaveOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-enclaveoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HibernationOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions"></a>
Indicates whether an instance is enabled for hibernation\. This parameter is valid only if the instance meets the [hibernation prerequisites](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/hibernating-prerequisites.html)\. For more information, see [Hibernate your instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: [HibernationOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamInstanceProfile`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile"></a>
The name or Amazon Resource Name \(ARN\) of an IAM instance profile\.  
*Required*: No  
*Type*: [IamInstanceProfile](aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-imageid"></a>
The ID of the AMI\. Alternatively, you can specify a Systems Manager parameter, which will resolve to an AMI ID on launch\.  
Valid formats:  
+  `ami-17characters00000` 
+  `resolve:ssm:parameter-name` 
+  `resolve:ssm:parameter-name:version-number` 
+  `resolve:ssm:parameter-name:label` 
For more information, see [Use a Systems Manager parameter to find an AMI](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/finding-an-ami.html#using-systems-manager-parameter-to-find-AMI) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceInitiatedShutdownBehavior`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instanceinitiatedshutdownbehavior"></a>
Indicates whether an instance stops or terminates when you initiate shutdown from the instance \(using the operating system command for system shutdown\)\.  
Default: `stop`   
*Required*: No  
*Type*: String  
*Allowed values*: `stop | terminate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceMarketOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions"></a>
The market \(purchasing\) option for the instances\.  
*Required*: No  
*Type*: [InstanceMarketOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceRequirements`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancerequirements"></a>
The attributes for the instance types\. When you specify instance attributes, Amazon EC2 will identify instance types with these attributes\.  
If you specify `InstanceRequirements`, you can't specify `InstanceType`\.  
*Required*: No  
*Type*: [InstanceRequirements](aws-properties-ec2-launchtemplate-launchtemplatedata-instancerequirements.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancetype"></a>
The instance type\. For more information, see [Instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
If you specify `InstanceType`, you can't specify `InstanceRequirements`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `a1.2xlarge | a1.4xlarge | a1.large | a1.medium | a1.metal | a1.xlarge | c1.medium | c1.xlarge | c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.12xlarge | c5.18xlarge | c5.24xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.metal | c5.xlarge | c5a.12xlarge | c5a.16xlarge | c5a.24xlarge | c5a.2xlarge | c5a.4xlarge | c5a.8xlarge | c5a.large | c5a.xlarge | c5ad.12xlarge | c5ad.16xlarge | c5ad.24xlarge | c5ad.2xlarge | c5ad.4xlarge | c5ad.8xlarge | c5ad.large | c5ad.xlarge | c5d.12xlarge | c5d.18xlarge | c5d.24xlarge | c5d.2xlarge | c5d.4xlarge | c5d.9xlarge | c5d.large | c5d.metal | c5d.xlarge | c5n.18xlarge | c5n.2xlarge | c5n.4xlarge | c5n.9xlarge | c5n.large | c5n.metal | c5n.xlarge | c6a.12xlarge | c6a.16xlarge | c6a.24xlarge | c6a.2xlarge | c6a.32xlarge | c6a.48xlarge | c6a.4xlarge | c6a.8xlarge | c6a.large | c6a.metal | c6a.xlarge | c6g.12xlarge | c6g.16xlarge | c6g.2xlarge | c6g.4xlarge | c6g.8xlarge | c6g.large | c6g.medium | c6g.metal | c6g.xlarge | c6gd.12xlarge | c6gd.16xlarge | c6gd.2xlarge | c6gd.4xlarge | c6gd.8xlarge | c6gd.large | c6gd.medium | c6gd.metal | c6gd.xlarge | c6gn.12xlarge | c6gn.16xlarge | c6gn.2xlarge | c6gn.4xlarge | c6gn.8xlarge | c6gn.large | c6gn.medium | c6gn.xlarge | c6i.12xlarge | c6i.16xlarge | c6i.24xlarge | c6i.2xlarge | c6i.32xlarge | c6i.4xlarge | c6i.8xlarge | c6i.large | c6i.metal | c6i.xlarge | c6id.12xlarge | c6id.16xlarge | c6id.24xlarge | c6id.2xlarge | c6id.32xlarge | c6id.4xlarge | c6id.8xlarge | c6id.large | c6id.metal | c6id.xlarge | c6in.12xlarge | c6in.16xlarge | c6in.24xlarge | c6in.2xlarge | c6in.32xlarge | c6in.4xlarge | c6in.8xlarge | c6in.large | c6in.xlarge | c7g.12xlarge | c7g.16xlarge | c7g.2xlarge | c7g.4xlarge | c7g.8xlarge | c7g.large | c7g.medium | c7g.xlarge | cc1.4xlarge | cc2.8xlarge | cg1.4xlarge | cr1.8xlarge | d2.2xlarge | d2.4xlarge | d2.8xlarge | d2.xlarge | d3.2xlarge | d3.4xlarge | d3.8xlarge | d3.xlarge | d3en.12xlarge | d3en.2xlarge | d3en.4xlarge | d3en.6xlarge | d3en.8xlarge | d3en.xlarge | dl1.24xlarge | f1.16xlarge | f1.2xlarge | f1.4xlarge | g2.2xlarge | g2.8xlarge | g3.16xlarge | g3.4xlarge | g3.8xlarge | g3s.xlarge | g4ad.16xlarge | g4ad.2xlarge | g4ad.4xlarge | g4ad.8xlarge | g4ad.xlarge | g4dn.12xlarge | g4dn.16xlarge | g4dn.2xlarge | g4dn.4xlarge | g4dn.8xlarge | g4dn.metal | g4dn.xlarge | g5.12xlarge | g5.16xlarge | g5.24xlarge | g5.2xlarge | g5.48xlarge | g5.4xlarge | g5.8xlarge | g5.xlarge | g5g.16xlarge | g5g.2xlarge | g5g.4xlarge | g5g.8xlarge | g5g.metal | g5g.xlarge | h1.16xlarge | h1.2xlarge | h1.4xlarge | h1.8xlarge | hi1.4xlarge | hpc6a.48xlarge | hpc6id.32xlarge | hs1.8xlarge | i2.2xlarge | i2.4xlarge | i2.8xlarge | i2.xlarge | i3.16xlarge | i3.2xlarge | i3.4xlarge | i3.8xlarge | i3.large | i3.metal | i3.xlarge | i3en.12xlarge | i3en.24xlarge | i3en.2xlarge | i3en.3xlarge | i3en.6xlarge | i3en.large | i3en.metal | i3en.xlarge | i4i.16xlarge | i4i.2xlarge | i4i.32xlarge | i4i.4xlarge | i4i.8xlarge | i4i.large | i4i.metal | i4i.xlarge | im4gn.16xlarge | im4gn.2xlarge | im4gn.4xlarge | im4gn.8xlarge | im4gn.large | im4gn.xlarge | inf1.24xlarge | inf1.2xlarge | inf1.6xlarge | inf1.xlarge | is4gen.2xlarge | is4gen.4xlarge | is4gen.8xlarge | is4gen.large | is4gen.medium | is4gen.xlarge | m1.large | m1.medium | m1.small | m1.xlarge | m2.2xlarge | m2.4xlarge | m2.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.16xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.16xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.8xlarge | m5.large | m5.metal | m5.xlarge | m5a.12xlarge | m5a.16xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.8xlarge | m5a.large | m5a.xlarge | m5ad.12xlarge | m5ad.16xlarge | m5ad.24xlarge | m5ad.2xlarge | m5ad.4xlarge | m5ad.8xlarge | m5ad.large | m5ad.xlarge | m5d.12xlarge | m5d.16xlarge | m5d.24xlarge | m5d.2xlarge | m5d.4xlarge | m5d.8xlarge | m5d.large | m5d.metal | m5d.xlarge | m5dn.12xlarge | m5dn.16xlarge | m5dn.24xlarge | m5dn.2xlarge | m5dn.4xlarge | m5dn.8xlarge | m5dn.large | m5dn.metal | m5dn.xlarge | m5n.12xlarge | m5n.16xlarge | m5n.24xlarge | m5n.2xlarge | m5n.4xlarge | m5n.8xlarge | m5n.large | m5n.metal | m5n.xlarge | m5zn.12xlarge | m5zn.2xlarge | m5zn.3xlarge | m5zn.6xlarge | m5zn.large | m5zn.metal | m5zn.xlarge | m6a.12xlarge | m6a.16xlarge | m6a.24xlarge | m6a.2xlarge | m6a.32xlarge | m6a.48xlarge | m6a.4xlarge | m6a.8xlarge | m6a.large | m6a.metal | m6a.xlarge | m6g.12xlarge | m6g.16xlarge | m6g.2xlarge | m6g.4xlarge | m6g.8xlarge | m6g.large | m6g.medium | m6g.metal | m6g.xlarge | m6gd.12xlarge | m6gd.16xlarge | m6gd.2xlarge | m6gd.4xlarge | m6gd.8xlarge | m6gd.large | m6gd.medium | m6gd.metal | m6gd.xlarge | m6i.12xlarge | m6i.16xlarge | m6i.24xlarge | m6i.2xlarge | m6i.32xlarge | m6i.4xlarge | m6i.8xlarge | m6i.large | m6i.metal | m6i.xlarge | m6id.12xlarge | m6id.16xlarge | m6id.24xlarge | m6id.2xlarge | m6id.32xlarge | m6id.4xlarge | m6id.8xlarge | m6id.large | m6id.metal | m6id.xlarge | m6idn.12xlarge | m6idn.16xlarge | m6idn.24xlarge | m6idn.2xlarge | m6idn.32xlarge | m6idn.4xlarge | m6idn.8xlarge | m6idn.large | m6idn.xlarge | m6in.12xlarge | m6in.16xlarge | m6in.24xlarge | m6in.2xlarge | m6in.32xlarge | m6in.4xlarge | m6in.8xlarge | m6in.large | m6in.xlarge | mac1.metal | mac2.metal | p2.16xlarge | p2.8xlarge | p2.xlarge | p3.16xlarge | p3.2xlarge | p3.8xlarge | p3dn.24xlarge | p4d.24xlarge | p4de.24xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.16xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.8xlarge | r5.large | r5.metal | r5.xlarge | r5a.12xlarge | r5a.16xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.8xlarge | r5a.large | r5a.xlarge | r5ad.12xlarge | r5ad.16xlarge | r5ad.24xlarge | r5ad.2xlarge | r5ad.4xlarge | r5ad.8xlarge | r5ad.large | r5ad.xlarge | r5b.12xlarge | r5b.16xlarge | r5b.24xlarge | r5b.2xlarge | r5b.4xlarge | r5b.8xlarge | r5b.large | r5b.metal | r5b.xlarge | r5d.12xlarge | r5d.16xlarge | r5d.24xlarge | r5d.2xlarge | r5d.4xlarge | r5d.8xlarge | r5d.large | r5d.metal | r5d.xlarge | r5dn.12xlarge | r5dn.16xlarge | r5dn.24xlarge | r5dn.2xlarge | r5dn.4xlarge | r5dn.8xlarge | r5dn.large | r5dn.metal | r5dn.xlarge | r5n.12xlarge | r5n.16xlarge | r5n.24xlarge | r5n.2xlarge | r5n.4xlarge | r5n.8xlarge | r5n.large | r5n.metal | r5n.xlarge | r6a.12xlarge | r6a.16xlarge | r6a.24xlarge | r6a.2xlarge | r6a.32xlarge | r6a.48xlarge | r6a.4xlarge | r6a.8xlarge | r6a.large | r6a.metal | r6a.xlarge | r6g.12xlarge | r6g.16xlarge | r6g.2xlarge | r6g.4xlarge | r6g.8xlarge | r6g.large | r6g.medium | r6g.metal | r6g.xlarge | r6gd.12xlarge | r6gd.16xlarge | r6gd.2xlarge | r6gd.4xlarge | r6gd.8xlarge | r6gd.large | r6gd.medium | r6gd.metal | r6gd.xlarge | r6i.12xlarge | r6i.16xlarge | r6i.24xlarge | r6i.2xlarge | r6i.32xlarge | r6i.4xlarge | r6i.8xlarge | r6i.large | r6i.metal | r6i.xlarge | r6id.12xlarge | r6id.16xlarge | r6id.24xlarge | r6id.2xlarge | r6id.32xlarge | r6id.4xlarge | r6id.8xlarge | r6id.large | r6id.metal | r6id.xlarge | r6idn.12xlarge | r6idn.16xlarge | r6idn.24xlarge | r6idn.2xlarge | r6idn.32xlarge | r6idn.4xlarge | r6idn.8xlarge | r6idn.large | r6idn.xlarge | r6in.12xlarge | r6in.16xlarge | r6in.24xlarge | r6in.2xlarge | r6in.32xlarge | r6in.4xlarge | r6in.8xlarge | r6in.large | r6in.xlarge | t1.micro | t2.2xlarge | t2.large | t2.medium | t2.micro | t2.nano | t2.small | t2.xlarge | t3.2xlarge | t3.large | t3.medium | t3.micro | t3.nano | t3.small | t3.xlarge | t3a.2xlarge | t3a.large | t3a.medium | t3a.micro | t3a.nano | t3a.small | t3a.xlarge | t4g.2xlarge | t4g.large | t4g.medium | t4g.micro | t4g.nano | t4g.small | t4g.xlarge | trn1.2xlarge | trn1.32xlarge | u-12tb1.112xlarge | u-12tb1.metal | u-18tb1.112xlarge | u-18tb1.metal | u-24tb1.112xlarge | u-24tb1.metal | u-3tb1.56xlarge | u-6tb1.112xlarge | u-6tb1.56xlarge | u-6tb1.metal | u-9tb1.112xlarge | u-9tb1.metal | vt1.24xlarge | vt1.3xlarge | vt1.6xlarge | x1.16xlarge | x1.32xlarge | x1e.16xlarge | x1e.2xlarge | x1e.32xlarge | x1e.4xlarge | x1e.8xlarge | x1e.xlarge | x2gd.12xlarge | x2gd.16xlarge | x2gd.2xlarge | x2gd.4xlarge | x2gd.8xlarge | x2gd.large | x2gd.medium | x2gd.metal | x2gd.xlarge | x2idn.16xlarge | x2idn.24xlarge | x2idn.32xlarge | x2idn.metal | x2iedn.16xlarge | x2iedn.24xlarge | x2iedn.2xlarge | x2iedn.32xlarge | x2iedn.4xlarge | x2iedn.8xlarge | x2iedn.metal | x2iedn.xlarge | x2iezn.12xlarge | x2iezn.2xlarge | x2iezn.4xlarge | x2iezn.6xlarge | x2iezn.8xlarge | x2iezn.metal | z1d.12xlarge | z1d.2xlarge | z1d.3xlarge | z1d.6xlarge | z1d.large | z1d.metal | z1d.xlarge`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KernelId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-kernelid"></a>
The ID of the kernel\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User Provided Kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon EC2 User Guide*\.  
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

`MaintenanceOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-maintenanceoptions"></a>
The maintenance options of your instance\.  
*Required*: No  
*Type*: [MaintenanceOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-maintenanceoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetadataOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions"></a>
The metadata options for the instance\. For more information, see [Instance metadata and user data](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: [MetadataOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Monitoring`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-monitoring"></a>
The monitoring for the instance\.  
*Required*: No  
*Type*: [Monitoring](aws-properties-ec2-launchtemplate-launchtemplatedata-monitoring.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaces`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-networkinterfaces"></a>
One or more network interfaces\. If you specify a network interface, you must specify any security groups and subnets as part of the network interface\.  
*Required*: No  
*Type*: List of [NetworkInterface](aws-properties-ec2-launchtemplate-networkinterface.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Placement`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement"></a>
The placement for the instance\.  
*Required*: No  
*Type*: [Placement](aws-properties-ec2-launchtemplate-launchtemplatedata-placement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateDnsNameOptions`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions"></a>
The options for the instance hostname\. The default values are inherited from the subnet\.  
*Required*: No  
*Type*: [PrivateDnsNameOptions](aws-properties-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RamDiskId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-ramdiskid"></a>
The ID of the RAM disk\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User provided kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon Elastic Compute Cloud User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-securitygroupids"></a>
One or more security group IDs\. You can create a security group using [CreateSecurityGroup](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSecurityGroup.html)\. You cannot specify both a security group ID and security name in the same request\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroups`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-securitygroups"></a>
One or more security group names\. For a nondefault VPC, you must use security group IDs instead\. You cannot specify both a security group ID and security name in the same request\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagSpecifications`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications"></a>
The tags to apply to the resources that are created during instance launch\.  
You can specify tags for the following resources only:  
+ Instances
+ Volumes
+ Elastic graphics
+ Spot Instance requests
+ Network interfaces
To tag a resource after it has been created, see [CreateTags](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTags.html)\.  
To tag the launch template itself, you must use the [TagSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLaunchTemplate.html) parameter\.
*Required*: No  
*Type*: List of [TagSpecification](aws-properties-ec2-launchtemplate-tagspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserData`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-userdata"></a>
The user data to make available to the instance\. You must provide base64\-encoded text\. User data is limited to 16 KB\. For more information, see [Run commands on your Linux instance at launch](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html) \(Linux\) or [Work with instance user data](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/instancedata-add-user-data.html) \(Windows\) in the *Amazon Elastic Compute Cloud User Guide*\.  
If you are creating the launch template for use with AWS Batch, the user data must be provided in the [ MIME multi\-part archive format](https://cloudinit.readthedocs.io/en/latest/topics/format.html#mime-multi-part-archive)\. For more information, see [Amazon EC2 user data in launch templates](https://docs.aws.amazon.com/batch/latest/userguide/launch-templates.html) in the * AWS Batch User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata--seealso"></a>
+  [RequestLaunchTemplateData](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RequestLaunchTemplateData.html) in the *Amazon EC2 API Reference* 


# AWS::EC2::Instance<a name="aws-properties-ec2-instance"></a>

Specifies an EC2 instance\.

If an Elastic IP address is attached to your instance, AWS CloudFormation reattaches the Elastic IP address after it updates the instance\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

## Syntax<a name="aws-properties-ec2-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Instance",
  "Properties" : {
      "[AdditionalInfo](#cfn-ec2-instance-additionalinfo)" : String,
      "[Affinity](#cfn-ec2-instance-affinity)" : String,
      "[AvailabilityZone](#cfn-ec2-instance-availabilityzone)" : String,
      "[BlockDeviceMappings](#cfn-ec2-instance-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
      "[CpuOptions](#cfn-ec2-instance-cpuoptions)" : CpuOptions,
      "[CreditSpecification](#cfn-ec2-instance-creditspecification)" : CreditSpecification,
      "[DisableApiTermination](#cfn-ec2-instance-disableapitermination)" : Boolean,
      "[EbsOptimized](#cfn-ec2-instance-ebsoptimized)" : Boolean,
      "[ElasticGpuSpecifications](#cfn-ec2-instance-elasticgpuspecifications)" : [ ElasticGpuSpecification, ... ],
      "[ElasticInferenceAccelerators](#cfn-ec2-instance-elasticinferenceaccelerators)" : [ ElasticInferenceAccelerator, ... ],
      "[EnclaveOptions](#cfn-ec2-instance-enclaveoptions)" : EnclaveOptions,
      "[HibernationOptions](#cfn-ec2-instance-hibernationoptions)" : HibernationOptions,
      "[HostId](#cfn-ec2-instance-hostid)" : String,
      "[HostResourceGroupArn](#cfn-ec2-instance-hostresourcegrouparn)" : String,
      "[IamInstanceProfile](#cfn-ec2-instance-iaminstanceprofile)" : String,
      "[ImageId](#cfn-ec2-instance-imageid)" : String,
      "[InstanceInitiatedShutdownBehavior](#cfn-ec2-instance-instanceinitiatedshutdownbehavior)" : String,
      "[InstanceType](#cfn-ec2-instance-instancetype)" : String,
      "[Ipv6AddressCount](#cfn-ec2-instance-ipv6addresscount)" : Integer,
      "[Ipv6Addresses](#cfn-ec2-instance-ipv6addresses)" : [ InstanceIpv6Address, ... ],
      "[KernelId](#cfn-ec2-instance-kernelid)" : String,
      "[KeyName](#cfn-ec2-instance-keyname)" : String,
      "[LaunchTemplate](#cfn-ec2-instance-launchtemplate)" : LaunchTemplateSpecification,
      "[LicenseSpecifications](#cfn-ec2-instance-licensespecifications)" : [ LicenseSpecification, ... ],
      "[Monitoring](#cfn-ec2-instance-monitoring)" : Boolean,
      "[NetworkInterfaces](#cfn-ec2-instance-networkinterfaces)" : [ NetworkInterface, ... ],
      "[PlacementGroupName](#cfn-ec2-instance-placementgroupname)" : String,
      "[PrivateDnsNameOptions](#cfn-ec2-instance-privatednsnameoptions)" : PrivateDnsNameOptions,
      "[PrivateIpAddress](#cfn-ec2-instance-privateipaddress)" : String,
      "[PropagateTagsToVolumeOnCreation](#cfn-ec2-instance-propagatetagstovolumeoncreation)" : Boolean,
      "[RamdiskId](#cfn-ec2-instance-ramdiskid)" : String,
      "[SecurityGroupIds](#cfn-ec2-instance-securitygroupids)" : [ String, ... ],
      "[SecurityGroups](#cfn-ec2-instance-securitygroups)" : [ String, ... ],
      "[SourceDestCheck](#cfn-ec2-instance-sourcedestcheck)" : Boolean,
      "[SsmAssociations](#cfn-ec2-instance-ssmassociations)" : [ SsmAssociation, ... ],
      "[SubnetId](#cfn-ec2-instance-subnetid)" : String,
      "[Tags](#cfn-ec2-instance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Tenancy](#cfn-ec2-instance-tenancy)" : String,
      "[UserData](#cfn-ec2-instance-userdata)" : String,
      "[Volumes](#cfn-ec2-instance-volumes)" : [ Volume, ... ]
    }
}
```

### YAML<a name="aws-properties-ec2-instance-syntax.yaml"></a>

```
Type: AWS::EC2::Instance
Properties: 
  [AdditionalInfo](#cfn-ec2-instance-additionalinfo): String
  [Affinity](#cfn-ec2-instance-affinity): String
  [AvailabilityZone](#cfn-ec2-instance-availabilityzone): String
  [BlockDeviceMappings](#cfn-ec2-instance-blockdevicemappings): 
    - BlockDeviceMapping
  [CpuOptions](#cfn-ec2-instance-cpuoptions): 
    CpuOptions
  [CreditSpecification](#cfn-ec2-instance-creditspecification): 
    CreditSpecification
  [DisableApiTermination](#cfn-ec2-instance-disableapitermination): Boolean
  [EbsOptimized](#cfn-ec2-instance-ebsoptimized): Boolean
  [ElasticGpuSpecifications](#cfn-ec2-instance-elasticgpuspecifications): 
    - ElasticGpuSpecification
  [ElasticInferenceAccelerators](#cfn-ec2-instance-elasticinferenceaccelerators): 
    - ElasticInferenceAccelerator
  [EnclaveOptions](#cfn-ec2-instance-enclaveoptions): 
    EnclaveOptions
  [HibernationOptions](#cfn-ec2-instance-hibernationoptions): 
    HibernationOptions
  [HostId](#cfn-ec2-instance-hostid): String
  [HostResourceGroupArn](#cfn-ec2-instance-hostresourcegrouparn): String
  [IamInstanceProfile](#cfn-ec2-instance-iaminstanceprofile): String
  [ImageId](#cfn-ec2-instance-imageid): String
  [InstanceInitiatedShutdownBehavior](#cfn-ec2-instance-instanceinitiatedshutdownbehavior): String
  [InstanceType](#cfn-ec2-instance-instancetype): String
  [Ipv6AddressCount](#cfn-ec2-instance-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-instance-ipv6addresses): 
    - InstanceIpv6Address
  [KernelId](#cfn-ec2-instance-kernelid): String
  [KeyName](#cfn-ec2-instance-keyname): String
  [LaunchTemplate](#cfn-ec2-instance-launchtemplate): 
    LaunchTemplateSpecification
  [LicenseSpecifications](#cfn-ec2-instance-licensespecifications): 
    - LicenseSpecification
  [Monitoring](#cfn-ec2-instance-monitoring): Boolean
  [NetworkInterfaces](#cfn-ec2-instance-networkinterfaces): 
    - NetworkInterface
  [PlacementGroupName](#cfn-ec2-instance-placementgroupname): String
  [PrivateDnsNameOptions](#cfn-ec2-instance-privatednsnameoptions): 
    PrivateDnsNameOptions
  [PrivateIpAddress](#cfn-ec2-instance-privateipaddress): String
  [PropagateTagsToVolumeOnCreation](#cfn-ec2-instance-propagatetagstovolumeoncreation): Boolean
  [RamdiskId](#cfn-ec2-instance-ramdiskid): String
  [SecurityGroupIds](#cfn-ec2-instance-securitygroupids): 
    - String
  [SecurityGroups](#cfn-ec2-instance-securitygroups): 
    - String
  [SourceDestCheck](#cfn-ec2-instance-sourcedestcheck): Boolean
  [SsmAssociations](#cfn-ec2-instance-ssmassociations): 
    - SsmAssociation
  [SubnetId](#cfn-ec2-instance-subnetid): String
  [Tags](#cfn-ec2-instance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Tenancy](#cfn-ec2-instance-tenancy): String
  [UserData](#cfn-ec2-instance-userdata): String
  [Volumes](#cfn-ec2-instance-volumes): 
    - Volume
```

## Properties<a name="aws-properties-ec2-instance-properties"></a>

`AdditionalInfo`  <a name="cfn-ec2-instance-additionalinfo"></a>
This property is reserved for internal use\. If you use it, the stack fails with this error: `Bad property set: [Testing this property] (Service: AmazonEC2; Status Code: 400; Error Code: InvalidParameterCombination; Request ID: 0XXXXXX-49c7-4b40-8bcc-76885dcXXXXX)`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Affinity`  <a name="cfn-ec2-instance-affinity"></a>
Indicates whether the instance is associated with a dedicated host\. If you want the instance to always restart on the same host on which it was launched, specify `host`\. If you want the instance to restart on any available host, but try to launch onto the last host it ran on \(on a best\-effort basis\), specify `default`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-instance-availabilityzone"></a>
The Availability Zone of the instance\.  
If not specified, an Availability Zone will be automatically chosen for you based on the load balancing criteria for the Region\.  
This parameter is not supported by [DescribeImageAttribute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeImageAttribute.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BlockDeviceMappings`  <a name="cfn-ec2-instance-blockdevicemappings"></a>
The block device mapping entries that defines the block devices to attach to the instance at launch\.  
By default, the block devices specified in the block device mapping for the AMI are used\. You can override the AMI block device mapping using the instance block device mapping\. For the root volume, you can override only the volume size, volume type, volume encryption settings, and the `DeleteOnTermination` setting\.  
After the instance is running, you can modify only the `DeleteOnTermination` parameter for the attached volumes without interrupting the instance\. Modifying any other parameter results in instance [ replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)\.
*Required*: No  
*Type*: List of [BlockDeviceMapping](aws-properties-ec2-blockdev-mapping.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`CpuOptions`  <a name="cfn-ec2-instance-cpuoptions"></a>
The CPU options for the instance\. For more information, see [Optimize CPU options](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-optimize-cpu.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: [CpuOptions](aws-properties-ec2-instance-cpuoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CreditSpecification`  <a name="cfn-ec2-instance-creditspecification"></a>
The credit option for CPU usage of the burstable performance instance\. Valid values are `standard` and `unlimited`\. To change this attribute after launch, use [ ModifyInstanceCreditSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyInstanceCreditSpecification.html)\. For more information, see [Burstable performance instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/burstable-performance-instances.html) in the *Amazon EC2 User Guide*\.  
Default: `standard` \(T2 instances\) or `unlimited` \(T3/T3a/T4g instances\)  
For T3 instances with `host` tenancy, only `standard` is supported\.  
*Required*: No  
*Type*: [CreditSpecification](aws-properties-ec2-instance-creditspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableApiTermination`  <a name="cfn-ec2-instance-disableapitermination"></a>
If you set this parameter to `true`, you can't terminate the instance using the Amazon EC2 console, CLI, or API; otherwise, you can\. To change this attribute after launch, use [ModifyInstanceAttribute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyInstanceAttribute.html)\. Alternatively, if you set `InstanceInitiatedShutdownBehavior` to `terminate`, you can terminate the instance by running the shutdown command from the instance\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbsOptimized`  <a name="cfn-ec2-instance-ebsoptimized"></a>
Indicates whether the instance is optimized for Amazon EBS I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal Amazon EBS I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when using an EBS\-optimized instance\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`ElasticGpuSpecifications`  <a name="cfn-ec2-instance-elasticgpuspecifications"></a>
An elastic GPU to associate with the instance\. An Elastic GPU is a GPU resource that you can attach to your Windows instance to accelerate the graphics performance of your applications\. For more information, see [Amazon EC2 Elastic GPUs](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/elastic-graphics.html) in the *Amazon EC2 User Guide*\.  
*Required*: No  
*Type*: List of [ElasticGpuSpecification](aws-properties-ec2-instance-elasticgpuspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ElasticInferenceAccelerators`  <a name="cfn-ec2-instance-elasticinferenceaccelerators"></a>
An elastic inference accelerator to associate with the instance\. Elastic inference accelerators are a resource you can attach to your Amazon EC2 instances to accelerate your Deep Learning \(DL\) inference workloads\.  
You cannot specify accelerators from different generations in the same request\.  
*Required*: No  
*Type*: List of [ElasticInferenceAccelerator](aws-properties-ec2-instance-elasticinferenceaccelerator.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnclaveOptions`  <a name="cfn-ec2-instance-enclaveoptions"></a>
Indicates whether the instance is enabled for AWS Nitro Enclaves\.  
*Required*: No  
*Type*: [EnclaveOptions](aws-properties-ec2-instance-enclaveoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HibernationOptions`  <a name="cfn-ec2-instance-hibernationoptions"></a>
Indicates whether an instance is enabled for hibernation\. For more information, see [Hibernate your instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html) in the *Amazon EC2 User Guide*\.  
You can't enable hibernation and AWS Nitro Enclaves on the same instance\.  
*Required*: No  
*Type*: [HibernationOptions](aws-properties-ec2-instance-hibernationoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostId`  <a name="cfn-ec2-instance-hostid"></a>
If you specify host for the `Affinity` property, the ID of a dedicated host that the instance is associated with\. If you don't specify an ID, Amazon EC2 launches the instance onto any available, compatible dedicated host in your account\. This type of launch is called an untargeted launch\. Note that for untargeted launches, you must have a compatible, dedicated host available to successfully launch instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`HostResourceGroupArn`  <a name="cfn-ec2-instance-hostresourcegrouparn"></a>
The ARN of the host resource group in which to launch the instances\. If you specify a host resource group ARN, omit the **Tenancy** parameter or set it to `host`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamInstanceProfile`  <a name="cfn-ec2-instance-iaminstanceprofile"></a>
The name of an IAM instance profile\. To create a new IAM instance profile, use the [AWS::IAM::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html) resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageId`  <a name="cfn-ec2-instance-imageid"></a>
The ID of the AMI\. An AMI ID is required to launch an instance and must be specified here or in a launch template\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceInitiatedShutdownBehavior`  <a name="cfn-ec2-instance-instanceinitiatedshutdownbehavior"></a>
Indicates whether an instance stops or terminates when you initiate shutdown from the instance \(using the operating system command for system shutdown\)\.  
Default: `stop`   
*Required*: No  
*Type*: String  
*Allowed values*: `stop | terminate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-ec2-instance-instancetype"></a>
The instance type\. For more information, see [Instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon EC2 User Guide*\.  
Default: `m1.small`   
*Required*: No  
*Type*: String  
*Allowed values*: `a1.2xlarge | a1.4xlarge | a1.large | a1.medium | a1.metal | a1.xlarge | c1.medium | c1.xlarge | c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.12xlarge | c5.18xlarge | c5.24xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.metal | c5.xlarge | c5a.12xlarge | c5a.16xlarge | c5a.24xlarge | c5a.2xlarge | c5a.4xlarge | c5a.8xlarge | c5a.large | c5a.xlarge | c5ad.12xlarge | c5ad.16xlarge | c5ad.24xlarge | c5ad.2xlarge | c5ad.4xlarge | c5ad.8xlarge | c5ad.large | c5ad.xlarge | c5d.12xlarge | c5d.18xlarge | c5d.24xlarge | c5d.2xlarge | c5d.4xlarge | c5d.9xlarge | c5d.large | c5d.metal | c5d.xlarge | c5n.18xlarge | c5n.2xlarge | c5n.4xlarge | c5n.9xlarge | c5n.large | c5n.metal | c5n.xlarge | c6a.12xlarge | c6a.16xlarge | c6a.24xlarge | c6a.2xlarge | c6a.32xlarge | c6a.48xlarge | c6a.4xlarge | c6a.8xlarge | c6a.large | c6a.metal | c6a.xlarge | c6g.12xlarge | c6g.16xlarge | c6g.2xlarge | c6g.4xlarge | c6g.8xlarge | c6g.large | c6g.medium | c6g.metal | c6g.xlarge | c6gd.12xlarge | c6gd.16xlarge | c6gd.2xlarge | c6gd.4xlarge | c6gd.8xlarge | c6gd.large | c6gd.medium | c6gd.metal | c6gd.xlarge | c6gn.12xlarge | c6gn.16xlarge | c6gn.2xlarge | c6gn.4xlarge | c6gn.8xlarge | c6gn.large | c6gn.medium | c6gn.xlarge | c6i.12xlarge | c6i.16xlarge | c6i.24xlarge | c6i.2xlarge | c6i.32xlarge | c6i.4xlarge | c6i.8xlarge | c6i.large | c6i.metal | c6i.xlarge | c6id.12xlarge | c6id.16xlarge | c6id.24xlarge | c6id.2xlarge | c6id.32xlarge | c6id.4xlarge | c6id.8xlarge | c6id.large | c6id.metal | c6id.xlarge | c6in.12xlarge | c6in.16xlarge | c6in.24xlarge | c6in.2xlarge | c6in.32xlarge | c6in.4xlarge | c6in.8xlarge | c6in.large | c6in.xlarge | c7g.12xlarge | c7g.16xlarge | c7g.2xlarge | c7g.4xlarge | c7g.8xlarge | c7g.large | c7g.medium | c7g.xlarge | cc1.4xlarge | cc2.8xlarge | cg1.4xlarge | cr1.8xlarge | d2.2xlarge | d2.4xlarge | d2.8xlarge | d2.xlarge | d3.2xlarge | d3.4xlarge | d3.8xlarge | d3.xlarge | d3en.12xlarge | d3en.2xlarge | d3en.4xlarge | d3en.6xlarge | d3en.8xlarge | d3en.xlarge | dl1.24xlarge | f1.16xlarge | f1.2xlarge | f1.4xlarge | g2.2xlarge | g2.8xlarge | g3.16xlarge | g3.4xlarge | g3.8xlarge | g3s.xlarge | g4ad.16xlarge | g4ad.2xlarge | g4ad.4xlarge | g4ad.8xlarge | g4ad.xlarge | g4dn.12xlarge | g4dn.16xlarge | g4dn.2xlarge | g4dn.4xlarge | g4dn.8xlarge | g4dn.metal | g4dn.xlarge | g5.12xlarge | g5.16xlarge | g5.24xlarge | g5.2xlarge | g5.48xlarge | g5.4xlarge | g5.8xlarge | g5.xlarge | g5g.16xlarge | g5g.2xlarge | g5g.4xlarge | g5g.8xlarge | g5g.metal | g5g.xlarge | h1.16xlarge | h1.2xlarge | h1.4xlarge | h1.8xlarge | hi1.4xlarge | hpc6a.48xlarge | hpc6id.32xlarge | hs1.8xlarge | i2.2xlarge | i2.4xlarge | i2.8xlarge | i2.xlarge | i3.16xlarge | i3.2xlarge | i3.4xlarge | i3.8xlarge | i3.large | i3.metal | i3.xlarge | i3en.12xlarge | i3en.24xlarge | i3en.2xlarge | i3en.3xlarge | i3en.6xlarge | i3en.large | i3en.metal | i3en.xlarge | i4i.16xlarge | i4i.2xlarge | i4i.32xlarge | i4i.4xlarge | i4i.8xlarge | i4i.large | i4i.metal | i4i.xlarge | im4gn.16xlarge | im4gn.2xlarge | im4gn.4xlarge | im4gn.8xlarge | im4gn.large | im4gn.xlarge | inf1.24xlarge | inf1.2xlarge | inf1.6xlarge | inf1.xlarge | is4gen.2xlarge | is4gen.4xlarge | is4gen.8xlarge | is4gen.large | is4gen.medium | is4gen.xlarge | m1.large | m1.medium | m1.small | m1.xlarge | m2.2xlarge | m2.4xlarge | m2.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.16xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.16xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.8xlarge | m5.large | m5.metal | m5.xlarge | m5a.12xlarge | m5a.16xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.8xlarge | m5a.large | m5a.xlarge | m5ad.12xlarge | m5ad.16xlarge | m5ad.24xlarge | m5ad.2xlarge | m5ad.4xlarge | m5ad.8xlarge | m5ad.large | m5ad.xlarge | m5d.12xlarge | m5d.16xlarge | m5d.24xlarge | m5d.2xlarge | m5d.4xlarge | m5d.8xlarge | m5d.large | m5d.metal | m5d.xlarge | m5dn.12xlarge | m5dn.16xlarge | m5dn.24xlarge | m5dn.2xlarge | m5dn.4xlarge | m5dn.8xlarge | m5dn.large | m5dn.metal | m5dn.xlarge | m5n.12xlarge | m5n.16xlarge | m5n.24xlarge | m5n.2xlarge | m5n.4xlarge | m5n.8xlarge | m5n.large | m5n.metal | m5n.xlarge | m5zn.12xlarge | m5zn.2xlarge | m5zn.3xlarge | m5zn.6xlarge | m5zn.large | m5zn.metal | m5zn.xlarge | m6a.12xlarge | m6a.16xlarge | m6a.24xlarge | m6a.2xlarge | m6a.32xlarge | m6a.48xlarge | m6a.4xlarge | m6a.8xlarge | m6a.large | m6a.metal | m6a.xlarge | m6g.12xlarge | m6g.16xlarge | m6g.2xlarge | m6g.4xlarge | m6g.8xlarge | m6g.large | m6g.medium | m6g.metal | m6g.xlarge | m6gd.12xlarge | m6gd.16xlarge | m6gd.2xlarge | m6gd.4xlarge | m6gd.8xlarge | m6gd.large | m6gd.medium | m6gd.metal | m6gd.xlarge | m6i.12xlarge | m6i.16xlarge | m6i.24xlarge | m6i.2xlarge | m6i.32xlarge | m6i.4xlarge | m6i.8xlarge | m6i.large | m6i.metal | m6i.xlarge | m6id.12xlarge | m6id.16xlarge | m6id.24xlarge | m6id.2xlarge | m6id.32xlarge | m6id.4xlarge | m6id.8xlarge | m6id.large | m6id.metal | m6id.xlarge | m6idn.12xlarge | m6idn.16xlarge | m6idn.24xlarge | m6idn.2xlarge | m6idn.32xlarge | m6idn.4xlarge | m6idn.8xlarge | m6idn.large | m6idn.xlarge | m6in.12xlarge | m6in.16xlarge | m6in.24xlarge | m6in.2xlarge | m6in.32xlarge | m6in.4xlarge | m6in.8xlarge | m6in.large | m6in.xlarge | mac1.metal | mac2.metal | p2.16xlarge | p2.8xlarge | p2.xlarge | p3.16xlarge | p3.2xlarge | p3.8xlarge | p3dn.24xlarge | p4d.24xlarge | p4de.24xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.16xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.8xlarge | r5.large | r5.metal | r5.xlarge | r5a.12xlarge | r5a.16xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.8xlarge | r5a.large | r5a.xlarge | r5ad.12xlarge | r5ad.16xlarge | r5ad.24xlarge | r5ad.2xlarge | r5ad.4xlarge | r5ad.8xlarge | r5ad.large | r5ad.xlarge | r5b.12xlarge | r5b.16xlarge | r5b.24xlarge | r5b.2xlarge | r5b.4xlarge | r5b.8xlarge | r5b.large | r5b.metal | r5b.xlarge | r5d.12xlarge | r5d.16xlarge | r5d.24xlarge | r5d.2xlarge | r5d.4xlarge | r5d.8xlarge | r5d.large | r5d.metal | r5d.xlarge | r5dn.12xlarge | r5dn.16xlarge | r5dn.24xlarge | r5dn.2xlarge | r5dn.4xlarge | r5dn.8xlarge | r5dn.large | r5dn.metal | r5dn.xlarge | r5n.12xlarge | r5n.16xlarge | r5n.24xlarge | r5n.2xlarge | r5n.4xlarge | r5n.8xlarge | r5n.large | r5n.metal | r5n.xlarge | r6a.12xlarge | r6a.16xlarge | r6a.24xlarge | r6a.2xlarge | r6a.32xlarge | r6a.48xlarge | r6a.4xlarge | r6a.8xlarge | r6a.large | r6a.metal | r6a.xlarge | r6g.12xlarge | r6g.16xlarge | r6g.2xlarge | r6g.4xlarge | r6g.8xlarge | r6g.large | r6g.medium | r6g.metal | r6g.xlarge | r6gd.12xlarge | r6gd.16xlarge | r6gd.2xlarge | r6gd.4xlarge | r6gd.8xlarge | r6gd.large | r6gd.medium | r6gd.metal | r6gd.xlarge | r6i.12xlarge | r6i.16xlarge | r6i.24xlarge | r6i.2xlarge | r6i.32xlarge | r6i.4xlarge | r6i.8xlarge | r6i.large | r6i.metal | r6i.xlarge | r6id.12xlarge | r6id.16xlarge | r6id.24xlarge | r6id.2xlarge | r6id.32xlarge | r6id.4xlarge | r6id.8xlarge | r6id.large | r6id.metal | r6id.xlarge | r6idn.12xlarge | r6idn.16xlarge | r6idn.24xlarge | r6idn.2xlarge | r6idn.32xlarge | r6idn.4xlarge | r6idn.8xlarge | r6idn.large | r6idn.xlarge | r6in.12xlarge | r6in.16xlarge | r6in.24xlarge | r6in.2xlarge | r6in.32xlarge | r6in.4xlarge | r6in.8xlarge | r6in.large | r6in.xlarge | t1.micro | t2.2xlarge | t2.large | t2.medium | t2.micro | t2.nano | t2.small | t2.xlarge | t3.2xlarge | t3.large | t3.medium | t3.micro | t3.nano | t3.small | t3.xlarge | t3a.2xlarge | t3a.large | t3a.medium | t3a.micro | t3a.nano | t3a.small | t3a.xlarge | t4g.2xlarge | t4g.large | t4g.medium | t4g.micro | t4g.nano | t4g.small | t4g.xlarge | trn1.2xlarge | trn1.32xlarge | u-12tb1.112xlarge | u-12tb1.metal | u-18tb1.112xlarge | u-18tb1.metal | u-24tb1.112xlarge | u-24tb1.metal | u-3tb1.56xlarge | u-6tb1.112xlarge | u-6tb1.56xlarge | u-6tb1.metal | u-9tb1.112xlarge | u-9tb1.metal | vt1.24xlarge | vt1.3xlarge | vt1.6xlarge | x1.16xlarge | x1.32xlarge | x1e.16xlarge | x1e.2xlarge | x1e.32xlarge | x1e.4xlarge | x1e.8xlarge | x1e.xlarge | x2gd.12xlarge | x2gd.16xlarge | x2gd.2xlarge | x2gd.4xlarge | x2gd.8xlarge | x2gd.large | x2gd.medium | x2gd.metal | x2gd.xlarge | x2idn.16xlarge | x2idn.24xlarge | x2idn.32xlarge | x2idn.metal | x2iedn.16xlarge | x2iedn.24xlarge | x2iedn.2xlarge | x2iedn.32xlarge | x2iedn.4xlarge | x2iedn.8xlarge | x2iedn.metal | x2iedn.xlarge | x2iezn.12xlarge | x2iezn.2xlarge | x2iezn.4xlarge | x2iezn.6xlarge | x2iezn.8xlarge | x2iezn.metal | z1d.12xlarge | z1d.2xlarge | z1d.3xlarge | z1d.6xlarge | z1d.large | z1d.metal | z1d.xlarge`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Ipv6AddressCount`  <a name="cfn-ec2-instance-ipv6addresscount"></a>
\[EC2\-VPC\] The number of IPv6 addresses to associate with the primary network interface\. Amazon EC2 chooses the IPv6 addresses from the range of your subnet\. You cannot specify this option and the option to assign specific IPv6 addresses in the same request\. You can specify this option if you've specified a minimum number of instances to launch\.  
You cannot specify this option and the network interfaces option in the same request\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ipv6Addresses`  <a name="cfn-ec2-instance-ipv6addresses"></a>
\[EC2\-VPC\] The IPv6 addresses from the range of the subnet to associate with the primary network interface\. You cannot specify this option and the option to assign a number of IPv6 addresses in the same request\. You cannot specify this option if you've specified a minimum number of instances to launch\.  
You cannot specify this option and the network interfaces option in the same request\.  
*Required*: No  
*Type*: List of [InstanceIpv6Address](aws-properties-ec2-instance-instanceipv6address.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KernelId`  <a name="cfn-ec2-instance-kernelid"></a>
The ID of the kernel\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [PV\-GRUB](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon EC2 User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`KeyName`  <a name="cfn-ec2-instance-keyname"></a>
The name of the key pair\. You can create a key pair using [CreateKeyPair](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateKeyPair.html) or [ImportKeyPair](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportKeyPair.html)\.  
If you do not specify a key pair, you can't connect to the instance unless you choose an AMI that is configured to allow users another way to log in\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchTemplate`  <a name="cfn-ec2-instance-launchtemplate"></a>
The launch template to use to launch the instances\. Any parameters that you specify in the AWS CloudFormation template override the same parameters in the launch template\. You can specify either the name or ID of a launch template, but not both\.  
*Required*: No  
*Type*: [LaunchTemplateSpecification](aws-properties-ec2-instance-launchtemplatespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LicenseSpecifications`  <a name="cfn-ec2-instance-licensespecifications"></a>
The license configurations\.  
*Required*: No  
*Type*: List of [LicenseSpecification](aws-properties-ec2-instance-licensespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Monitoring`  <a name="cfn-ec2-instance-monitoring"></a>
Specifies whether detailed monitoring is enabled for the instance\. Specify `true` to enable detailed monitoring\. Otherwise, basic monitoring is enabled\. For more information about detailed monitoring, see [Enable or turn off detailed monitoring for your instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch-new.html) in the *Amazon EC2 User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaces`  <a name="cfn-ec2-instance-networkinterfaces"></a>
The network interfaces to associate with the instance\.  
If you use this property to point to a network interface, you must terminate the original interface before attaching a new one to allow the update of the instance to succeed\.  
If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the [ DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the VPC\-gateway attachment\.
*Required*: No  
*Type*: List of [NetworkInterface](aws-properties-ec2-network-iface-embedded.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlacementGroupName`  <a name="cfn-ec2-instance-placementgroupname"></a>
The name of an existing placement group that you want to launch the instance into \(cluster \| partition \| spread\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrivateDnsNameOptions`  <a name="cfn-ec2-instance-privatednsnameoptions"></a>
The options for the instance hostname\.  
*Required*: No  
*Type*: [PrivateDnsNameOptions](aws-properties-ec2-instance-privatednsnameoptions.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-instance-privateipaddress"></a>
\[EC2\-VPC\] The primary IPv4 address\. You must specify a value from the IPv4 address range of the subnet\.  
Only one private IP address can be designated as primary\. You can't specify this option if you've specified the option to designate a private IP address as the primary IP address in a network interface specification\. You cannot specify this option if you're launching more than one instance in the request\.  
You cannot specify this option and the network interfaces option in the same request\.  
If you make an update to an instance that requires replacement, you must assign a new private IP address\. During a replacement, AWS CloudFormation creates a new instance but doesn't delete the old instance until the stack has successfully updated\. If the stack update fails, AWS CloudFormation uses the old instance to roll back the stack to the previous working state\. The old and new instances cannot have the same private IP address\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PropagateTagsToVolumeOnCreation`  <a name="cfn-ec2-instance-propagatetagstovolumeoncreation"></a>
Indicates whether to assign the tags from the instance to all of the volumes attached to the instance at launch\. If you specify `true` and you assign tags to the instance, those tags are automatically assigned to all of the volumes that you attach to the instance at launch\. If you specify `false`, those tags are not assigned to the attached volumes\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RamdiskId`  <a name="cfn-ec2-instance-ramdiskid"></a>
The ID of the RAM disk to select\. Some kernels require additional drivers at launch\. Check the kernel requirements for information about whether you need to specify a RAM disk\. To find kernel requirements, go to the AWS Resource Center and search for the kernel ID\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [PV\-GRUB](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon EC2 User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SecurityGroupIds`  <a name="cfn-ec2-instance-securitygroupids"></a>
The IDs of the security groups\. You can create a security group using [CreateSecurityGroup](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSecurityGroup.html)\.  
If you specify a network interface, you must specify any security groups as part of the network interface\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SecurityGroups`  <a name="cfn-ec2-instance-securitygroups"></a>
\[EC2\-Classic, default VPC\] The names of the security groups\. For a nondefault VPC, you must use security group IDs instead\.  
You cannot specify this option and the network interfaces option in the same request\. The list can contain both the name of existing Amazon EC2 security groups or references to AWS::EC2::SecurityGroup resources created in the template\.  
Default: Amazon EC2 uses the default security group\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceDestCheck`  <a name="cfn-ec2-instance-sourcedestcheck"></a>
Enable or disable source/destination checks, which ensure that the instance is either the source or the destination of any traffic that it receives\. If the value is `true`, source/destination checks are enabled; otherwise, they are disabled\. The default value is `true`\. You must disable source/destination checks if the instance runs services such as network address translation, routing, or firewalls\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SsmAssociations`  <a name="cfn-ec2-instance-ssmassociations"></a>
The SSM [ document](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-document.html) and parameter values in AWS Systems Manager to associate with this instance\. To use this property, you must specify an IAM instance profile role for the instance\. For more information, see [Create an IAM instance profile for Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-configuring-access-role.html) in the *AWS Systems Manager User Guide*\.  
You can currently associate only one document with an instance\.
*Required*: No  
*Type*: List of [SsmAssociation](aws-properties-ec2-instance-ssmassociations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-ec2-instance-subnetid"></a>
\[EC2\-VPC\] The ID of the subnet to launch the instance into\.  
If you specify a network interface, you must specify any subnets as part of the network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-instance-tags"></a>
The tags to add to the instance\. These tags are not applied to the EBS volumes, such as the root volume\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tenancy`  <a name="cfn-ec2-instance-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of `dedicated` runs on single\-tenant hardware\.   
*Required*: No  
*Type*: String  
*Allowed values*: `dedicated | default | host`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`UserData`  <a name="cfn-ec2-instance-userdata"></a>
The user data script to make available to the instance\. User data is limited to 16 KB\. You must provide base64\-encoded text\. For more information, see [Fn::Base64](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-base64.html)\.  
User data runs only at instance launch\. For more information, see [Run commands on your Linux instance at launch](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html) and [Run commands on your Windows instance at launch](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/ec2-windows-user-data.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Volumes`  <a name="cfn-ec2-instance-volumes"></a>
The volumes to attach to the instance\.  
*Required*: No  
*Type*: List of [Volume](aws-properties-ec2-mount-point.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-ec2-instance-return-values"></a>

### Ref<a name="aws-properties-ec2-instance-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the instance ID\. For example: `i-1234567890abcdef0`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-ec2-instance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-ec2-instance-return-values-fn--getatt-fn--getatt"></a>

`AvailabilityZone`  <a name="AvailabilityZone-fn::getatt"></a>
The Availability Zone where the specified instance is launched\. For example: `us-east-1b`\.  
You can retrieve a list of all Availability Zones for a Region by using the [Fn::GetAZs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getavailabilityzones.html) intrinsic function\.

`PrivateDnsName`  <a name="PrivateDnsName-fn::getatt"></a>
The private DNS name of the specified instance\. For example: `ip-10-24-34-0.ec2.internal`\.

`PrivateIp`  <a name="PrivateIp-fn::getatt"></a>
The private IP address of the specified instance\. For example: `10.24.34.0`\.

`PublicDnsName`  <a name="PublicDnsName-fn::getatt"></a>
The public DNS name of the specified instance\. For example: `ec2-107-20-50-45.compute-1.amazonaws.com`\.

`PublicIp`  <a name="PublicIp-fn::getatt"></a>
The public IP address of the specified instance\. For example: `192.0.2.0`\.

## Examples<a name="aws-properties-ec2-instance--examples"></a>

### EC2 instance with an EBS block device mapping<a name="aws-properties-ec2-instance--examples--EC2_instance_with_an_EBS_block_device_mapping"></a>

The following example creates an EC2 instance with a block device mapping with an entry that specifies an io1 volume with a size of 20 GB and an entry that uses NoDevice to override a device specified in the AMI block device mapping\.

#### JSON<a name="aws-properties-ec2-instance--examples--EC2_instance_with_an_EBS_block_device_mapping--json"></a>

```
"MyEC2Instance" : {
   "Type" : "AWS::EC2::Instance",
   "Properties" : {
      "ImageId" : "ami-79fd7eee",
      "KeyName" : "testkey",
      "BlockDeviceMappings" : [
         {
            "DeviceName" : "/dev/sdm",
            "Ebs" : {
              "VolumeType" : "io1",
              "Iops" : "200",
              "DeleteOnTermination" : "false",
              "VolumeSize" : "20"
            }
          }, 
          {
            "DeviceName" : "/dev/sdk",
            "NoDevice" : {}
          }
      ]
   }
}
```

#### YAML<a name="aws-properties-ec2-instance--examples--EC2_instance_with_an_EBS_block_device_mapping--yaml"></a>

```
  MyEC2Instance: 
    Type: AWS::EC2::Instance
    Properties: 
      ImageId: "ami-79fd7eee"
      KeyName: "testkey"
      BlockDeviceMappings: 
      - DeviceName: "/dev/sdm"
        Ebs: 
          VolumeType: "io1"
          Iops: "200"
          DeleteOnTermination: "false"
          VolumeSize: "20"
      - DeviceName: "/dev/sdk"
        NoDevice: {}
```

### Automatically assign a public IP address<a name="aws-properties-ec2-instance--examples--Automatically_assign_a_public_IP_address"></a>

You can associate a public IP address with a network interface only if it is the primary network interface \(the device index is 0\) and if you are creating a new network interface, not attaching an existing network interface\.

#### JSON<a name="aws-properties-ec2-instance--examples--Automatically_assign_a_public_IP_address--json"></a>

```
"Ec2Instance" : {
  "Type" : "AWS::EC2::Instance",
  "Properties" : {
    "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]},
    "KeyName" : { "Ref" : "KeyName" },
    "NetworkInterfaces": [ {
      "AssociatePublicIpAddress": "true",
      "DeviceIndex": "0",
      "GroupSet": [{ "Ref" : "myVPCEC2SecurityGroup" }],
      "SubnetId": { "Ref" : "PublicSubnet" }
    } ]
  }
}
```

#### YAML<a name="aws-properties-ec2-instance--examples--Automatically_assign_a_public_IP_address--yaml"></a>

```
Ec2Instance: 
  Type: AWS::EC2::Instance
  Properties: 
    ImageId: 
      Fn::FindInMap: 
        - "RegionMap"
        - Ref: "AWS::Region"
        - "AMI"
    KeyName: 
      Ref: "KeyName"
    NetworkInterfaces: 
      - AssociatePublicIpAddress: "true"
        DeviceIndex: "0"
        GroupSet: 
          - Ref: "myVPCEC2SecurityGroup"
        SubnetId: 
          Ref: "PublicSubnet"
```

## See also<a name="aws-properties-ec2-instance--seealso"></a>
+  [ RunInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RunInstances.html) in the *Amazon EC2 API Reference* 
+  [ Amazon EC2 instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Instances.html) in the *Amazon EC2 User Guide* 
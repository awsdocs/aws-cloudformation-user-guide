# AWS::EC2::Instance<a name="aws-properties-ec2-instance"></a>

Specifies an EC2 instance\.

If an Elastic IP address is attached to your instance, AWS CloudFormation reattaches the Elastic IP address after it updates the instance\. For more information about updating stacks, see [ AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

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
      "[BlockDeviceMappings](#cfn-ec2-instance-blockdevicemappings)" : [ [BlockDeviceMapping](aws-properties-ec2-blockdev-mapping.md), ... ],
      "[CpuOptions](#cfn-ec2-instance-cpuoptions)" : [CpuOptions](aws-properties-ec2-instance-cpuoptions.md),
      "[CreditSpecification](#cfn-ec2-instance-creditspecification)" : [CreditSpecification](aws-properties-ec2-instance-creditspecification.md),
      "[DisableApiTermination](#cfn-ec2-instance-disableapitermination)" : Boolean,
      "[EbsOptimized](#cfn-ec2-instance-ebsoptimized)" : Boolean,
      "[ElasticGpuSpecifications](#cfn-ec2-instance-elasticgpuspecifications)" : [ [ElasticGpuSpecification](aws-properties-ec2-instance-elasticgpuspecification.md), ... ],
      "[ElasticInferenceAccelerators](#cfn-ec2-instance-elasticinferenceaccelerators)" : [ [ElasticInferenceAccelerator](aws-properties-ec2-instance-elasticinferenceaccelerator.md), ... ],
      "[HostId](#cfn-ec2-instance-hostid)" : String,
      "[IamInstanceProfile](#cfn-ec2-instance-iaminstanceprofile)" : String,
      "[ImageId](#cfn-ec2-instance-imageid)" : String,
      "[InstanceInitiatedShutdownBehavior](#cfn-ec2-instance-instanceinitiatedshutdownbehavior)" : String,
      "[InstanceType](#cfn-ec2-instance-instancetype)" : String,
      "[Ipv6AddressCount](#cfn-ec2-instance-ipv6addresscount)" : Integer,
      "[Ipv6Addresses](#cfn-ec2-instance-ipv6addresses)" : [ [InstanceIpv6Address](aws-properties-ec2-instance-instanceipv6address.md), ... ],
      "[KernelId](#cfn-ec2-instance-kernelid)" : String,
      "[KeyName](#cfn-ec2-instance-keyname)" : String,
      "[LaunchTemplate](#cfn-ec2-instance-launchtemplate)" : [LaunchTemplateSpecification](aws-properties-ec2-instance-launchtemplatespecification.md),
      "[LicenseSpecifications](#cfn-ec2-instance-licensespecifications)" : [ [LicenseSpecification](aws-properties-ec2-instance-licensespecification.md), ... ],
      "[Monitoring](#cfn-ec2-instance-monitoring)" : Boolean,
      "[NetworkInterfaces](#cfn-ec2-instance-networkinterfaces)" : [ [NetworkInterface](aws-properties-ec2-network-iface-embedded.md), ... ],
      "[PlacementGroupName](#cfn-ec2-instance-placementgroupname)" : String,
      "[PrivateIpAddress](#cfn-ec2-instance-privateipaddress)" : String,
      "[RamdiskId](#cfn-ec2-instance-ramdiskid)" : String,
      "[SecurityGroupIds](#cfn-ec2-instance-securitygroupids)" : [ String, ... ],
      "[SecurityGroups](#cfn-ec2-instance-securitygroups)" : [ String, ... ],
      "[SourceDestCheck](#cfn-ec2-instance-sourcedestcheck)" : Boolean,
      "[SsmAssociations](#cfn-ec2-instance-ssmassociations)" : [ [SsmAssociation](aws-properties-ec2-instance-ssmassociations.md), ... ],
      "[SubnetId](#cfn-ec2-instance-subnetid)" : String,
      "[Tags](#cfn-ec2-instance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Tenancy](#cfn-ec2-instance-tenancy)" : String,
      "[UserData](#cfn-ec2-instance-userdata)" : String,
      "[Volumes](#cfn-ec2-instance-volumes)" : [ [Volume](aws-properties-ec2-mount-point.md), ... ]
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
    - [BlockDeviceMapping](aws-properties-ec2-blockdev-mapping.md)
  [CpuOptions](#cfn-ec2-instance-cpuoptions): 
    [CpuOptions](aws-properties-ec2-instance-cpuoptions.md)
  [CreditSpecification](#cfn-ec2-instance-creditspecification): 
    [CreditSpecification](aws-properties-ec2-instance-creditspecification.md)
  [DisableApiTermination](#cfn-ec2-instance-disableapitermination): Boolean
  [EbsOptimized](#cfn-ec2-instance-ebsoptimized): Boolean
  [ElasticGpuSpecifications](#cfn-ec2-instance-elasticgpuspecifications): 
    - [ElasticGpuSpecification](aws-properties-ec2-instance-elasticgpuspecification.md)
  [ElasticInferenceAccelerators](#cfn-ec2-instance-elasticinferenceaccelerators): 
    - [ElasticInferenceAccelerator](aws-properties-ec2-instance-elasticinferenceaccelerator.md)
  [HostId](#cfn-ec2-instance-hostid): String
  [IamInstanceProfile](#cfn-ec2-instance-iaminstanceprofile): String
  [ImageId](#cfn-ec2-instance-imageid): String
  [InstanceInitiatedShutdownBehavior](#cfn-ec2-instance-instanceinitiatedshutdownbehavior): String
  [InstanceType](#cfn-ec2-instance-instancetype): String
  [Ipv6AddressCount](#cfn-ec2-instance-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-instance-ipv6addresses): 
    - [InstanceIpv6Address](aws-properties-ec2-instance-instanceipv6address.md)
  [KernelId](#cfn-ec2-instance-kernelid): String
  [KeyName](#cfn-ec2-instance-keyname): String
  [LaunchTemplate](#cfn-ec2-instance-launchtemplate): 
    [LaunchTemplateSpecification](aws-properties-ec2-instance-launchtemplatespecification.md)
  [LicenseSpecifications](#cfn-ec2-instance-licensespecifications): 
    - [LicenseSpecification](aws-properties-ec2-instance-licensespecification.md)
  [Monitoring](#cfn-ec2-instance-monitoring): Boolean
  [NetworkInterfaces](#cfn-ec2-instance-networkinterfaces): 
    - [NetworkInterface](aws-properties-ec2-network-iface-embedded.md)
  [PlacementGroupName](#cfn-ec2-instance-placementgroupname): String
  [PrivateIpAddress](#cfn-ec2-instance-privateipaddress): String
  [RamdiskId](#cfn-ec2-instance-ramdiskid): String
  [SecurityGroupIds](#cfn-ec2-instance-securitygroupids): 
    - String
  [SecurityGroups](#cfn-ec2-instance-securitygroups): 
    - String
  [SourceDestCheck](#cfn-ec2-instance-sourcedestcheck): Boolean
  [SsmAssociations](#cfn-ec2-instance-ssmassociations): 
    - [SsmAssociation](aws-properties-ec2-instance-ssmassociations.md)
  [SubnetId](#cfn-ec2-instance-subnetid): String
  [Tags](#cfn-ec2-instance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Tenancy](#cfn-ec2-instance-tenancy): String
  [UserData](#cfn-ec2-instance-userdata): String
  [Volumes](#cfn-ec2-instance-volumes): 
    - [Volume](aws-properties-ec2-mount-point.md)
```

## Properties<a name="aws-properties-ec2-instance-properties"></a>

`AdditionalInfo`  <a name="cfn-ec2-instance-additionalinfo"></a>
Reserved\.  
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
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BlockDeviceMappings`  <a name="cfn-ec2-instance-blockdevicemappings"></a>
The block device mapping entries that defines the block devices to attach to the instance at launch\.  
By default, the block devices specified in the block device mapping for the AMI are used\. You can override the AMI block device mapping using the instance block device mapping\. For the root volume, you can only override the volume size, volume type, and `DeleteOnTermination` setting\. After the instance is running, you can only modify the `DeleteOnTermination` settings of the attached EBS volumes\.  
*Required*: No  
*Type*: List of [BlockDeviceMapping](aws-properties-ec2-blockdev-mapping.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`CpuOptions`  <a name="cfn-ec2-instance-cpuoptions"></a>
The CPU options for the instance\.  
*Required*: No  
*Type*: [CpuOptions](aws-properties-ec2-instance-cpuoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CreditSpecification`  <a name="cfn-ec2-instance-creditspecification"></a>
The credit option for CPU usage of the T2 or T3 instance\. Valid values are `standard` and `unlimited`\. To change this attribute after launch, use [ ModifyInstanceCreditSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyInstanceCreditSpecification.html)\. For more information, see [Burstable Performance Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/burstable-performance-instances.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Default: `standard` \(T2 instances\) or `unlimited` \(T3 instances\)  
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
An elastic GPU to associate with the instance\. An Elastic GPU is a GPU resource that you can attach to your Windows instance to accelerate the graphics performance of your applications\. For more information, see [ Amazon EC2 Elastic GPUs](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/elastic-graphics.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: List of [ElasticGpuSpecification](aws-properties-ec2-instance-elasticgpuspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ElasticInferenceAccelerators`  <a name="cfn-ec2-instance-elasticinferenceaccelerators"></a>
An elastic inference accelerator to associate with the instance\. Elastic inference accelerators are a resource you can attach to your Amazon EC2 instances to accelerate your Deep Learning \(DL\) inference workloads\.  
*Required*: No  
*Type*: List of [ElasticInferenceAccelerator](aws-properties-ec2-instance-elasticinferenceaccelerator.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostId`  <a name="cfn-ec2-instance-hostid"></a>
If you specify host for the `Affinity` property, the ID of a dedicated host that the instance is associated with\. If you don't specify an ID, Amazon EC2 launches the instance onto any available, compatible dedicated host in your account\. This type of launch is called an untargeted launch\. Note that for untargeted launches, you must have a compatible, dedicated host available to successfully launch instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`IamInstanceProfile`  <a name="cfn-ec2-instance-iaminstanceprofile"></a>
The IAM instance profile\.  
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
*Allowed Values*: `stop | terminate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-ec2-instance-instancetype"></a>
The instance type\. For more information, see [Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Default: `m1.small`   
*Required*: No  
*Type*: String  
*Allowed Values*: `a1.2xlarge | a1.4xlarge | a1.large | a1.medium | a1.xlarge | c1.medium | c1.xlarge | c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.12xlarge | c5.18xlarge | c5.24xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.metal | c5.xlarge | c5d.18xlarge | c5d.2xlarge | c5d.4xlarge | c5d.9xlarge | c5d.large | c5d.xlarge | c5n.18xlarge | c5n.2xlarge | c5n.4xlarge | c5n.9xlarge | c5n.large | c5n.xlarge | cc1.4xlarge | cc2.8xlarge | cg1.4xlarge | cr1.8xlarge | d2.2xlarge | d2.4xlarge | d2.8xlarge | d2.xlarge | f1.16xlarge | f1.2xlarge | f1.4xlarge | g2.2xlarge | g2.8xlarge | g3.16xlarge | g3.4xlarge | g3.8xlarge | g3s.xlarge | h1.16xlarge | h1.2xlarge | h1.4xlarge | h1.8xlarge | hi1.4xlarge | hs1.8xlarge | i2.2xlarge | i2.4xlarge | i2.8xlarge | i2.xlarge | i3.16xlarge | i3.2xlarge | i3.4xlarge | i3.8xlarge | i3.large | i3.metal | i3.xlarge | i3en.12xlarge | i3en.24xlarge | i3en.2xlarge | i3en.3xlarge | i3en.6xlarge | i3en.large | i3en.metal | i3en.xlarge | m1.large | m1.medium | m1.small | m1.xlarge | m2.2xlarge | m2.4xlarge | m2.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.16xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.16xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.8xlarge | m5.large | m5.metal | m5.xlarge | m5a.12xlarge | m5a.16xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.8xlarge | m5a.large | m5a.xlarge | m5ad.12xlarge | m5ad.16xlarge | m5ad.24xlarge | m5ad.2xlarge | m5ad.4xlarge | m5ad.8xlarge | m5ad.large | m5ad.xlarge | m5d.12xlarge | m5d.16xlarge | m5d.24xlarge | m5d.2xlarge | m5d.4xlarge | m5d.8xlarge | m5d.large | m5d.metal | m5d.xlarge | p2.16xlarge | p2.8xlarge | p2.xlarge | p3.16xlarge | p3.2xlarge | p3.8xlarge | p3dn.24xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.16xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.8xlarge | r5.large | r5.metal | r5.xlarge | r5a.12xlarge | r5a.16xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.8xlarge | r5a.large | r5a.xlarge | r5ad.12xlarge | r5ad.16xlarge | r5ad.24xlarge | r5ad.2xlarge | r5ad.4xlarge | r5ad.8xlarge | r5ad.large | r5ad.xlarge | r5d.12xlarge | r5d.16xlarge | r5d.24xlarge | r5d.2xlarge | r5d.4xlarge | r5d.8xlarge | r5d.large | r5d.metal | r5d.xlarge | t1.micro | t2.2xlarge | t2.large | t2.medium | t2.micro | t2.nano | t2.small | t2.xlarge | t3.2xlarge | t3.large | t3.medium | t3.micro | t3.nano | t3.small | t3.xlarge | t3a.2xlarge | t3a.large | t3a.medium | t3a.micro | t3a.nano | t3a.small | t3a.xlarge | u-12tb1.metal | u-6tb1.metal | u-9tb1.metal | x1.16xlarge | x1.32xlarge | x1e.16xlarge | x1e.2xlarge | x1e.32xlarge | x1e.4xlarge | x1e.8xlarge | x1e.xlarge | z1d.12xlarge | z1d.2xlarge | z1d.3xlarge | z1d.6xlarge | z1d.large | z1d.metal | z1d.xlarge`  
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
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [ PV\-GRUB](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon Elastic Compute Cloud User Guide*\.
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
Specifies whether detailed monitoring is enabled for the instance\.  
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
The name of an existing placement group that you want to launch the instance into \(for cluster instances\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrivateIpAddress`  <a name="cfn-ec2-instance-privateipaddress"></a>
\[EC2\-VPC\] The primary IPv4 address\. You must specify a value from the IPv4 address range of the subnet\.  
Only one private IP address can be designated as primary\. You can't specify this option if you've specified the option to designate a private IP address as the primary IP address in a network interface specification\. You cannot specify this option if you're launching more than one instance in the request\.  
You cannot specify this option and the network interfaces option in the same request\.  
If you make an update to an instance that requires replacement, you must assign a new private IP address\. During a replacement, AWS CloudFormation creates a new instance but doesn't delete the old instance until the stack has successfully updated\. If the stack update fails, AWS CloudFormation uses the old instance in order to roll back the stack to the previous working state\. The old and new instances cannot have the same private IP address\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RamdiskId`  <a name="cfn-ec2-instance-ramdiskid"></a>
The ID of the RAM disk to select\. Some kernels require additional drivers at launch\. Check the kernel requirements for information about whether you need to specify a RAM disk\. To find kernel requirements, go to the AWS Resource Center and search for the kernel ID\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [ PV\-GRUB](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedkernels.html) in the *Amazon Elastic Compute Cloud User Guide*\.
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
Specifies whether to enable an instance launched in a VPC to perform NAT\. This controls whether source/destination checking is enabled on the instance\. A value of `true` means that checking is enabled, and `false` means that checking is disabled\. The value must be `false` for the instance to perform NAT\. For more information, see [NAT Instances](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_NAT_Instance.html) in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SsmAssociations`  <a name="cfn-ec2-instance-ssmassociations"></a>
The SSM [ document](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-document.html) and parameter values in AWS Systems Manager to associate with this instance\. To use this property, you must specify an IAM instance profile role for the instance\. For more information, see [ Create an Instance Profile for Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-configuring-access-role.html) in the *AWS Systems Manager User Guide*\.  
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
The tags to apply to the resources during launch\. You can only tag instances and volumes on launch\. The specified tags are applied to all instances or volumes that are created during launch\. To tag a resource after it has been created, see [CreateTags](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tenancy`  <a name="cfn-ec2-instance-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of `dedicated` runs on single\-tenant hardware\.   
*Required*: No  
*Type*: String  
*Allowed Values*: `dedicated | default | host`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`UserData`  <a name="cfn-ec2-instance-userdata"></a>
The user data to make available to the instance\. For more information, see [Running Commands on Your Linux Instance at Launch](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html) \(Linux\) and [Adding User Data](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/ec2-instance-metadata.html#instancedata-add-user-data) \(Windows\)\. If you are using a command line tool, base64\-encoding is performed for you, and you can load the text from a file\. Otherwise, you must provide base64\-encoded text\. User data is limited to 16 KB\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Volumes`  <a name="cfn-ec2-instance-volumes"></a>
The volumes to attach to the instance\.  
*Required*: No  
*Type*: List of [Volume](aws-properties-ec2-mount-point.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-properties-ec2-instance-return-values"></a>

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

### EC2 Instance with an EBS Block Device Mapping<a name="aws-properties-ec2-instance--examples--EC2_Instance_with_an_EBS_Block_Device_Mapping"></a>

#### JSON<a name="aws-properties-ec2-instance--examples--EC2_Instance_with_an_EBS_Block_Device_Mapping--json"></a>

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

#### YAML<a name="aws-properties-ec2-instance--examples--EC2_Instance_with_an_EBS_Block_Device_Mapping--yaml"></a>

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

### Automatically Assign a Public IP Address<a name="aws-properties-ec2-instance--examples--Automatically_Assign_a_Public_IP_Address"></a>

You can associate a public IP address with a network interface only if it has a device index of `0` and if it is a new network interface \(not an existing one\)\.

#### JSON<a name="aws-properties-ec2-instance--examples--Automatically_Assign_a_Public_IP_Address--json"></a>

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

#### YAML<a name="aws-properties-ec2-instance--examples--Automatically_Assign_a_Public_IP_Address--yaml"></a>

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

## See Also<a name="aws-properties-ec2-instance--seealso"></a>
+  [ RunInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RunInstances.html) in the *Amazon EC2 API Reference* 
+  [ EBS\-Optimized Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#EBSOptimized) in the *Amazon EC2 API Reference* 
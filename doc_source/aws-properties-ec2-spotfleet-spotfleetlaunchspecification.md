# AWS::EC2::SpotFleet SpotFleetLaunchSpecification<a name="aws-properties-ec2-spotfleet-spotfleetlaunchspecification"></a>

Specifies the launch specification for one or more Spot Instances\. If you include On\-Demand capacity in your fleet request, you can't use `SpotFleetLaunchSpecification`; you must use [ LaunchTemplateConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-launchtemplateconfig.html)\. 

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleetlaunchspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetlaunchspecification-syntax.json"></a>

```
{
  "[BlockDeviceMappings](#cfn-ec2-spotfleet-spotfleetlaunchspecification-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
  "[EbsOptimized](#cfn-ec2-spotfleet-spotfleetlaunchspecification-ebsoptimized)" : Boolean,
  "[IamInstanceProfile](#cfn-ec2-spotfleet-spotfleetlaunchspecification-iaminstanceprofile)" : IamInstanceProfileSpecification,
  "[ImageId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-imageid)" : String,
  "[InstanceRequirements](#cfn-ec2-spotfleet-spotfleetlaunchspecification-instancerequirements)" : InstanceRequirementsRequest,
  "[InstanceType](#cfn-ec2-spotfleet-spotfleetlaunchspecification-instancetype)" : String,
  "[KernelId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-kernelid)" : String,
  "[KeyName](#cfn-ec2-spotfleet-spotfleetlaunchspecification-keyname)" : String,
  "[Monitoring](#cfn-ec2-spotfleet-spotfleetlaunchspecification-monitoring)" : SpotFleetMonitoring,
  "[NetworkInterfaces](#cfn-ec2-spotfleet-spotfleetlaunchspecification-networkinterfaces)" : [ InstanceNetworkInterfaceSpecification, ... ],
  "[Placement](#cfn-ec2-spotfleet-spotfleetlaunchspecification-placement)" : SpotPlacement,
  "[RamdiskId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-ramdiskid)" : String,
  "[SecurityGroups](#cfn-ec2-spotfleet-spotfleetlaunchspecification-securitygroups)" : [ GroupIdentifier, ... ],
  "[SpotPrice](#cfn-ec2-spotfleet-spotfleetlaunchspecification-spotprice)" : String,
  "[SubnetId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-subnetid)" : String,
  "[TagSpecifications](#cfn-ec2-spotfleet-spotfleetlaunchspecification-tagspecifications)" : [ SpotFleetTagSpecification, ... ],
  "[UserData](#cfn-ec2-spotfleet-spotfleetlaunchspecification-userdata)" : String,
  "[WeightedCapacity](#cfn-ec2-spotfleet-spotfleetlaunchspecification-weightedcapacity)" : Double
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetlaunchspecification-syntax.yaml"></a>

```
  [BlockDeviceMappings](#cfn-ec2-spotfleet-spotfleetlaunchspecification-blockdevicemappings): 
    - BlockDeviceMapping
  [EbsOptimized](#cfn-ec2-spotfleet-spotfleetlaunchspecification-ebsoptimized): Boolean
  [IamInstanceProfile](#cfn-ec2-spotfleet-spotfleetlaunchspecification-iaminstanceprofile): 
    IamInstanceProfileSpecification
  [ImageId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-imageid): String
  [InstanceRequirements](#cfn-ec2-spotfleet-spotfleetlaunchspecification-instancerequirements): 
    InstanceRequirementsRequest
  [InstanceType](#cfn-ec2-spotfleet-spotfleetlaunchspecification-instancetype): String
  [KernelId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-kernelid): String
  [KeyName](#cfn-ec2-spotfleet-spotfleetlaunchspecification-keyname): String
  [Monitoring](#cfn-ec2-spotfleet-spotfleetlaunchspecification-monitoring): 
    SpotFleetMonitoring
  [NetworkInterfaces](#cfn-ec2-spotfleet-spotfleetlaunchspecification-networkinterfaces): 
    - InstanceNetworkInterfaceSpecification
  [Placement](#cfn-ec2-spotfleet-spotfleetlaunchspecification-placement): 
    SpotPlacement
  [RamdiskId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-ramdiskid): String
  [SecurityGroups](#cfn-ec2-spotfleet-spotfleetlaunchspecification-securitygroups): 
    - GroupIdentifier
  [SpotPrice](#cfn-ec2-spotfleet-spotfleetlaunchspecification-spotprice): String
  [SubnetId](#cfn-ec2-spotfleet-spotfleetlaunchspecification-subnetid): String
  [TagSpecifications](#cfn-ec2-spotfleet-spotfleetlaunchspecification-tagspecifications): 
    - SpotFleetTagSpecification
  [UserData](#cfn-ec2-spotfleet-spotfleetlaunchspecification-userdata): String
  [WeightedCapacity](#cfn-ec2-spotfleet-spotfleetlaunchspecification-weightedcapacity): Double
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleetlaunchspecification-properties"></a>

`BlockDeviceMappings`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-blockdevicemappings"></a>
One or more block devices that are mapped to the Spot Instances\. You can't specify both a snapshot ID and an encryption value\. This is because only blank volumes can be encrypted on creation\. If a snapshot is the basis for a volume, it is not blank and its encryption status is used for the volume encryption status\.  
*Required*: No  
*Type*: List of [BlockDeviceMapping](aws-properties-ec2-spotfleet-blockdevicemapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsOptimized`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-ebsoptimized"></a>
Indicates whether the instances are optimized for EBS I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal EBS I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when using an EBS Optimized instance\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamInstanceProfile`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-iaminstanceprofile"></a>
The IAM instance profile\.  
*Required*: No  
*Type*: [IamInstanceProfileSpecification](aws-properties-ec2-spotfleet-iaminstanceprofilespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageId`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-imageid"></a>
The ID of the AMI\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceRequirements`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-instancerequirements"></a>
The attributes for the instance types\. When you specify instance attributes, Amazon EC2 will identify instance types with those attributes\.  
If you specify `InstanceRequirements`, you can't specify `InstanceType`\.
*Required*: No  
*Type*: [InstanceRequirementsRequest](aws-properties-ec2-spotfleet-instancerequirementsrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-instancetype"></a>
The instance type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `a1.2xlarge | a1.4xlarge | a1.large | a1.medium | a1.metal | a1.xlarge | c1.medium | c1.xlarge | c3.2xlarge | c3.4xlarge | c3.8xlarge | c3.large | c3.xlarge | c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.12xlarge | c5.18xlarge | c5.24xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.metal | c5.xlarge | c5a.12xlarge | c5a.16xlarge | c5a.24xlarge | c5a.2xlarge | c5a.4xlarge | c5a.8xlarge | c5a.large | c5a.xlarge | c5ad.12xlarge | c5ad.16xlarge | c5ad.24xlarge | c5ad.2xlarge | c5ad.4xlarge | c5ad.8xlarge | c5ad.large | c5ad.xlarge | c5d.12xlarge | c5d.18xlarge | c5d.24xlarge | c5d.2xlarge | c5d.4xlarge | c5d.9xlarge | c5d.large | c5d.metal | c5d.xlarge | c5n.18xlarge | c5n.2xlarge | c5n.4xlarge | c5n.9xlarge | c5n.large | c5n.metal | c5n.xlarge | c6a.12xlarge | c6a.16xlarge | c6a.24xlarge | c6a.2xlarge | c6a.32xlarge | c6a.48xlarge | c6a.4xlarge | c6a.8xlarge | c6a.large | c6a.metal | c6a.xlarge | c6g.12xlarge | c6g.16xlarge | c6g.2xlarge | c6g.4xlarge | c6g.8xlarge | c6g.large | c6g.medium | c6g.metal | c6g.xlarge | c6gd.12xlarge | c6gd.16xlarge | c6gd.2xlarge | c6gd.4xlarge | c6gd.8xlarge | c6gd.large | c6gd.medium | c6gd.metal | c6gd.xlarge | c6gn.12xlarge | c6gn.16xlarge | c6gn.2xlarge | c6gn.4xlarge | c6gn.8xlarge | c6gn.large | c6gn.medium | c6gn.xlarge | c6i.12xlarge | c6i.16xlarge | c6i.24xlarge | c6i.2xlarge | c6i.32xlarge | c6i.4xlarge | c6i.8xlarge | c6i.large | c6i.metal | c6i.xlarge | c6id.12xlarge | c6id.16xlarge | c6id.24xlarge | c6id.2xlarge | c6id.32xlarge | c6id.4xlarge | c6id.8xlarge | c6id.large | c6id.metal | c6id.xlarge | c6in.12xlarge | c6in.16xlarge | c6in.24xlarge | c6in.2xlarge | c6in.32xlarge | c6in.4xlarge | c6in.8xlarge | c6in.large | c6in.xlarge | c7g.12xlarge | c7g.16xlarge | c7g.2xlarge | c7g.4xlarge | c7g.8xlarge | c7g.large | c7g.medium | c7g.xlarge | cc1.4xlarge | cc2.8xlarge | cg1.4xlarge | cr1.8xlarge | d2.2xlarge | d2.4xlarge | d2.8xlarge | d2.xlarge | d3.2xlarge | d3.4xlarge | d3.8xlarge | d3.xlarge | d3en.12xlarge | d3en.2xlarge | d3en.4xlarge | d3en.6xlarge | d3en.8xlarge | d3en.xlarge | dl1.24xlarge | f1.16xlarge | f1.2xlarge | f1.4xlarge | g2.2xlarge | g2.8xlarge | g3.16xlarge | g3.4xlarge | g3.8xlarge | g3s.xlarge | g4ad.16xlarge | g4ad.2xlarge | g4ad.4xlarge | g4ad.8xlarge | g4ad.xlarge | g4dn.12xlarge | g4dn.16xlarge | g4dn.2xlarge | g4dn.4xlarge | g4dn.8xlarge | g4dn.metal | g4dn.xlarge | g5.12xlarge | g5.16xlarge | g5.24xlarge | g5.2xlarge | g5.48xlarge | g5.4xlarge | g5.8xlarge | g5.xlarge | g5g.16xlarge | g5g.2xlarge | g5g.4xlarge | g5g.8xlarge | g5g.metal | g5g.xlarge | h1.16xlarge | h1.2xlarge | h1.4xlarge | h1.8xlarge | hi1.4xlarge | hpc6a.48xlarge | hpc6id.32xlarge | hs1.8xlarge | i2.2xlarge | i2.4xlarge | i2.8xlarge | i2.xlarge | i3.16xlarge | i3.2xlarge | i3.4xlarge | i3.8xlarge | i3.large | i3.metal | i3.xlarge | i3en.12xlarge | i3en.24xlarge | i3en.2xlarge | i3en.3xlarge | i3en.6xlarge | i3en.large | i3en.metal | i3en.xlarge | i4i.16xlarge | i4i.2xlarge | i4i.32xlarge | i4i.4xlarge | i4i.8xlarge | i4i.large | i4i.metal | i4i.xlarge | im4gn.16xlarge | im4gn.2xlarge | im4gn.4xlarge | im4gn.8xlarge | im4gn.large | im4gn.xlarge | inf1.24xlarge | inf1.2xlarge | inf1.6xlarge | inf1.xlarge | is4gen.2xlarge | is4gen.4xlarge | is4gen.8xlarge | is4gen.large | is4gen.medium | is4gen.xlarge | m1.large | m1.medium | m1.small | m1.xlarge | m2.2xlarge | m2.4xlarge | m2.xlarge | m3.2xlarge | m3.large | m3.medium | m3.xlarge | m4.10xlarge | m4.16xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.16xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.8xlarge | m5.large | m5.metal | m5.xlarge | m5a.12xlarge | m5a.16xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.8xlarge | m5a.large | m5a.xlarge | m5ad.12xlarge | m5ad.16xlarge | m5ad.24xlarge | m5ad.2xlarge | m5ad.4xlarge | m5ad.8xlarge | m5ad.large | m5ad.xlarge | m5d.12xlarge | m5d.16xlarge | m5d.24xlarge | m5d.2xlarge | m5d.4xlarge | m5d.8xlarge | m5d.large | m5d.metal | m5d.xlarge | m5dn.12xlarge | m5dn.16xlarge | m5dn.24xlarge | m5dn.2xlarge | m5dn.4xlarge | m5dn.8xlarge | m5dn.large | m5dn.metal | m5dn.xlarge | m5n.12xlarge | m5n.16xlarge | m5n.24xlarge | m5n.2xlarge | m5n.4xlarge | m5n.8xlarge | m5n.large | m5n.metal | m5n.xlarge | m5zn.12xlarge | m5zn.2xlarge | m5zn.3xlarge | m5zn.6xlarge | m5zn.large | m5zn.metal | m5zn.xlarge | m6a.12xlarge | m6a.16xlarge | m6a.24xlarge | m6a.2xlarge | m6a.32xlarge | m6a.48xlarge | m6a.4xlarge | m6a.8xlarge | m6a.large | m6a.metal | m6a.xlarge | m6g.12xlarge | m6g.16xlarge | m6g.2xlarge | m6g.4xlarge | m6g.8xlarge | m6g.large | m6g.medium | m6g.metal | m6g.xlarge | m6gd.12xlarge | m6gd.16xlarge | m6gd.2xlarge | m6gd.4xlarge | m6gd.8xlarge | m6gd.large | m6gd.medium | m6gd.metal | m6gd.xlarge | m6i.12xlarge | m6i.16xlarge | m6i.24xlarge | m6i.2xlarge | m6i.32xlarge | m6i.4xlarge | m6i.8xlarge | m6i.large | m6i.metal | m6i.xlarge | m6id.12xlarge | m6id.16xlarge | m6id.24xlarge | m6id.2xlarge | m6id.32xlarge | m6id.4xlarge | m6id.8xlarge | m6id.large | m6id.metal | m6id.xlarge | m6idn.12xlarge | m6idn.16xlarge | m6idn.24xlarge | m6idn.2xlarge | m6idn.32xlarge | m6idn.4xlarge | m6idn.8xlarge | m6idn.large | m6idn.xlarge | m6in.12xlarge | m6in.16xlarge | m6in.24xlarge | m6in.2xlarge | m6in.32xlarge | m6in.4xlarge | m6in.8xlarge | m6in.large | m6in.xlarge | mac1.metal | mac2.metal | p2.16xlarge | p2.8xlarge | p2.xlarge | p3.16xlarge | p3.2xlarge | p3.8xlarge | p3dn.24xlarge | p4d.24xlarge | p4de.24xlarge | r3.2xlarge | r3.4xlarge | r3.8xlarge | r3.large | r3.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.16xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.8xlarge | r5.large | r5.metal | r5.xlarge | r5a.12xlarge | r5a.16xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.8xlarge | r5a.large | r5a.xlarge | r5ad.12xlarge | r5ad.16xlarge | r5ad.24xlarge | r5ad.2xlarge | r5ad.4xlarge | r5ad.8xlarge | r5ad.large | r5ad.xlarge | r5b.12xlarge | r5b.16xlarge | r5b.24xlarge | r5b.2xlarge | r5b.4xlarge | r5b.8xlarge | r5b.large | r5b.metal | r5b.xlarge | r5d.12xlarge | r5d.16xlarge | r5d.24xlarge | r5d.2xlarge | r5d.4xlarge | r5d.8xlarge | r5d.large | r5d.metal | r5d.xlarge | r5dn.12xlarge | r5dn.16xlarge | r5dn.24xlarge | r5dn.2xlarge | r5dn.4xlarge | r5dn.8xlarge | r5dn.large | r5dn.metal | r5dn.xlarge | r5n.12xlarge | r5n.16xlarge | r5n.24xlarge | r5n.2xlarge | r5n.4xlarge | r5n.8xlarge | r5n.large | r5n.metal | r5n.xlarge | r6a.12xlarge | r6a.16xlarge | r6a.24xlarge | r6a.2xlarge | r6a.32xlarge | r6a.48xlarge | r6a.4xlarge | r6a.8xlarge | r6a.large | r6a.metal | r6a.xlarge | r6g.12xlarge | r6g.16xlarge | r6g.2xlarge | r6g.4xlarge | r6g.8xlarge | r6g.large | r6g.medium | r6g.metal | r6g.xlarge | r6gd.12xlarge | r6gd.16xlarge | r6gd.2xlarge | r6gd.4xlarge | r6gd.8xlarge | r6gd.large | r6gd.medium | r6gd.metal | r6gd.xlarge | r6i.12xlarge | r6i.16xlarge | r6i.24xlarge | r6i.2xlarge | r6i.32xlarge | r6i.4xlarge | r6i.8xlarge | r6i.large | r6i.metal | r6i.xlarge | r6id.12xlarge | r6id.16xlarge | r6id.24xlarge | r6id.2xlarge | r6id.32xlarge | r6id.4xlarge | r6id.8xlarge | r6id.large | r6id.metal | r6id.xlarge | r6idn.12xlarge | r6idn.16xlarge | r6idn.24xlarge | r6idn.2xlarge | r6idn.32xlarge | r6idn.4xlarge | r6idn.8xlarge | r6idn.large | r6idn.xlarge | r6in.12xlarge | r6in.16xlarge | r6in.24xlarge | r6in.2xlarge | r6in.32xlarge | r6in.4xlarge | r6in.8xlarge | r6in.large | r6in.xlarge | t1.micro | t2.2xlarge | t2.large | t2.medium | t2.micro | t2.nano | t2.small | t2.xlarge | t3.2xlarge | t3.large | t3.medium | t3.micro | t3.nano | t3.small | t3.xlarge | t3a.2xlarge | t3a.large | t3a.medium | t3a.micro | t3a.nano | t3a.small | t3a.xlarge | t4g.2xlarge | t4g.large | t4g.medium | t4g.micro | t4g.nano | t4g.small | t4g.xlarge | trn1.2xlarge | trn1.32xlarge | u-12tb1.112xlarge | u-12tb1.metal | u-18tb1.112xlarge | u-18tb1.metal | u-24tb1.112xlarge | u-24tb1.metal | u-3tb1.56xlarge | u-6tb1.112xlarge | u-6tb1.56xlarge | u-6tb1.metal | u-9tb1.112xlarge | u-9tb1.metal | vt1.24xlarge | vt1.3xlarge | vt1.6xlarge | x1.16xlarge | x1.32xlarge | x1e.16xlarge | x1e.2xlarge | x1e.32xlarge | x1e.4xlarge | x1e.8xlarge | x1e.xlarge | x2gd.12xlarge | x2gd.16xlarge | x2gd.2xlarge | x2gd.4xlarge | x2gd.8xlarge | x2gd.large | x2gd.medium | x2gd.metal | x2gd.xlarge | x2idn.16xlarge | x2idn.24xlarge | x2idn.32xlarge | x2idn.metal | x2iedn.16xlarge | x2iedn.24xlarge | x2iedn.2xlarge | x2iedn.32xlarge | x2iedn.4xlarge | x2iedn.8xlarge | x2iedn.metal | x2iedn.xlarge | x2iezn.12xlarge | x2iezn.2xlarge | x2iezn.4xlarge | x2iezn.6xlarge | x2iezn.8xlarge | x2iezn.metal | z1d.12xlarge | z1d.2xlarge | z1d.3xlarge | z1d.6xlarge | z1d.large | z1d.metal | z1d.xlarge`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KernelId`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-kernelid"></a>
The ID of the kernel\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyName`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-keyname"></a>
The name of the key pair\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Monitoring`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-monitoring"></a>
Enable or disable monitoring for the instances\.  
*Required*: No  
*Type*: [SpotFleetMonitoring](aws-properties-ec2-spotfleet-spotfleetmonitoring.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInterfaces`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-networkinterfaces"></a>
One or more network interfaces\. If you specify a network interface, you must specify subnet IDs and security group IDs using the network interface\.  
 `SpotFleetLaunchSpecification` currently does not support Elastic Fabric Adapter \(EFA\)\. To specify an EFA, you must use [LaunchTemplateConfig](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateConfig.html)\.
*Required*: No  
*Type*: List of [InstanceNetworkInterfaceSpecification](aws-properties-ec2-spotfleet-instancenetworkinterfacespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Placement`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-placement"></a>
The placement information\.  
*Required*: No  
*Type*: [SpotPlacement](aws-properties-ec2-spotfleet-spotplacement.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RamdiskId`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-ramdiskid"></a>
The ID of the RAM disk\. Some kernels require additional drivers at launch\. Check the kernel requirements for information about whether you need to specify a RAM disk\. To find kernel requirements, refer to the AWS Resource Center and search for the kernel ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-securitygroups"></a>
One or more security groups\. When requesting instances in a VPC, you must specify the IDs of the security groups\. When requesting instances in EC2\-Classic, you can specify the names or the IDs of the security groups\.  
*Required*: No  
*Type*: List of [GroupIdentifier](aws-properties-ec2-spotfleet-groupidentifier.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpotPrice`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-spotprice"></a>
The maximum price per unit hour that you are willing to pay for a Spot Instance\. We do not recommend using this parameter because it can lead to increased interruptions\. If you do not specify this parameter, you will pay the current Spot price\.  
If you specify a maximum price, your instances will be interrupted more frequently than if you do not specify this parameter\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-subnetid"></a>
The IDs of the subnets in which to launch the instances\. To specify multiple subnets, separate them using commas; for example, "subnet\-1234abcdeexample1, subnet\-0987cdef6example2"\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagSpecifications`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-tagspecifications"></a>
The tags to apply during creation\.  
*Required*: No  
*Type*: List of [SpotFleetTagSpecification](aws-properties-ec2-spotfleet-spotfleettagspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserData`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-userdata"></a>
The base64\-encoded user data that instances use when starting up\. User data is limited to 16 KB\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WeightedCapacity`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-weightedcapacity"></a>
The number of units provided by the specified instance type\. These are the same units that you chose to set the target capacity in terms of instances, or a performance characteristic such as vCPUs, memory, or I/O\.  
If the target capacity divided by this value is not a whole number, Amazon EC2 rounds the number of instances to the next whole number\. If this value is not specified, the default is 1\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
# Amazon Elastic Compute Cloud SpotFleet LaunchSpecifications<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications"></a>

`LaunchSpecifications` is a property of the [Amazon EC2 SpotFleet SpotFleetRequestConfigData](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata.md) property that defines the launch specifications for the Spot fleet request\.

## Syntax<a name="w3ab2c21c14d773b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-syntax.json"></a>

```
{
  "[BlockDeviceMappings](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
  "[EbsOptimized](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ebsoptimized)" : Boolean,
  "[IamInstanceProfile](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile)" : IamInstanceProfile,
  "[ImageId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-imageid)" : String,
  "[InstanceType](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-instancetype)" : String,
  "[KernelId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-kernelid)" : String,
  "[KeyName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-keyname)" : String,
  "[Monitoring](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring)" : Boolean,
  "[NetworkInterfaces](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces)" : [ NetworkInterface, ... ],
  "[Placement](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement)" : Placement,
  "[RamdiskId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ramdiskid)" : String,
  "[SecurityGroups](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups)" : [ SecurityGroup, ... ],
  "[SpotPrice](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-spotprice)" : String,
  "[SubnetId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-subnetid)" : String,
  "[TagSpecifications](#cfn-ec2-spotfleet-spotfleetlaunchspecification-tagspecifications)" : SpotFleetTagSpecification,     
  "[UserData](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-userdata)" : String,
  "[WeightedCapacity](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-weightedcapacity)" : Number
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-syntax.yaml"></a>

```
[BlockDeviceMappings](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings):
  - BlockDeviceMapping
[EbsOptimized](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ebsoptimized): Boolean
[IamInstanceProfile](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile):
  IamInstanceProfile
[ImageId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-imageid): String
[InstanceType](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-instancetype): String
[KernelId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-kernelid): String
[KeyName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-keyname): String
[Monitoring](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring): Boolean
[NetworkInterfaces](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces):
  - NetworkInterface
[Placement](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement):
  Placement
[RamdiskId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ramdiskid): String
[SecurityGroups](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups):
  - SecurityGroup
[SpotPrice](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-spotprice): String
[SubnetId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-subnetid): String
[TagSpecifications](#cfn-ec2-spotfleet-spotfleetlaunchspecification-tagspecifications): 
  - SpotFleetTagSpecification
[UserData](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-userdata): String
[WeightedCapacity](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-weightedcapacity): Number
```

## Properties<a name="w3ab2c21c14d773b7"></a>

`BlockDeviceMappings`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings"></a>
Defines the block devices that are mapped to the Spot instances\.  
*Required*: No  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet BlockDeviceMappings](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings.md)

`EbsOptimized`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ebsoptimized"></a>
Indicates whether the instances are optimized for Amazon Elastic Block Store \(Amazon EBS\) I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal EBS I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when you use an Amazon EBS\-optimized instance\.  
*Required*: No  
*Type*: Boolean

`IamInstanceProfile`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile"></a>
Defines the AWS Identity and Access Management \(IAM\) instance profile to associate with the instances\.  
*Required*: No  
*Type*: [Amazon Elastic Compute Cloud SpotFleet IamInstanceProfile](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile.md)

`ImageId`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-imageid"></a>
The unique ID of the Amazon Machine Image \(AMI\) to launch on the instances\.  
*Required*: Yes  
*Type*: String

`InstanceType`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-instancetype"></a>
Specifies the instance type of the EC2 instances\.  
*Required*: Yes  
*Type*: String

`KernelId`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-kernelid"></a>
The ID of the kernel that is associated with the Amazon Elastic Compute Cloud \(Amazon EC2\) AMI\.  
*Required*: No  
*Type*: String

`KeyName`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-keyname"></a>
An Amazon EC2 key pair to associate with the instances\.  
*Required*: No  
*Type*: String

`Monitoring`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring"></a>
Enable or disable monitoring for the instances\.  
*Required*: No  
*Type*: [Amazon EC2 SpotFleet Monitoring](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring.md)

`NetworkInterfaces`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces"></a>
The network interfaces to associate with the instances\.  
*Required*: No  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet NetworkInterfaces](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces.md)

`Placement`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement"></a>
Defines a placement group, which is a logical grouping of instances within a single Availability Zone \(AZ\)\.  
*Required*: No  
*Type*: [Amazon Elastic Compute Cloud SpotFleet Placement](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement.md)

`RamdiskId`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ramdiskid"></a>
The ID of the RAM disk to select\. Some kernels require additional drivers at launch\. Check the kernel requirements for information about whether you need to specify a RAM disk\. To find kernel requirements, refer to the AWS Resource Center and search for the kernel ID\.  
*Required*: No  
*Type*: String

`SecurityGroups`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups"></a>
One or more security group IDs to associate with the instances\.  
*Required*: No  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet SecurityGroups](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups.md)

`SpotPrice`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-spotprice"></a>
The bid price per unit hour for the specified instance type\. If you don't specify a value, Amazon EC2 uses the Spot bid price for the fleet\. For more information, see [How Spot Fleet Works](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String

`SubnetId`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-subnetid"></a>
The ID of the subnet in which to launch the instances\.  
*Required*: No  
*Type*: String

`TagSpecifications`  <a name="cfn-ec2-spotfleet-spotfleetlaunchspecification-tagspecifications"></a>
The tags to apply during creation\.  
*Required*: No  
*Type*: List of [Amazon EC2 SpotFleet SpotFleetTagSpecification](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-tagspecifications.md)

`UserData`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-userdata"></a>
Base64\-encoded MIME user data that instances use when starting up\.  
*Required*: No  
*Type*: String

`WeightedCapacity`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-weightedcapacity"></a>
The number of units provided by the specified instance type\. These units are the same units that you chose to set the target capacity in terms of instances or a performance characteristic, such as vCPUs, memory, or I/O\. For more information, see [How Spot Fleet Works](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
If the target capacity divided by this value is not a whole number, Amazon EC2 rounds the number of instances to the next whole number\.  
*Required*: No  
*Type*: Number
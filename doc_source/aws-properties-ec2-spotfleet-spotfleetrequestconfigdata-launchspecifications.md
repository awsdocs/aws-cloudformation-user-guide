# Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications"></a>

`LaunchSpecifications` is a property of the [Amazon EC2 SpotFleet SpotFleetRequestConfigData](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata.md) property that defines the launch specifications for the Spot fleet request\.

## Syntax<a name="w3ab2c21c14d613b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ebsoptimized)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile)" : IamInstanceProfile,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-imageid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-instancetype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-kernelid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-keyname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces)" : [ NetworkInterface, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement)" : Placement,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ramdiskid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups)" : [ SecurityGroup, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-spotprice)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-subnetid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-userdata)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-weightedcapacity)" : Number
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings):
  - BlockDeviceMapping
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ebsoptimized): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile):
  IamInstanceProfile
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-imageid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-instancetype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-kernelid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-keyname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces):
  - NetworkInterface
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement):
  Placement
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-ramdiskid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups):
  - SecurityGroup
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-spotprice): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-subnetid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-userdata): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-weightedcapacity): Number
```

## Properties<a name="w3ab2c21c14d613b7"></a>

`BlockDeviceMappings`  
Defines the block devices that are mapped to the Spot instances\.  
*Required: *No  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications BlockDeviceMappings](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings.md)

`EbsOptimized`  
Indicates whether the instances are optimized for Amazon Elastic Block Store \(Amazon EBS\) I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal EBS I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when you use an Amazon EBS\-optimized instance\.  
*Required: *No  
*Type*: Boolean

`IamInstanceProfile`  
Defines the AWS Identity and Access Management \(IAM\) instance profile to associate with the instances\.  
*Required: *No  
*Type*: [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications IamInstanceProfile](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile.md)

`ImageId`  
The unique ID of the Amazon Machine Image \(AMI\) to launch on the instances\.  
*Required: *Yes  
*Type*: String

`InstanceType`  
Specifies the instance type of the EC2 instances\.  
*Required: *Yes  
*Type*: String

`KernelId`  
The ID of the kernel that is associated with the Amazon Elastic Compute Cloud \(Amazon EC2\) AMI\.  
*Required: *No  
*Type*: String

`KeyName`  
An Amazon EC2 key pair to associate with the instances\.  
*Required: *No  
*Type*: String

`Monitoring`  
Enable or disable monitoring for the instances\.  
*Required: *No  
*Type*: [Amazon EC2 SpotFleet SpotFleetRequestConfigData LaunchSpecifications Monitoring](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-monitoring.md)

`NetworkInterfaces`  
The network interfaces to associate with the instances\.  
*Required: *No  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications NetworkInterfaces](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces.md)

`Placement`  
Defines a placement group, which is a logical grouping of instances within a single Availability Zone \(AZ\)\.  
*Required: *No  
*Type*: [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications Placement](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-placement.md)

`RamdiskId`  
The ID of the RAM disk to select\. Some kernels require additional drivers at launch\. Check the kernel requirements for information about whether you need to specify a RAM disk\. To find kernel requirements, refer to the AWS Resource Center and search for the kernel ID\.  
*Required: *No  
*Type*: String

`SecurityGroups`  
One or more security group IDs to associate with the instances\.  
*Required: *No  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications SecurityGroups](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups.md)

`SpotPrice`  
The bid price per unit hour for the specified instance type\. If you don't specify a value, Amazon EC2 uses the Spot bid price for the fleet\. For more information, see [How Spot Fleet Works](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *No  
*Type*: String

`SubnetId`  
The ID of the subnet in which to launch the instances\.  
*Required: *No  
*Type*: String

`UserData`  
Base64\-encoded MIME user data that instances use when starting up\.  
*Required: *No  
*Type*: String

`WeightedCapacity`  
The number of units provided by the specified instance type\. These units are the same units that you chose to set the target capacity in terms of instances or a performance characteristic, such as vCPUs, memory, or I/O\. For more information, see [How Spot Fleet Works](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
If the target capacity divided by this value is not a whole number, Amazon EC2 rounds the number of instances to the next whole number\.  
*Required: *No  
*Type*: Number
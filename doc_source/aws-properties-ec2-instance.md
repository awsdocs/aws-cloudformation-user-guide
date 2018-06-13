# AWS::EC2::Instance<a name="aws-properties-ec2-instance"></a>

The `AWS::EC2::Instance` resource creates an EC2 instance\.

If an Elastic IP address is attached to your instance, AWS CloudFormation reattaches the Elastic IP address after it updates the instance\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

**Topics**
+ [Syntax](#aws-resource-ec2-instance-syntax)
+ [Properties](#aws-properties-ec2-instance-prop)
+ [Return Values](#aws-properties-ec2-instance-returnvalues)
+ [Examples](#aws-properties-ec2-instance-examples)
+ [See Also](#w3ab2c21c10d409c17)

## Syntax<a name="aws-resource-ec2-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::Instance",
   "Properties" : {
      "[Affinity](#cfn-ec2-instance-affinity)" : String,
      "[AvailabilityZone](#cfn-ec2-instance-availabilityzone)" : String,
      "[BlockDeviceMappings](#cfn-ec2-instance-blockdevicemappings)" : [ EC2 Block Device Mapping, ... ],
      "[CreditSpecification](#cfn-ec2-instance-creditspecification)" : CreditSpecification,     
      "[DisableApiTermination](#cfn-ec2-instance-disableapitermination)" : Boolean,
      "[EbsOptimized](#cfn-ec2-instance-ebsoptimized)" : Boolean,
      "[ElasticGpuSpecifications](#cfn-ec2-instance-elasticgpuspecifications)" : [ ElasticGpuSpecification, ... ],
      "[HostId](#cfn-ec2-instance-hostid)" : String,
      "[IamInstanceProfile](#cfn-ec2-instance-iaminstanceprofile)" : String,
      "[ImageId](#cfn-ec2-instance-imageid)" : String,
      "[InstanceInitiatedShutdownBehavior](#cfn-ec2-instance-instanceinitiatedshutdownbehavior)" : String,
      "[InstanceType](#cfn-ec2-instance-instancetype)" : String,
      "[Ipv6AddressCount](#cfn-ec2-instance-ipv6addresscount)" : Integer,
      "[Ipv6Addresses](#cfn-ec2-instance-ipv6addresses)" : [ IPv6 Address Type, ... ],
      "[KernelId](#cfn-ec2-instance-kernelid)" : String,
      "[KeyName](#cfn-ec2-instance-keyname)" : String,
      "[LaunchTemplate](#cfn-ec2-instance-launchtemplate)" : [Amazon EC2 Instance LaunchTemplateSpecification](aws-properties-ec2-instance-launchtemplatespecification.md),
      "[Monitoring](#cfn-ec2-instance-monitoring)" : Boolean,
      "[NetworkInterfaces](#cfn-ec2-instance-networkinterfaces)" : [ EC2 Network Interface, ... ],
      "[PlacementGroupName](#cfn-ec2-instance-placementgroupname)" : String,
      "[PrivateIpAddress](#cfn-ec2-instance-privateipaddress)" : String,
      "[RamdiskId](#cfn-ec2-instance-ramdiskid)" : String,
      "[SecurityGroupIds](#cfn-ec2-instance-securitygroupids)" : [ String, ... ],
      "[SecurityGroups](#cfn-ec2-instance-securitygroups)" : [ String, ... ],
      "[SourceDestCheck](#cfn-ec2-instance-sourcedestcheck)" : Boolean,
      "[SsmAssociations](#cfn-ec2-instance-ssmassociations)" : [ SSMAssociation, ... ],
      "[SubnetId](#cfn-ec2-instance-subnetid)" : String,
      "[Tags](#cfn-ec2-instance-tags)" : [ Resource Tag, ... ],
      "[Tenancy](#cfn-ec2-instance-tenancy)" : String,
      "[UserData](#cfn-ec2-instance-userdata)" : String,
      "[Volumes](#cfn-ec2-instance-volumes)" : [ [EC2 MountPoint](aws-properties-ec2-mount-point.md), ... ],
      "[AdditionalInfo](#cfn-ec2-instance-additionalinfo)" : String
   }
}
```

### YAML<a name="aws-properties-ec2-instance-syntax.yaml"></a>

```
Type: "AWS::EC2::Instance"
Properties: 
  [Affinity](#cfn-ec2-instance-affinity): String
  [AvailabilityZone](#cfn-ec2-instance-availabilityzone): String
  [BlockDeviceMappings](#cfn-ec2-instance-blockdevicemappings): 
    - EC2 Block Device Mapping
  [CreditSpecification](#cfn-ec2-instance-creditspecification): CreditSpecification
  [DisableApiTermination](#cfn-ec2-instance-disableapitermination): Boolean
  [EbsOptimized](#cfn-ec2-instance-ebsoptimized): Boolean
  [ElasticGpuSpecifications](#cfn-ec2-instance-elasticgpuspecifications): [ ElasticGpuSpecification, ... ]
  [HostId](#cfn-ec2-instance-hostid): String
  [IamInstanceProfile](#cfn-ec2-instance-iaminstanceprofile): String
  [ImageId](#cfn-ec2-instance-imageid): String
  [InstanceInitiatedShutdownBehavior](#cfn-ec2-instance-instanceinitiatedshutdownbehavior): String
  [InstanceType](#cfn-ec2-instance-instancetype): String
  [Ipv6AddressCount](#cfn-ec2-instance-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-instance-ipv6addresses):
    - IPv6 Address Type
  [KernelId](#cfn-ec2-instance-kernelid): String
  [KeyName](#cfn-ec2-instance-keyname): String
  [LaunchTemplate](#cfn-ec2-instance-launchtemplate): [Amazon EC2 Instance LaunchTemplateSpecification](aws-properties-ec2-instance-launchtemplatespecification.md)
  [Monitoring](#cfn-ec2-instance-monitoring): Boolean
  [NetworkInterfaces](#cfn-ec2-instance-networkinterfaces): 
    - EC2 Network Interface
  [PlacementGroupName](#cfn-ec2-instance-placementgroupname): String
  [PrivateIpAddress](#cfn-ec2-instance-privateipaddress): String
  [RamdiskId](#cfn-ec2-instance-ramdiskid): String
  [SecurityGroupIds](#cfn-ec2-instance-securitygroupids): 
    - String
  [SecurityGroups](#cfn-ec2-instance-securitygroups): 
    - String
  [SourceDestCheck](#cfn-ec2-instance-sourcedestcheck): Boolean
  [SsmAssociations](#cfn-ec2-instance-ssmassociations): 
    - SSMAssociation
  [SubnetId](#cfn-ec2-instance-subnetid): String
  [Tags](#cfn-ec2-instance-tags): 
    - Resource Tag
  [Tenancy](#cfn-ec2-instance-tenancy): String
  [UserData](#cfn-ec2-instance-userdata): String
  [Volumes](#cfn-ec2-instance-volumes): 
    - EC2 MountPoint
  [AdditionalInfo](#cfn-ec2-instance-additionalinfo): String
```

## Properties<a name="aws-properties-ec2-instance-prop"></a>

`Affinity`  <a name="cfn-ec2-instance-affinity"></a>
Indicates whether Amazon Elastic Compute Cloud \(Amazon EC2\) always associates the instance with a [dedicated host](#cfn-ec2-instance-hostid)\. If you want Amazon EC2 to always restart the instance \(if it was stopped\) onto the same host on which it was launched, specify `host`\. If you want Amazon EC2 to restart the instance on any available host, but to try to launch the instance onto the last host it ran on \(on a best\-effort basis\), specify `default`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-instance-availabilityzone"></a>
Specifies the name of the Availability Zone in which the instance is located\.  
For more information about AWS regions and Availability Zones, see [Regions and Availability Zones](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) in the *Amazon EC2 User Guide*\.  
*Required*: No\. If not specified, an Availability Zone will be automatically chosen for you based on the load balancing criteria for the region\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`BlockDeviceMappings`  <a name="cfn-ec2-instance-blockdevicemappings"></a>
Defines a set of Amazon Elastic Block Store block device mappings, ephemeral instance store block device mappings, or both\. For more information, see [Amazon Elastic Block Store](http://docs.aws.amazon.com/AWSEC2/latest/DeveloperGuide/AmazonEBS.html) or [Amazon EC2 Instance Store](http://docs.aws.amazon.com/AWSEC2/latest/DeveloperGuide/InstanceStorage.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: A list of [Amazon EC2 Block Device Mapping Property](aws-properties-ec2-blockdev-mapping.md)\.  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\. If you change only the `DeleteOnTermination` property for one or more block devices, update requires [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`CreditSpecification`  <a name="cfn-ec2-instance-creditspecification"></a>
Specifies the credit option for CPU usage of a T2 instance\.  
*Required*: No  
*Type*: [Amazon EC2 Instance CreditSpecification](aws-properties-ec2-instance-creditspecification.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DisableApiTermination`  <a name="cfn-ec2-instance-disableapitermination"></a>
Specifies whether the instance can be terminated through the API\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EbsOptimized`  <a name="cfn-ec2-instance-ebsoptimized"></a>
Specifies whether the instance is optimized for Amazon Elastic Block Store I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal `EBS` I/O performance\.  
For more information about the instance types that can be launched as Amazon EBS optimized instances, see [Amazon EBS\-Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon Elastic Compute Cloud User Guide*\. Additional fees are incurred when using Amazon EBS\-optimized instances\.  
*Required*: No\. By default, AWS CloudFormation specifies `false`\.  
*Type*: Boolean  
*Update requires*:  
+ *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) for Amazon EBS\-backed instances
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for instance store\-backed instances

`ElasticGpuSpecifications`  <a name="cfn-ec2-instance-elasticgpuspecifications"></a>
Specifies the Elastic GPUs\. An Elastic GPU is a GPU resource that you can attach to your instance to accelerate the graphics performance of your applications\. For more information, see [Amazon EC2 Elastic GPUs](http://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/elastic-gpus.html) in the *Amazon EC2 User Guide for Windows Instances*\. Duplicates are not allowed\.  
*Required*: No  
*Type:* List of [Amazon EC2 Instance ElasticGpuSpecification](aws-properties-ec2-instance-elasticgpuspecification.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`HostId`  <a name="cfn-ec2-instance-hostid"></a>
If you specify `host` for the `Affinity` property, the ID of a dedicated host that the instance is associated with\. If you don't specify an ID, Amazon EC2 launches the instance onto any available, compatible dedicated host in your account\. This type of launch is called an untargeted launch\. Note that for untargeted launches, you must have a compatible, dedicated host available to successfully launch instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IamInstanceProfile`  <a name="cfn-ec2-instance-iaminstanceprofile"></a>
The name of an instance profile or a reference to an [AWS::IAM::InstanceProfile](aws-resource-iam-instanceprofile.md) resource\.  
For more information about IAM roles, see [Working with Roles](http://docs.aws.amazon.com/IAM/latest/UserGuide/WorkingWithRoles.html) in the *AWS Identity and Access Management User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ImageId`  <a name="cfn-ec2-instance-imageid"></a>
Provides the unique ID of the Amazon Machine Image \(AMI\) that was assigned during registration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceInitiatedShutdownBehavior`  <a name="cfn-ec2-instance-instanceinitiatedshutdownbehavior"></a>
Indicates whether an instance stops or terminates when you shut down the instance from the instance's operating system shutdown command\. You can specify `stop` or `terminate`\. For more information, see the [RunInstances](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-RunInstances.html) command in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceType`  <a name="cfn-ec2-instance-instancetype"></a>
The instance type, such as `t2.micro`\. The default type is `"m3.medium"`\. For a list of instance types, see [Instance Families and Types](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html)\.  
*Required*: No  
*Type*: String  
*Update requires*:  
+ *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) for Amazon EBS\-backed instances
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for instance store\-backed instances

`Ipv6AddressCount`  <a name="cfn-ec2-instance-ipv6addresscount"></a>
The number of IPv6 addresses to associate with the instance's primary network interface\. Amazon EC2 automatically selects the IPv6 addresses from the subnet range\. To specify specific IPv6 addresses, use the `Ipv6Addresses` property and don't specify this property\.  
For restrictions on which instance types support IPv6 addresses, see the [RunInstances](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-RunInstances.html) action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Ipv6Addresses`  <a name="cfn-ec2-instance-ipv6addresses"></a>
One or more specific IPv6 addresses from the IPv6 CIDR block range of your subnet to associate with the instance's primary network interface\. To specify a number of IPv6 addresses, use the `Ipv6AddressCount` property and don't specify this property\.  
For information about restrictions on which instance types support IPv6 addresses, see the [RunInstances](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-RunInstances.html) action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: List of [EC2 NetworkInterface Ipv6Addresses](aws-properties-ec2-networkinterface-ipv6addresses.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KernelId`  <a name="cfn-ec2-instance-kernelid"></a>
The kernel ID\.  
*Required*: No  
*Type*: String  
*Update requires*:  
+ *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) for Amazon EBS\-backed instances
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for instance store\-backed instances

`KeyName`  <a name="cfn-ec2-instance-keyname"></a>
Provides the name of the Amazon EC2 key pair\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LaunchTemplate`  <a name="cfn-ec2-instance-launchtemplate"></a>
The launch template to use\.  
*Required*: No  
*Type*: [Amazon EC2 Instance LaunchTemplateSpecification](aws-properties-ec2-instance-launchtemplatespecification.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Monitoring`  <a name="cfn-ec2-instance-monitoring"></a>
Specifies whether detailed monitoring is enabled for the instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NetworkInterfaces`  <a name="cfn-ec2-instance-networkinterfaces"></a>
A list of embedded objects that describes the network interfaces to associate with this instance\.  
If you use this property to point to a network interface, you must terminate the original interface before attaching a new one to allow the update of the instance to succeed\.  
If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the `DependsOn` attribute to declare a dependency on the VPC\-gateway attachment\. For more information, see [DependsOn Attribute](aws-attribute-dependson.md)\.
*Required*: No  
*Type*: A list of [EC2 NetworkInterface Embedded Property Type](aws-properties-ec2-network-iface-embedded.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PlacementGroupName`  <a name="cfn-ec2-instance-placementgroupname"></a>
The name of an existing placement group that you want to launch the instance into \(for cluster instances\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PrivateIpAddress`  <a name="cfn-ec2-instance-privateipaddress"></a>
The private IP address for this instance\.  
If you make an update to an instance that requires replacement, you must assign a new private IP address\. During a replacement, AWS CloudFormation creates a new instance but doesn't delete the old instance until the stack has successfully updated\. If the stack update fails, AWS CloudFormation uses the old instance in order to roll back the stack to the previous working state\. The old and new instances cannot have the same private IP address\.
\(Optional\) If you're using Amazon VPC, you can use this parameter to assign the instance a specific available IP address from the subnet \(for example, 10\.0\.0\.25\)\. By default, Amazon VPC selects an IP address from the subnet for the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RamdiskId`  <a name="cfn-ec2-instance-ramdiskid"></a>
The ID of the RAM disk to select\. Some kernels require additional drivers at launch\. Check the kernel requirements for information about whether you need to specify a RAM disk\. To find kernel requirements, go to the AWS Resource Center and search for the kernel ID\.  
*Required*: No  
*Type*: String  
*Update requires*:  
+ *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) for Amazon EBS\-backed instances
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for instance store\-backed instances

`SecurityGroupIds`  <a name="cfn-ec2-instance-securitygroupids"></a>
A list that contains the security group IDs for VPC security groups to assign to the Amazon EC2 instance\. If you specified the `NetworkInterfaces` property, do not specify this property\.  
*Required*: Conditional\. Required for VPC security groups\.  
*Type*: List of String values  
*Update requires*:  
+ *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) for instances that are in a VPC\.
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for instances that are not in a VPC\.

`SecurityGroups`  <a name="cfn-ec2-instance-securitygroups"></a>
Valid only for Amazon EC2 security groups\. A list that contains the Amazon EC2 security groups to assign to the Amazon EC2 instance\. The list can contain both the name of existing Amazon EC2 security groups or references to AWS::EC2::SecurityGroup resources created in the template\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`SourceDestCheck`  <a name="cfn-ec2-instance-sourcedestcheck"></a>
Controls whether source/destination checking is enabled on the instance\. Also determines if an instance in a VPC will perform network address translation \(NAT\)\.  
A value of `"true"` means that source/destination checking is enabled, and a value of `"false"` means that checking is disabled\. For the instance to perform NAT, the value *must* be `"false"`\. For more information, see [NAT Instances](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_NAT_Instance.html) in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SsmAssociations`  <a name="cfn-ec2-instance-ssmassociations"></a>
The SSM [document](aws-resource-ssm-document.md) and parameter values in AWS Systems Manager to associate with this instance\. To use this property, you must specify an IAM instance profile role for the instance\. For more information, see [Create an Instance Profile for Systems Manager](http://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-configuring-access-role.html) in the *AWS Systems Manager User Guide*\.  
You can currently associate only one document with an instance\.
*Required*: No  
*Type*: List of [Amazon EC2 Instance SsmAssociations](aws-properties-ec2-instance-ssmassociations.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetId`  <a name="cfn-ec2-instance-subnetid"></a>
If you're using Amazon VPC, this property specifies the ID of the subnet that you want to launch the instance into\. If you specified the `NetworkInterfaces` property, do not specify this property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-ec2-instance-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this instance\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`Tenancy`  <a name="cfn-ec2-instance-tenancy"></a>
The tenancy of the instance that you want to launch, such as `default`, `dedicated`, or `host`\. If you specify a tenancy value of `dedicated` or `host`, you must launch the instance in a VPC\. For more information, see [Dedicated Instances](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/dedicated-instance.html) in the *Amazon VPC User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*:  
+ *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) if this property was set to `dedicated` and you change it to `host` or vice versa\.
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for all other changes\.

`UserData`  <a name="cfn-ec2-instance-userdata"></a>
Base64\-encoded MIME user data that is made available to the instances\.  
*Required*: No  
*Type*: String  
*Update requires*:  
+ *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) for Amazon EBS\-backed instances\.
**Note**  
For EBS\-backed instances, changing the `UserData` stops and then starts the instance; however, Amazon EC2 doesn't automatically run the updated `UserData`\. To update configurations on your instance, use the [cfn\-hup](cfn-hup.md) helper script\.
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for instance store\-backed instances\.

`Volumes`  <a name="cfn-ec2-instance-volumes"></a>
The Amazon EBS volumes to attach to the instance\.  
Before detaching a volume, unmount any file systems on the device within your operating system\. If you don't unmount the file system, a volume might get stuck in a busy state while detaching\.
*Required*: No  
*Type*: A list of [EC2 MountPoints](aws-properties-ec2-mount-point.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AdditionalInfo`  <a name="cfn-ec2-instance-additionalinfo"></a>
Reserved\.  
*Required*: No  
*Type*: String  
*Update requires*:  
+ *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) for Amazon EBS\-backed instances
+ *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) for instance store\-backed instances

## Return Values<a name="aws-properties-ec2-instance-returnvalues"></a>

### Ref<a name="aws-properties-ec2-instance-ref"></a>

When you pass the logical ID of an AWS::EC2::Instance object to the intrinsic `Ref` function, the object's InstanceId is returned\. For example: `i-636be302`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d409c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`AvailabilityZone`  
The Availability Zone where the specified instance is launched\. For example: `us-east-1b`\.  
You can retrieve a list of all Availability Zones for a region by using the [`Fn::GetAZs`](intrinsic-function-reference-getavailabilityzones.md) intrinsic function\.

`PrivateDnsName`  
The private DNS name of the specified instance\. For example: `ip-10-24-34-0.ec2.internal`\.

`PublicDnsName`  
The public DNS name of the specified instance\. For example: `ec2-107-20-50-45.compute-1.amazonaws.com`\.

`PrivateIp`  
The private IP address of the specified instance\. For example: `10.24.34.0`\.

`PublicIp`  
The public IP address of the specified instance\. For example: `192.0.2.0`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-properties-ec2-instance-examples"></a>

### EC2 Instance with an EBS Block Device Mapping<a name="w3ab2c21c10d409c15b2"></a>

#### JSON<a name="aws-properties-ec2-instance-examples-json1"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Description" : "Ec2 block device mapping",
   "Resources" : {
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
   }
}
```

#### YAML<a name="aws-properties-ec2-instance-examples-yaml1"></a>

```
  AWSTemplateFormatVersion: "2010-09-09"
  Description: "Ec2 block device mapping"
  Resources: 
    MyEC2Instance: 
      Type: "AWS::EC2::Instance"
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

### Automatically Assign a Public IP Address<a name="w3ab2c21c10d409c15b4"></a>

You can associate a public IP address with a network interface only if it has a device index of `0` and if it is a new network interface \(not an existing one\)\.

#### JSON<a name="aws-properties-ec2-instance-examples-json2"></a>

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

#### YAML<a name="aws-properties-ec2-instance-examples-yaml2"></a>

```
  Ec2Instance: 
    Type: "AWS::EC2::Instance"
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

### Other Examples<a name="w3ab2c21c10d409c15b6"></a>

You can download templates that show how to use `AWS::EC2::Instance` to create a virtual private cloud \(VPC\):
+ [Single instance in a single subnet](https://s3.amazonaws.com/cloudformation-templates-us-east-1/vpc_single_instance_in_subnet.template)
+ [Multiple subnets with ELB and Auto Scaling group](https://s3.amazonaws.com/cloudformation-templates-us-east-1/vpc_multiple_subnets.template)

For more information about an `AWS::EC2::Instance` that has an IAM instance profile, see: [Create an EC2 instance with an associated instance profile](https://s3.amazonaws.com/cloudformation-templates-us-east-1/ec2_instance_with_instance_profile.template)\.

For more information about Amazon EC2 template examples, see: [Amazon EC2 Template Snippets](quickref-ec2.md)\.

## See Also<a name="w3ab2c21c10d409c17"></a>
+ [RunInstances](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-RunInstances.html) in the *Amazon Elastic Compute Cloud API Reference*
+ [EBS\-Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#EBSOptimized) in the *Amazon Elastic Compute Cloud User Guide*
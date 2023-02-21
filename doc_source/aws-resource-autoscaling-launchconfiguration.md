# AWS::AutoScaling::LaunchConfiguration<a name="aws-resource-autoscaling-launchconfiguration"></a>

The `AWS::AutoScaling::LaunchConfiguration` resource specifies the launch configuration that can be used by an Auto Scaling group to configure Amazon EC2 instances\. 

When you update the launch configuration for an Auto Scaling group, CloudFormation deletes that resource and creates a new launch configuration with the updated properties and a new name\. Existing instances are not affected\. To update existing instances when you update the `AWS::AutoScaling::LaunchConfiguration` resource, you can specify an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for the group\. You can find sample update policies for rolling updates in [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\. 

**Note**  
Amazon EC2 Auto Scaling configures instances launched as part of an Auto Scaling group using either a [launch template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) or a launch configuration\. We strongly recommend that you do not use launch configurations\. They do not provide full functionality for Amazon EC2 Auto Scaling or Amazon EC2\. For more information, see [Launch configurations](https://docs.aws.amazon.com/autoscaling/ec2/userguide/launch-configurations.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-resource-autoscaling-launchconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-launchconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::LaunchConfiguration",
  "Properties" : {
      "[AssociatePublicIpAddress](#cfn-autoscaling-launchconfiguration-associatepublicipaddress)" : Boolean,
      "[BlockDeviceMappings](#cfn-autoscaling-launchconfiguration-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
      "[ClassicLinkVPCId](#cfn-autoscaling-launchconfiguration-classiclinkvpcid)" : String,
      "[ClassicLinkVPCSecurityGroups](#cfn-autoscaling-launchconfiguration-classiclinkvpcsecuritygroups)" : [ String, ... ],
      "[EbsOptimized](#cfn-autoscaling-launchconfiguration-ebsoptimized)" : Boolean,
      "[IamInstanceProfile](#cfn-autoscaling-launchconfiguration-iaminstanceprofile)" : String,
      "[ImageId](#cfn-autoscaling-launchconfiguration-imageid)" : String,
      "[InstanceId](#cfn-autoscaling-launchconfiguration-instanceid)" : String,
      "[InstanceMonitoring](#cfn-autoscaling-launchconfiguration-instancemonitoring)" : Boolean,
      "[InstanceType](#cfn-autoscaling-launchconfiguration-instancetype)" : String,
      "[KernelId](#cfn-autoscaling-launchconfiguration-kernelid)" : String,
      "[KeyName](#cfn-autoscaling-launchconfiguration-keyname)" : String,
      "[LaunchConfigurationName](#cfn-autoscaling-launchconfiguration-launchconfigurationname)" : String,
      "[MetadataOptions](#cfn-autoscaling-launchconfiguration-metadataoptions)" : MetadataOptions,
      "[PlacementTenancy](#cfn-autoscaling-launchconfiguration-placementtenancy)" : String,
      "[RamDiskId](#cfn-autoscaling-launchconfiguration-ramdiskid)" : String,
      "[SecurityGroups](#cfn-autoscaling-launchconfiguration-securitygroups)" : [ String, ... ],
      "[SpotPrice](#cfn-autoscaling-launchconfiguration-spotprice)" : String,
      "[UserData](#cfn-autoscaling-launchconfiguration-userdata)" : String
    }
}
```

### YAML<a name="aws-resource-autoscaling-launchconfiguration-syntax.yaml"></a>

```
Type: AWS::AutoScaling::LaunchConfiguration
Properties: 
  [AssociatePublicIpAddress](#cfn-autoscaling-launchconfiguration-associatepublicipaddress): Boolean
  [BlockDeviceMappings](#cfn-autoscaling-launchconfiguration-blockdevicemappings): 
    - BlockDeviceMapping
  [ClassicLinkVPCId](#cfn-autoscaling-launchconfiguration-classiclinkvpcid): String
  [ClassicLinkVPCSecurityGroups](#cfn-autoscaling-launchconfiguration-classiclinkvpcsecuritygroups): 
    - String
  [EbsOptimized](#cfn-autoscaling-launchconfiguration-ebsoptimized): Boolean
  [IamInstanceProfile](#cfn-autoscaling-launchconfiguration-iaminstanceprofile): String
  [ImageId](#cfn-autoscaling-launchconfiguration-imageid): String
  [InstanceId](#cfn-autoscaling-launchconfiguration-instanceid): String
  [InstanceMonitoring](#cfn-autoscaling-launchconfiguration-instancemonitoring): Boolean
  [InstanceType](#cfn-autoscaling-launchconfiguration-instancetype): String
  [KernelId](#cfn-autoscaling-launchconfiguration-kernelid): String
  [KeyName](#cfn-autoscaling-launchconfiguration-keyname): String
  [LaunchConfigurationName](#cfn-autoscaling-launchconfiguration-launchconfigurationname): String
  [MetadataOptions](#cfn-autoscaling-launchconfiguration-metadataoptions): 
    MetadataOptions
  [PlacementTenancy](#cfn-autoscaling-launchconfiguration-placementtenancy): String
  [RamDiskId](#cfn-autoscaling-launchconfiguration-ramdiskid): String
  [SecurityGroups](#cfn-autoscaling-launchconfiguration-securitygroups): 
    - String
  [SpotPrice](#cfn-autoscaling-launchconfiguration-spotprice): String
  [UserData](#cfn-autoscaling-launchconfiguration-userdata): String
```

## Properties<a name="aws-resource-autoscaling-launchconfiguration-properties"></a>

`AssociatePublicIpAddress`  <a name="cfn-autoscaling-launchconfiguration-associatepublicipaddress"></a>
Specifies whether to assign a public IPv4 address to the group's instances\. If the instance is launched into a default subnet, the default is to assign a public IPv4 address, unless you disabled the option to assign a public IPv4 address on the subnet\. If the instance is launched into a nondefault subnet, the default is not to assign a public IPv4 address, unless you enabled the option to assign a public IPv4 address on the subnet\.  
If you specify `true`, each instance in the Auto Scaling group receives a unique public IPv4 address\. For more information, see [Launching Auto Scaling instances in a VPC](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-in-vpc.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
If you specify this property, you must specify at least one subnet for `VPCZoneIdentifier` when you create your group\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BlockDeviceMappings`  <a name="cfn-autoscaling-launchconfiguration-blockdevicemappings"></a>
The block device mapping entries that define the block devices to attach to the instances at launch\. By default, the block devices specified in the block device mapping for the AMI are used\. For more information, see [Block device mappings](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/block-device-mapping-concepts.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: List of [BlockDeviceMapping](aws-properties-autoscaling-launchconfiguration-blockdevicemapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClassicLinkVPCId`  <a name="cfn-autoscaling-launchconfiguration-classiclinkvpcid"></a>
Available for backward compatibility\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClassicLinkVPCSecurityGroups`  <a name="cfn-autoscaling-launchconfiguration-classiclinkvpcsecuritygroups"></a>
Available for backward compatibility\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsOptimized`  <a name="cfn-autoscaling-launchconfiguration-ebsoptimized"></a>
Specifies whether the launch configuration is optimized for EBS I/O \(`true`\) or not \(`false`\)\. The optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal I/O performance\. This optimization is not available with all instance types\. Additional fees are incurred when you enable EBS optimization for an instance type that is not EBS\-optimized by default\. For more information, see [Amazon EBS\-optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamInstanceProfile`  <a name="cfn-autoscaling-launchconfiguration-iaminstanceprofile"></a>
The name or the Amazon Resource Name \(ARN\) of the instance profile associated with the IAM role for the instance\. The instance profile contains the IAM role\. For more information, see [IAM role for applications that run on Amazon EC2 instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/us-iam-role.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageId`  <a name="cfn-autoscaling-launchconfiguration-imageid"></a>
The ID of the Amazon Machine Image \(AMI\) that was assigned during registration\. For more information, see [Finding a Linux AMI](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/finding-an-ami.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
If you specify `InstanceId`, an `ImageId` is not required\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceId`  <a name="cfn-autoscaling-launchconfiguration-instanceid"></a>
The ID of the Amazon EC2 instance to use to create the launch configuration\. When you use an instance to create a launch configuration, all properties are derived from the instance with the exception of `BlockDeviceMapping` and `AssociatePublicIpAddress`\. You can override any properties from the instance by specifying them in the launch configuration\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceMonitoring`  <a name="cfn-autoscaling-launchconfiguration-instancemonitoring"></a>
Controls whether instances in this group are launched with detailed \(`true`\) or basic \(`false`\) monitoring\.  
The default value is `true` \(enabled\)\.  
When detailed monitoring is enabled, Amazon CloudWatch generates metrics every minute and your account is charged a fee\. When you disable detailed monitoring, CloudWatch generates metrics every 5 minutes\. For more information, see [Configure Monitoring for Auto Scaling Instances](https://docs.aws.amazon.com/autoscaling/latest/userguide/enable-as-instance-metrics.html) in the *Amazon EC2 Auto Scaling User Guide*\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-autoscaling-launchconfiguration-instancetype"></a>
Specifies the instance type of the EC2 instance\. For information about available instance types, see [Available instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableInstanceTypes) in the *Amazon EC2 User Guide for Linux Instances*\.  
If you specify `InstanceId`, an `InstanceType` is not required\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KernelId`  <a name="cfn-autoscaling-launchconfiguration-kernelid"></a>
The ID of the kernel associated with the AMI\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User provided kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyName`  <a name="cfn-autoscaling-launchconfiguration-keyname"></a>
The name of the key pair\. For more information, see [Amazon EC2 key pairs and Linux instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchConfigurationName`  <a name="cfn-autoscaling-launchconfiguration-launchconfigurationname"></a>
The name of the launch configuration\. This name must be unique per Region per account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MetadataOptions`  <a name="cfn-autoscaling-launchconfiguration-metadataoptions"></a>
The metadata options for the instances\. For more information, see [Configuring the Instance Metadata Options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-config.html#launch-configurations-imds) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: [MetadataOptions](aws-properties-autoscaling-launchconfiguration-metadataoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlacementTenancy`  <a name="cfn-autoscaling-launchconfiguration-placementtenancy"></a>
The tenancy of the instance, either `default` or `dedicated`\. An instance with `dedicated` tenancy runs on isolated, single\-tenant hardware and can only be launched into a VPC\. To launch dedicated instances into a shared tenancy VPC \(a VPC with the instance placement tenancy attribute set to `default`\), you must set the value of this property to `dedicated`\. For more information, see [Configuring instance tenancy with Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-dedicated-instances.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
If you specify `PlacementTenancy`, you must specify at least one subnet for `VPCZoneIdentifier` when you create your group\.  
Valid values: `default` \| `dedicated`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RamDiskId`  <a name="cfn-autoscaling-launchconfiguration-ramdiskid"></a>
The ID of the RAM disk to select\.  
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User provided kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-autoscaling-launchconfiguration-securitygroups"></a>
A list that contains the security groups to assign to the instances in the Auto Scaling group\. The list can contain both the IDs of existing security groups and references to [SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resources created in the template\.  
For more information, see [Control traffic to resources using security groups](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html) in the *Amazon Virtual Private Cloud User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpotPrice`  <a name="cfn-autoscaling-launchconfiguration-spotprice"></a>
The maximum hourly price to be paid for any Spot Instance launched to fulfill the request\. Spot Instances are launched when the price you specify exceeds the current Spot price\. For more information, see [Request Spot Instances for fault\-tolerant and flexible applications](https://docs.aws.amazon.com/autoscaling/ec2/userguide/launch-template-spot-instances.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
Valid Range: Minimum value of 0\.001  
When you change your maximum price by creating a new launch configuration, running instances will continue to run as long as the maximum price for those running instances is higher than the current Spot price\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserData`  <a name="cfn-autoscaling-launchconfiguration-userdata"></a>
The Base64\-encoded user data to make available to the launched EC2 instances\. For more information, see [Instance metadata and user data](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Maximum*: `21847`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-autoscaling-launchconfiguration-return-values"></a>

### Ref<a name="aws-resource-autoscaling-launchconfiguration-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-mylaunchconfig-1DDYF1E3B3I`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Remarks<a name="aws-resource-autoscaling-launchconfiguration--remarks"></a>

CloudFormation marks the Auto Scaling group as successful \(by setting its status to CREATE\_COMPLETE\) when its desired capacity is reached\. However, if `SpotPrice` is set in the launch configuration, then desired capacity is not used as a criteria for success\. Whether your request is fulfilled depends on Spot Instance capacity and your maximum price\. If the current Spot price is less than your specified maximum price, Amazon EC2 Auto Scaling uses the desired capacity as the target capacity for the group\. If the request for Spot Instances is unsuccessful, it keeps trying\. 

If your Auto Scaling instances receive a public IPv4 address and are launched in a VPC that is defined in the same stack template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the [VPC\-gateway attachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-gateway-attachment.html)\. 

## Examples<a name="aws-resource-autoscaling-launchconfiguration--examples"></a>

The following examples create launch configurations that can be used by an Auto Scaling group to configure Amazon EC2 instances\. 

**Note**  
For examples of Amazon EC2 launch templates, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate--examples) section of the `AWS::EC2::LaunchTemplate` resources\.

### Amazon EBS\-backed AMI and defined block device mappings<a name="aws-resource-autoscaling-launchconfiguration--examples--Amazon_EBS-backed_AMI_and_defined_block_device_mappings"></a>

This example shows a launch configuration with a `BlockDeviceMappings` property that lists two devices: a 30 gigabyte EBS root volume mapped to /dev/sda1 and a 100 gigabyte EBS volume mapped to /dev/sdm\. The /dev/sdm volume uses the default EBS volume type based on the region and is not deleted when terminating the instance it is attached to\. 

CloudFormation supports parameters from the AWS Systems Manager Parameter Store\. In this example, the `ImageId` property references the latest Amazon Linux 2 AMI \(EBS\-backed image\) from the Parameter Store\. For more information, see [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) in the *AWS Systems Manager User Guide* and the blog post [Query for the latest Amazon Linux AMI IDs using AWS Systems Manager Parameter Store](http://aws.amazon.com/blogs/compute/query-for-the-latest-amazon-linux-ami-ids-using-aws-systems-manager-parameter-store/) on the AWS Compute Blog\.

#### JSON<a name="aws-resource-autoscaling-launchconfiguration--examples--Amazon_EBS-backed_AMI_and_defined_block_device_mappings--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters": {
    "LatestAmiId": {
      "Description": "Region specific image from the Parameter Store",
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
    },
    "InstanceType": {
      "Description": "Amazon EC2 instance type for the instances",
      "Type": "String",
      "AllowedValues": [
        "t3.micro",
        "t3.small",
        "t3.medium"
      ],
      "Default": "t3.micro"
    }
  },  
  "Resources":{
    "myLaunchConfig":{
      "Type":"AWS::AutoScaling::LaunchConfiguration",
      "Properties":{
        "ImageId":{ "Ref":"LatestAmiId" },
        "SecurityGroups":[ { "Ref":"myEC2SecurityGroup" } ],
        "InstanceType":{ "Ref":"InstanceType" },
        "BlockDeviceMappings":[
          {
            "DeviceName":"/dev/sda1",
            "Ebs":{
              "VolumeSize":"30",
              "VolumeType":"gp3"
            }
          },
          {
            "DeviceName":"/dev/sdm",
            "Ebs":{
              "VolumeSize":"100",
              "DeleteOnTermination":"false"
            }
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-launchconfiguration--examples--Amazon_EBS-backed_AMI_and_defined_block_device_mappings--yaml"></a>

```
---
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  LatestAmiId:
    Description: Region specific image from the Parameter Store
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: '/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2'
  InstanceType:
    Description: Amazon EC2 instance type for the instances
    Type: String
    AllowedValues:
      - t3.micro
      - t3.small
      - t3.medium
    Default: t3.micro
Resources:
  myLaunchConfig: 
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties:
      ImageId: !Ref LatestAmiId
      SecurityGroups: 
        - !Ref myEC2SecurityGroup
      InstanceType: 
        !Ref InstanceType
      BlockDeviceMappings: 
        - DeviceName: /dev/sda1
          Ebs: 
            VolumeSize: '30'
            VolumeType: gp3
        - DeviceName: /dev/sdm
          Ebs: 
            VolumeSize: '100'
            DeleteOnTermination: false
```

### Instance store\-backed AMI with Spot price and IAM role<a name="aws-resource-autoscaling-launchconfiguration--examples--Instance_store-backed_AMI_with_Spot_price_and_IAM_role"></a>

This example shows a launch configuration that launches Spot Instances in the Auto Scaling group\. This launch configuration will only be active if the current Spot price is less than the price in the template specification \(0\.045\)\. It also demonstrates a launch configuration that uses the `IamInstanceProfile` property\. For an example of a full template, including the definition of, and further references from the [InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html) object referenced here as `RootInstanceProfile`, see [auto\_scaling\_with\_instance\_profile\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/auto_scaling_with_instance_profile.template)\.

In this example, the `ImageId` property references the latest Amazon Linux AMI \(instance store/S3\-backed image\) from the Parameter Store\. The BlockDeviceMappings property lists a virtual device `ephemeral0` mapped to /dev/sdc\.

#### JSON<a name="aws-resource-autoscaling-launchconfiguration--examples--Instance_store-backed_AMI_with_Spot_price_and_IAM_role--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters": {
    "LatestAmiId": {
      "Description": "Region specific image from the Parameter Store",
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-amazon-linux-latest/amzn-ami-hvm-x86_64-s3"
    }
  },
  "Resources":{
    "myLaunchConfig":{
      "Type":"AWS::AutoScaling::LaunchConfiguration",
      "Properties":{
        "ImageId":{ "Ref":"LatestAmiId" },
        "SecurityGroups":[ { "Ref":"myEC2SecurityGroup" } ],
        "InstanceType":"m3.medium",
        "SpotPrice":"0.045",
        "IamInstanceProfile":{ "Ref":"RootInstanceProfile" },
        "BlockDeviceMappings": [
          {
            "DeviceName": "/dev/sdc",
            "VirtualName": "ephemeral0"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-launchconfiguration--examples--Instance_store-backed_AMI_with_Spot_price_and_IAM_role--yaml"></a>

```
---
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  LatestAmiId:
    Description: Region specific image from the Parameter Store
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: '/aws/service/ami-amazon-linux-latest/amzn-ami-hvm-x86_64-s3'
Resources:
  myLaunchConfig: 
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties: 
      ImageId: !Ref LatestAmiId
      SecurityGroups: 
        - !Ref myEC2SecurityGroup
      InstanceType: m3.medium
      SpotPrice: '0.045'
      IamInstanceProfile: !Ref RootInstanceProfile
      BlockDeviceMappings:
      - DeviceName: /dev/sdc
        VirtualName: ephemeral0
```

### Provisioned IOPS EBS\-optimized volume with key\-pair name and user data<a name="aws-resource-autoscaling-launchconfiguration--examples--Provisioned_IOPS_EBS-optimized_volume_with_key-pair_name_and_user_data"></a>

This example demonstrates a launch configuration that configures the `EbsOptmized` property to launch instances with a provisioned IOPS EBS\-optimized volume\. This can increase the performance of your EBS\-backed instances\.

**Note**  
For instances that are not EBS–optimized by default, you must enable EBS optimization to achieve the level of performance described in the [Amazon EBS\-optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) documentation in the *Amazon Elastic Compute Cloud User Guide*\. For current generation instance types, EBS\-optimization is enabled by default at no additional cost\. Enabling EBS optimization for a previous generation instance type that is not EBS\-optimized by default incurs additional fees\.

When you use a launch configuration such as this one, your `m1.large` instances will contain optimized EBS root volumes with the provisioned IOPS settings that you specified in the AMI\. Because you cannot specify the IOPS settings in a launch configuration, the AMI must be configured with a block device mapping that specifies the desired number of IOPS\. The following are key attributes of this EBS\-optimized instance configuration:
+ An instance type of `m1.large` or greater\. This is required for EBS optimization\. This optimization is only available for certain instance types and sizes\.
+ An EBS\-backed AMI with a volume type of `io1` and the number of IOPS you want to provision for the volume\. 
+ The size of the EBS volume must accommodate the IOPS you need\. There is a 50:1 ratio between IOPS and Gibibytes \(GiB\) of storage\.

For more information about IOPS performance with provisioned IOPS volumes, see [Provisioned IOPS SSD \(`io1` and `io2`\) volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html#EBSVolumeTypes_piops) in the *Amazon Elastic Compute Cloud User Guide*\.

For more performance tips, see [Amazon EBS volume performance on Linux instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSPerformance.html) in the *Amazon Elastic Compute Cloud User Guide*\. 



#### JSON<a name="aws-resource-autoscaling-launchconfiguration--examples--Provisioned_IOPS_EBS-optimized_volume_with_key-pair_name_and_user_data--json"></a>

```
{
  "Resources":{
    "myLaunchConfig":{
      "Type":"AWS::AutoScaling::LaunchConfiguration",
      "Properties":{
        "ImageId":"ami-02354e95b3example",
        "SecurityGroups":[ { "Ref":"myEC2SecurityGroup" }, "myExistingEC2SecurityGroup" ],
        "InstanceType":"m1.large",
        "UserData": {"Fn::Base64": {"Fn::Join": ["", [
          "#!/bin/bash -x\n",
          "/opt/aws/bin/cfn-signal -e $? --stack ", {"Ref": "AWS::StackName"}, " --resource myASG ", " --region ", {"Ref": "AWS::Region"}, "\n"
        ]]}},
        "EbsOptimized":"true"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-launchconfiguration--examples--Provisioned_IOPS_EBS-optimized_volume_with_key-pair_name_and_user_data--yaml"></a>

```
---
Resources:
  myLaunchConfig: 
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties: 
      ImageId: ami-02354e95b3example
      SecurityGroups: 
        - !Ref myEC2SecurityGroup
        - myExistingEC2SecurityGroup
      InstanceType: m1.large
      UserData: !Base64 |
        #!/bin/bash -x
        yum install -y aws-cfn-bootstrap
        /opt/aws/bin/cfn-signal -e $? --stack !Ref 'AWS::StackName' --resource myASG --region !Ref 'AWS::Region'
      EbsOptimized: true
```

## See also<a name="aws-resource-autoscaling-launchconfiguration--seealso"></a>
+ [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)
+ [CreateLaunchConfiguration](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CreateLaunchConfiguration.html) in the *Amazon EC2 Auto Scaling API Reference*


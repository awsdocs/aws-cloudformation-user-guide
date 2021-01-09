# AWS::AutoScaling::LaunchConfiguration<a name="aws-properties-as-launchconfig"></a>

The `AWS::AutoScaling::LaunchConfiguration` resource specifies the launch configuration that can be used by an Auto Scaling group to configure Amazon EC2 instances\. 

When you update the launch configuration for an Auto Scaling group, AWS CloudFormation deletes that resource and creates a new launch configuration with the updated properties and a new name\. Existing instances are not affected\. To update existing instances when you update the `AWS::AutoScaling::LaunchConfiguration` resource, you can specify an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for the group\. You can find sample update policies for rolling updates in [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\. 

For more information, see [CreateLaunchConfiguration](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CreateLaunchConfiguration.html) in the *Amazon EC2 Auto Scaling API Reference* and [Launch configurations](https://docs.aws.amazon.com/autoscaling/ec2/userguide/LaunchConfiguration.html) in the *Amazon EC2 Auto Scaling User Guide*\.

**Note**  
To configure Amazon EC2 instances launched as part of the Auto Scaling group, you can specify a launch template or a launch configuration\. We recommend that you use a [launch template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) to make sure that you can use the latest features of Amazon EC2, such as Dedicated Hosts and T2 Unlimited instances\. For more information, see [Creating a launch template for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html)\.

## Syntax<a name="aws-properties-as-launchconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-launchconfig-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::LaunchConfiguration",
  "Properties" : {
      "[AssociatePublicIpAddress](#cf-as-launchconfig-associatepubip)" : Boolean,
      "[BlockDeviceMappings](#cfn-as-launchconfig-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
      "[ClassicLinkVPCId](#cfn-as-launchconfig-classiclinkvpcid)" : String,
      "[ClassicLinkVPCSecurityGroups](#cfn-as-launchconfig-classiclinkvpcsecuritygroups)" : [ String, ... ],
      "[EbsOptimized](#cfn-as-launchconfig-ebsoptimized)" : Boolean,
      "[IamInstanceProfile](#cfn-as-launchconfig-iaminstanceprofile)" : String,
      "[ImageId](#cfn-as-launchconfig-imageid)" : String,
      "[InstanceId](#cfn-as-launchconfig-instanceid)" : String,
      "[InstanceMonitoring](#cfn-as-launchconfig-instancemonitoring)" : Boolean,
      "[InstanceType](#cfn-as-launchconfig-instancetype)" : String,
      "[KernelId](#cfn-as-launchconfig-kernelid)" : String,
      "[KeyName](#cfn-as-launchconfig-keyname)" : String,
      "[LaunchConfigurationName](#cfn-autoscaling-launchconfig-launchconfigurationname)" : String,
      "[MetadataOptions](#cfn-autoscaling-launchconfig-metadataoptions)" : MetadataOptions,
      "[PlacementTenancy](#cfn-as-launchconfig-placementtenancy)" : String,
      "[RamDiskId](#cfn-as-launchconfig-ramdiskid)" : String,
      "[SecurityGroups](#cfn-as-launchconfig-securitygroups)" : [ String, ... ],
      "[SpotPrice](#cfn-as-launchconfig-spotprice)" : String,
      "[UserData](#cfn-as-launchconfig-userdata)" : String
    }
}
```

### YAML<a name="aws-properties-as-launchconfig-syntax.yaml"></a>

```
Type: AWS::AutoScaling::LaunchConfiguration
Properties: 
  [AssociatePublicIpAddress](#cf-as-launchconfig-associatepubip): Boolean
  [BlockDeviceMappings](#cfn-as-launchconfig-blockdevicemappings): 
    - BlockDeviceMapping
  [ClassicLinkVPCId](#cfn-as-launchconfig-classiclinkvpcid): String
  [ClassicLinkVPCSecurityGroups](#cfn-as-launchconfig-classiclinkvpcsecuritygroups): 
    - String
  [EbsOptimized](#cfn-as-launchconfig-ebsoptimized): Boolean
  [IamInstanceProfile](#cfn-as-launchconfig-iaminstanceprofile): String
  [ImageId](#cfn-as-launchconfig-imageid): String
  [InstanceId](#cfn-as-launchconfig-instanceid): String
  [InstanceMonitoring](#cfn-as-launchconfig-instancemonitoring): Boolean
  [InstanceType](#cfn-as-launchconfig-instancetype): String
  [KernelId](#cfn-as-launchconfig-kernelid): String
  [KeyName](#cfn-as-launchconfig-keyname): String
  [LaunchConfigurationName](#cfn-autoscaling-launchconfig-launchconfigurationname): String
  [MetadataOptions](#cfn-autoscaling-launchconfig-metadataoptions): 
    MetadataOptions
  [PlacementTenancy](#cfn-as-launchconfig-placementtenancy): String
  [RamDiskId](#cfn-as-launchconfig-ramdiskid): String
  [SecurityGroups](#cfn-as-launchconfig-securitygroups): 
    - String
  [SpotPrice](#cfn-as-launchconfig-spotprice): String
  [UserData](#cfn-as-launchconfig-userdata): String
```

## Properties<a name="aws-properties-as-launchconfig-properties"></a>

`AssociatePublicIpAddress`  <a name="cf-as-launchconfig-associatepubip"></a>
For Auto Scaling groups that are running in a virtual private cloud \(VPC\), specifies whether to assign a public IP address to the group's instances\. If you specify `true`, each instance in the Auto Scaling group receives a unique public IP address\. For more information, see [Launching Auto Scaling instances in a VPC](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-in-vpc.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
If an instance receives a public IP address and is also in a VPC that is defined in the same stack template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the [VPC\-gateway attachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-gateway-attachment.html)\.   
If the instance is launched into a default subnet, the default is to assign a public IP address, unless you disabled the option to assign a public IP address on the subnet\. If the instance is launched into a nondefault subnet, the default is not to assign a public IP address, unless you enabled the option to assign a public IP address on the subnet\. 
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BlockDeviceMappings`  <a name="cfn-as-launchconfig-blockdevicemappings"></a>
Specifies how block devices are exposed to the instance\. You can specify virtual devices and EBS volumes\.   
*Required*: No  
*Type*: List of [BlockDeviceMapping](aws-properties-as-launchconfig-blockdev-mapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClassicLinkVPCId`  <a name="cfn-as-launchconfig-classiclinkvpcid"></a>
The ID of a ClassicLink\-enabled VPC to link your EC2\-Classic instances to\.   
For more information, see [ClassicLink](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/vpc-classiclink.html) in the *Amazon EC2 User Guide for Linux Instances* and [Linking EC2\-Classic instances to a VPC](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-in-vpc.html#as-ClassicLink) in the *Amazon EC2 Auto Scaling User Guide*\.  
This property can only be used if you are launching EC2\-Classic instances\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClassicLinkVPCSecurityGroups`  <a name="cfn-as-launchconfig-classiclinkvpcsecuritygroups"></a>
The IDs of one or more security groups for the VPC that you specified in the `ClassicLinkVPCId` property\.   
If you specify the `ClassicLinkVPCId` property, you must specify this property\.   
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsOptimized`  <a name="cfn-as-launchconfig-ebsoptimized"></a>
Specifies whether the launch configuration is optimized for EBS I/O \(`true`\) or not \(`false`\)\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal EBS I/O performance\. Additional fees are incurred when you enable EBS optimization for an instance type that is not EBS\-optimized by default\. For more information, see [Amazon EBS–optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.   
The default value is `false`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamInstanceProfile`  <a name="cfn-as-launchconfig-iaminstanceprofile"></a>
Provides the name or the Amazon Resource Name \(ARN\) of the instance profile associated with the IAM role for the instance\. The instance profile contains the IAM role\.   
For more information, see [IAM role for applications that run on Amazon EC2 instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/us-iam-role.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageId`  <a name="cfn-as-launchconfig-imageid"></a>
Provides the unique ID of the Amazon Machine Image \(AMI\) that was assigned during registration\. For more information, see [Finding a Linux AMI](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/finding-an-ami.html) in the *Amazon EC2 User Guide for Linux Instances*\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceId`  <a name="cfn-as-launchconfig-instanceid"></a>
The ID of the Amazon EC2 instance you want to use to create the launch configuration\. Use this property if you want the launch configuration to use settings from an existing Amazon EC2 instance\. When you use an instance to create a launch configuration, all properties are derived from the instance with the exception of `BlockDeviceMapping` and `AssociatePublicIpAddress`\. You can override any properties from the instance by specifying them in the launch configuration\.   
  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceMonitoring`  <a name="cfn-as-launchconfig-instancemonitoring"></a>
Controls whether instances in this group are launched with detailed \(`true`\) or basic \(`false`\) monitoring\. The default value is `true` \(enabled\)\.   
When detailed monitoring is enabled, Amazon CloudWatch generates metrics every minute and your account is charged a fee\. When you disable detailed monitoring, CloudWatch generates metrics every 5 minutes\. For more information, see [Configure monitoring for Auto Scaling instances](https://docs.aws.amazon.com/autoscaling/latest/userguide/as-instance-monitoring.html#enable-as-instance-metrics) in the *Amazon EC2 Auto Scaling User Guide*\. 
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-as-launchconfig-instancetype"></a>
Specifies the instance type of the EC2 instance\. For information about available instance types, see [Available instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableInstanceTypes) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KernelId`  <a name="cfn-as-launchconfig-kernelid"></a>
Provides the ID of the kernel associated with the EC2 AMI\.   
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User provided kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyName`  <a name="cfn-as-launchconfig-keyname"></a>
Provides the name of the EC2 key pair\.   
If you do not specify a key pair, you can't connect to the instance unless you choose an AMI that is configured to allow users another way to log in\. For information on creating a key pair, see [Amazon EC2 key pairs and Linux instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) in the *Amazon EC2 User Guide for Linux Instances*\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchConfigurationName`  <a name="cfn-autoscaling-launchconfig-launchconfigurationname"></a>
The name of the launch configuration\. This name must be unique per Region per account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MetadataOptions`  <a name="cfn-autoscaling-launchconfig-metadataoptions"></a>
The metadata options for the instances\. For more information, see [Configuring the Instance Metadata Options](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-config.html#launch-configurations-imds) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: [MetadataOptions](aws-properties-autoscaling-launchconfig-metadataoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlacementTenancy`  <a name="cfn-as-launchconfig-placementtenancy"></a>
The tenancy of the instance, either `default` or `dedicated`\. An instance with `dedicated` tenancy runs on isolated, single\-tenant hardware and can only be launched into a VPC\. You must set the value of this property to `dedicated` if want to launch dedicated instances in a shared tenancy VPC \(a VPC with the instance placement tenancy attribute set to default\)\.   
If you specify this property, you must specify at least one subnet in the `VPCZoneIdentifier` property of the [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource\.  
For more information, see [Configuring instance tenancy with Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-dedicated-instances.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RamDiskId`  <a name="cfn-as-launchconfig-ramdiskid"></a>
The ID of the RAM disk to select\.   
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User provided kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-as-launchconfig-securitygroups"></a>
A list that contains the security groups to assign to the instances in the Auto Scaling group\. The list can contain both the IDs of existing security groups and references to [SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resources created in the template\.  
For more information, see [Security groups for your VPC](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html) in the *Amazon Virtual Private Cloud User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpotPrice`  <a name="cfn-as-launchconfig-spotprice"></a>
The maximum hourly price you are willing to pay for any Spot Instances launched to fulfill the request\. Spot Instances are launched when the price you specify exceeds the current Spot price\. For more information, see [Requesting Spot Instances for fault\-tolerant and flexible applications ](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-launch-spot-instances.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
When you change your maximum price by creating a new launch configuration, running instances will continue to run as long as the maximum price for those running instances is higher than the current Spot price\.
Valid Range: Minimum value of 0\.001  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserData`  <a name="cfn-as-launchconfig-userdata"></a>
The Base64\-encoded user data to make available to the launched EC2 instances\.  
For more information, see [Instance metadata and user data](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Maximum*: `21847`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-properties-as-launchconfig-return-values"></a>

### Ref<a name="aws-properties-as-launchconfig-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-mylaunchconfig-1DDYF1E3B3I`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-properties-as-launchconfig--examples"></a>

The following examples create launch configurations that can be used by an Auto Scaling group to configure Amazon EC2 instances\. 

For more template snippets, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

### Amazon EBS\-backed AMI and defined block device mappings<a name="aws-properties-as-launchconfig--examples--Amazon_EBS-backed_AMI_and_defined_block_device_mappings"></a>

This example shows a launch configuration with a `BlockDeviceMappings` property that lists two devices: a 30 gigabyte EBS root volume mapped to /dev/sda1 and a 100 gigabyte EBS volume mapped to /dev/sdm\. The /dev/sdm volume uses the default EBS volume type based on the region and is not deleted when terminating the instance it is attached to\. 

CloudFormation supports parameters from the AWS Systems Manager Parameter Store\. In this example, the `ImageId` property of the AWS::AutoScaling::LaunchConfiguration references the latest Amazon Linux 2 AMI \(EBS\-backed image\) from the Parameter Store\. For more information, see [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) in the *AWS Systems Manager User Guide* and the blog post [Query for the latest Amazon Linux AMI IDs using AWS Systems Manager Parameter Store](http://aws.amazon.com/blogs/compute/query-for-the-latest-amazon-linux-ami-ids-using-aws-systems-manager-parameter-store/) on the AWS Compute Blog\.

#### JSON<a name="aws-properties-as-launchconfig--examples--Amazon_EBS-backed_AMI_and_defined_block_device_mappings--json"></a>

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
              "VolumeType":"gp2"
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

#### YAML<a name="aws-properties-as-launchconfig--examples--Amazon_EBS-backed_AMI_and_defined_block_device_mappings--yaml"></a>

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
        - Ref: "myEC2SecurityGroup"
      InstanceType: 
        Ref: "InstanceType"
      BlockDeviceMappings: 
        - DeviceName: /dev/sda1
          Ebs: 
            VolumeSize: 30
            VolumeType: "gp2"
        - DeviceName: /dev/sdm
          Ebs: 
            VolumeSize: 100
            DeleteOnTermination: "false"
```

### Instance store\-backed AMI with Spot price and IAM role<a name="aws-properties-as-launchconfig--examples--Instance_store-backed_AMI_with_Spot_price_and_IAM_role"></a>

This example shows a launch configuration that launches Spot Instances in the Auto Scaling group\. This launch configuration will only be active if the current Spot price is less than the price in the template specification \(0\.045\)\. It also demonstrates a launch configuration that uses the `IamInstanceProfile` property\. For an example of a full template, including the definition of, and further references from the [InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html) object referenced here as `RootInstanceProfile`, see [auto\_scaling\_with\_instance\_profile\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/auto_scaling_with_instance_profile.template)\.

In this example, the `ImageId` property of the AWS::AutoScaling::LaunchConfiguration references the latest Amazon Linux AMI \(instance store/S3\-backed image\) from the Parameter Store\. The BlockDeviceMappings property lists a virtual device `ephemeral0` mapped to /dev/sdc\.

#### JSON<a name="aws-properties-as-launchconfig--examples--Instance_store-backed_AMI_with_Spot_price_and_IAM_role--json"></a>

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

#### YAML<a name="aws-properties-as-launchconfig--examples--Instance_store-backed_AMI_with_Spot_price_and_IAM_role--yaml"></a>

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
      SpotPrice: "0.045"
      IamInstanceProfile: !Ref RootInstanceProfile
      BlockDeviceMappings:
      - DeviceName: /dev/sdc
        VirtualName: ephemeral0
```

### Provisioned IOPS EBS\-optimized volume with key\-pair name and user data<a name="aws-properties-as-launchconfig--examples--Provisioned_IOPS_EBS-optimized_volume_with_key-pair_name_and_user_data"></a>

This example demonstrates a launch configuration that configures the `EbsOptmized` property to launch instances with a provisioned IOPS EBS\-optimized volume\. This can increase the performance of your EBS\-backed instances\.

**Note**  
For instances that are not EBS–optimized by default, you must enable EBS optimization to achieve the level of performance described in the [Amazon EBS\-optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) documentation in the *Amazon Elastic Compute Cloud User Guide*\. For current generation instance types, EBS\-optimization is enabled by default at no additional cost\. Enabling EBS optimization for a previous generation instance type that is not EBS\-optimized by default incurs additional fees\.

When you use a launch configuration such as this one, your `m1.large` instances will contain optimized EBS root volumes with the provisioned IOPS settings that you specified in the AMI\. Because you cannot specify the IOPS settings in a launch configuration, the AMI must be configured with a block device mapping that specifies the desired number of IOPS\. The following are key attributes of this EBS\-optimized instance configuration:
+ An instance type of `m1.large` or greater\. This is required for EBS optimization\. This optimization is only available for certain instance types and sizes\.
+ An EBS\-backed AMI with a volume type of `io1` and the number of IOPS you want to provision for the volume\. 
+ The size of the EBS volume must accommodate the IOPS you need\. There is a 50:1 ratio between IOPS and Gibibytes \(GiB\) of storage\.

For more information about IOPS performance with provisioned IOPS volumes, see [Provisioned IOPS SSD \(`io1` and `io2`\) volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html#EBSVolumeTypes_piops) in the *Amazon Elastic Compute Cloud User Guide*\.

For more performance tips, see [Amazon EBS volume performance on Linux instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSPerformance.html) in the *Amazon Elastic Compute Cloud User Guide*\. 



#### JSON<a name="aws-properties-as-launchconfig--examples--Provisioned_IOPS_EBS-optimized_volume_with_key-pair_name_and_user_data--json"></a>

```
{
  "Resources":{
    "myLaunchConfig":{
      "Type":"AWS::AutoScaling::LaunchConfiguration",
      "Properties":{
        "ImageId":"ami-02354e95b39ca8dec",
        "SecurityGroups":[ { "Ref":"myEC2SecurityGroup" }, "myExistingEC2SecurityGroup" ],
        "InstanceType":"m1.large",
        "KeyName":{
          "Ref":"KeyName"
        },
        "UserData": {"Fn::Join": ["", [
          "#!/bin/bash -x\n",
          "/opt/aws/bin/cfn-init -v --stack ", {"Ref": "AWS::StackName"}, " --resource myLaunchConfig ", " --configsets default ", " --region ", {"Ref": "AWS::Region"}, "\n",
          "/opt/aws/bin/cfn-signal -e $? --stack ", {"Ref": "AWS::StackName"}, " --resource myASG ", " --region ", {"Ref": "AWS::Region"}, "\n"
        ]]},
        "EbsOptimized":"true"
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-launchconfig--examples--Provisioned_IOPS_EBS-optimized_volume_with_key-pair_name_and_user_data--yaml"></a>

```
---
Resources:
  myLaunchConfig: 
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties: 
      ImageId: "ami-02354e95b39ca8dec"
      SecurityGroups: 
        - Ref: "myEC2SecurityGroup"
        - myExistingEC2SecurityGroup
      InstanceType: "m1.large"
      KeyName: 
        Ref: "KeyName"
      UserData: !Base64 |
        #!/bin/bash -x
        yum install -y aws-cfn-bootstrap
        /opt/aws/bin/cfn-init -v --stack !Ref 'AWS::StackName' --resource myLaunchConfig --configsets default --region !Ref 'AWS::Region'
        /opt/aws/bin/cfn-signal -e $? --stack !Ref 'AWS::StackName' --resource myASG --region !Ref 'AWS::Region'
      EbsOptimized: "true"
```
# AWS::AutoScaling::LaunchConfiguration<a name="aws-properties-as-launchconfig"></a>

Specifies an Amazon EC2 Auto Scaling launch configuration that can be used by an Auto Scaling group to configure Amazon EC2 instances\. 

**Important**  
When you update a property of the `LaunchConfiguration` resource, AWS CloudFormation deletes that resource and creates a new launch configuration with the updated properties and a new name\. This update action does not deploy any change across the running Amazon EC2 instances in the Auto Scaling group\. In other words, an update simply replaces the `LaunchConfiguration` so that when the Auto Scaling group launches new instances, they will get the updated configuration, but existing instances continue to run with the configuration that they were originally launched with\. This works the same way as if you made similar changes manually to an Auto Scaling group\.   
If you want to update existing instances when you update the `LaunchConfiguration` resource, you must specify an [UpdatePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html) for the `AWS::AutoScaling::AutoScalingGroup` resource\. 

For more information, see [CreateLaunchConfiguration](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CreateLaunchConfiguration.html) in the *Amazon EC2 Auto Scaling API Reference*\. For more information about Amazon EC2 Auto Scaling, see the [Amazon EC2 Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)\. 

## Syntax<a name="aws-properties-as-launchconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-launchconfig-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::LaunchConfiguration",
  "Properties" : {
      "[AssociatePublicIpAddress](#cf-as-launchconfig-associatepubip)" : Boolean,
      "[BlockDeviceMappings](#cfn-as-launchconfig-blockdevicemappings)" : [ [BlockDeviceMapping](aws-properties-as-launchconfig-blockdev-mapping.md), ... ],
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
Properties : 
﻿  [AssociatePublicIpAddress](#cf-as-launchconfig-associatepubip) : Boolean
﻿  [BlockDeviceMappings](#cfn-as-launchconfig-blockdevicemappings) : 
    - [BlockDeviceMapping](aws-properties-as-launchconfig-blockdev-mapping.md)
﻿  [ClassicLinkVPCId](#cfn-as-launchconfig-classiclinkvpcid) : String
﻿  [ClassicLinkVPCSecurityGroups](#cfn-as-launchconfig-classiclinkvpcsecuritygroups) : 
    - String
﻿  [EbsOptimized](#cfn-as-launchconfig-ebsoptimized) : Boolean
﻿  [IamInstanceProfile](#cfn-as-launchconfig-iaminstanceprofile) : String
﻿  [ImageId](#cfn-as-launchconfig-imageid) : String
﻿  [InstanceId](#cfn-as-launchconfig-instanceid) : String
﻿  [InstanceMonitoring](#cfn-as-launchconfig-instancemonitoring) : Boolean
﻿  [InstanceType](#cfn-as-launchconfig-instancetype) : String
﻿  [KernelId](#cfn-as-launchconfig-kernelid) : String
﻿  [KeyName](#cfn-as-launchconfig-keyname) : String
﻿  [LaunchConfigurationName](#cfn-autoscaling-launchconfig-launchconfigurationname) : String
﻿  [PlacementTenancy](#cfn-as-launchconfig-placementtenancy) : String
﻿  [RamDiskId](#cfn-as-launchconfig-ramdiskid) : String
﻿  [SecurityGroups](#cfn-as-launchconfig-securitygroups) : 
    - String
﻿  [SpotPrice](#cfn-as-launchconfig-spotprice) : String
﻿  [UserData](#cfn-as-launchconfig-userdata) : String
```

## Properties<a name="aws-properties-as-launchconfig-properties"></a>

`AssociatePublicIpAddress`  <a name="cf-as-launchconfig-associatepubip"></a>
Used for groups that launch instances into a virtual private cloud \(VPC\)\. Specifies whether to assign a public IP address to each instance\. If you specify `true`, each instance in the Auto Scaling group receives a unique public IP address\.   
For more information, see [Launching Auto Scaling Instances in a VPC](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-in-vpc.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
Default: If the instance is launched into a default subnet, the default is to assign a public IP address\. If the instance is launched into a nondefault subnet, the default is not to assign a public IP address\.   
If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the VPC\-gateway attachment\.
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
For more information, see [ClassicLink](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/vpc-classiclink.html) in the *Amazon EC2 User Guide for Linux Instances* and [Linking EC2\-Classic Instances to a VPC](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-in-vpc.html#as-ClassicLink) in the *Amazon EC2 Auto Scaling User Guide*\.  
This property can only be used if you are launching EC2\-Classic instances\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClassicLinkVPCSecurityGroups`  <a name="cfn-as-launchconfig-classiclinkvpcsecuritygroups"></a>
The IDs of one or more security groups for the VPC that you specified in the `ClassicLinkVPCId` property\.   
If you specify the `ClassicLinkVPCId` property, you must specify this property\.   
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsOptimized`  <a name="cfn-as-launchconfig-ebsoptimized"></a>
Specifies whether the launch configuration is optimized for EBS I/O \(`true`\) or not \(`false`\)\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal EBS I/O performance\.   
Additional fees are incurred when using EBS\-optimized instances\. For more information about fees and supported instance types, see [EBS\-Optimized Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.   
If this property is not specified, `false` is used\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamInstanceProfile`  <a name="cfn-as-launchconfig-iaminstanceprofile"></a>
Provides the name or the Amazon Resource Name \(ARN\) of the instance profile associated with the IAM role for the instance\. The instance profile contains the IAM role\.   
For more information, see [IAM Role for Applications that Run on Amazon EC2 Instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/us-iam-role.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageId`  <a name="cfn-as-launchconfig-imageid"></a>
Provides the unique ID of the Amazon Machine Image \(AMI\) that was assigned during registration\. For more information, see [Finding an AMI](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/finding-an-ami.html) in the *Amazon EC2 User Guide for Linux Instances*\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceId`  <a name="cfn-as-launchconfig-instanceid"></a>
The ID of the Amazon EC2 instance you want to use to create the launch configuration\. Use this property if you want the launch configuration to use settings from an existing Amazon EC2 instance\.   
When you use an instance to create a launch configuration, all properties are derived from the instance with the exception of `BlockDeviceMapping` and `AssociatePublicIpAddress`\. You can override any properties from the instance by specifying them in the launch configuration\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceMonitoring`  <a name="cfn-as-launchconfig-instancemonitoring"></a>
Controls whether instances in this group are launched with detailed \(`true`\) or basic \(`false`\) monitoring\. The default value is `true` \(enabled\)\.   
When detailed monitoring is enabled, Amazon CloudWatch generates metrics every minute and your account is charged a fee\. When you disable detailed monitoring, CloudWatch generates metrics every 5 minutes\. For more information, see [Configure Monitoring for Auto Scaling Instances](https://docs.aws.amazon.com/autoscaling/latest/userguide/as-instance-monitoring.html#enable-as-instance-metrics) in the *Amazon EC2 Auto Scaling User Guide*\. 
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-as-launchconfig-instancetype"></a>
Specifies the instance type of the EC2 instance\. For information about available instance types, see [Available Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableInstanceTypes) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KernelId`  <a name="cfn-as-launchconfig-kernelid"></a>
Provides the ID of the kernel associated with the EC2 AMI\.   
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User Provided Kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyName`  <a name="cfn-as-launchconfig-keyname"></a>
 Provides the name of the EC2 key pair\.   
If you do not specify a key pair, you can't connect to the instance unless you choose an AMI that is configured to allow users another way to log in\. For information on creating a key pair, see [Amazon EC2 Key Pairs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) in the *Amazon EC2 User Guide for Linux Instances*\. 
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchConfigurationName`  <a name="cfn-autoscaling-launchconfig-launchconfigurationname"></a>
The name of the launch configuration\. This name must be unique per Region per account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlacementTenancy`  <a name="cfn-as-launchconfig-placementtenancy"></a>
The tenancy of the instance, either `default` or `dedicated`\. An instance with `dedicated` tenancy runs in an isolated, single\-tenant hardware and can only be launched into a VPC\. You must set the value of this property to `dedicated` if want to launch dedicated instances in a shared tenancy VPC \(a VPC with the instance placement tenancy attribute set to default\)\.   
If you specify this property, you must specify at least one subnet in the `VPCZoneIdentifier` property of [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)\.   
For more information, see [Instance Placement Tenancy](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-in-vpc.html#as-vpc-tenancy) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RamDiskId`  <a name="cfn-as-launchconfig-ramdiskid"></a>
The ID of the RAM disk to select\.   
We recommend that you use PV\-GRUB instead of kernels and RAM disks\. For more information, see [User Provided Kernels](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UserProvidedKernels.html) in the *Amazon EC2 User Guide for Linux Instances*\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-as-launchconfig-securitygroups"></a>
A list that contains the EC2 security groups to assign to the instances in the Auto Scaling group\. The list can contain the IDs of existing EC2 security groups or references to [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resources created in the template\.   
For more information, see [Security Groups for Your VPC](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html) in the *Amazon Virtual Private Cloud User Guide*\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpotPrice`  <a name="cfn-as-launchconfig-spotprice"></a>
The maximum hourly price to be paid for any Spot Instance launched to fulfill the request\. Spot Instances are launched when the price you specify exceeds the current Spot market price\. For more information, see [Launching Spot Instances in your Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-launch-spot-instances.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
If a Spot price is set, then the Auto Scaling group will only launch when the Spot price has been met, regardless of the setting in the Auto Scaling group's `DesiredCapacity`\.   
When you change your Spot price by creating a new launch configuration, running instances will continue to run as long as the Spot price for those running instances is higher than the current Spot market price\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserData`  <a name="cfn-as-launchconfig-userdata"></a>
The user data available to the launched EC2 instances\.   
For more information, see [Instance Metadata and User Data](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Maximum*: `21847`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-properties-as-launchconfig-return-values"></a>

### Ref<a name="aws-properties-as-launchconfig-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mystack-mylaunchconfig-1DDYF1E3B3I`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-properties-as-launchconfig--examples"></a>

The following examples create launch configurations that can be used by an Auto Scaling group to configure Amazon EC2 instances\. 

### Launch Configuration with Block Device Mappings<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_Block_Device_Mappings"></a>

This example shows a launch configuration with a `BlockDeviceMappings` property that lists two devices: a 50 gigabyte EBS root volume mapped to /dev/sda1 and a 100 gigabyte EBS volume mapped to /dev/sdm\. The /dev/sdm volume uses the default EBS volume type based on the region and is not deleted when terminating the instance it is attached to\. 

#### JSON<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_Block_Device_Mappings--json"></a>

```
{
  "myLaunchConfig":{
    "Type":"AWS::AutoScaling::LaunchConfiguration",
    "Properties":{
      "KeyName":{
        "Ref":"KeyName"
      },
      "ImageId":{
        "Fn::FindInMap":[
          "AWSRegionArch2AMI",
          {
            "Ref":"AWS::Region"
          },
          {
            "Fn::FindInMap":[
              "AWSInstanceType2Arch",
              {
                "Ref":"InstanceType"
              },
              "Arch"
            ]
          }
        ]
      },
      "UserData":{
        "Fn::Base64":{
          "Ref":"WebServerPort"
        }
      },
      "SecurityGroups":[
        {
          "Ref":"InstanceSecurityGroup"
        }
      ],
      "InstanceType":{
        "Ref":"InstanceType"
      },
      "BlockDeviceMappings":[
        {
          "DeviceName":"/dev/sda1",
          "Ebs":{
            "VolumeSize":"50",
            "VolumeType":"io1",
            "Iops":200
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
```

#### YAML<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_Block_Device_Mappings--yaml"></a>

```
myLaunchConfig: 
  Type: AWS::AutoScaling::LaunchConfiguration
  Properties: 
    KeyName: 
      Ref: "KeyName"
    ImageId: 
      Fn::FindInMap: 
        - "AWSRegionArch2AMI"
        - Ref: "AWS::Region"
        - Fn::FindInMap: 
            - "AWSInstanceType2Arch"
            - Ref: "InstanceType"
            - "Arch"
    UserData: 
      Fn::Base64: 
        Ref: "WebServerPort"
    SecurityGroups: 
      - Ref: "InstanceSecurityGroup"
    InstanceType: 
      Ref: "InstanceType"
    BlockDeviceMappings: 
      - DeviceName: "/dev/sda1"
        Ebs: 
          VolumeSize: "50"
          VolumeType: "io1"
          Iops: 200
      - DeviceName: "/dev/sdm"
        Ebs: 
          VolumeSize: "100"
          DeleteOnTermination: "false"
```

### Launch Configuration with Spot Price<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_Spot_Price"></a>

This example shows a launch configuration that launches Spot Instances in the Auto Scaling group\. This launch configuration will only be active if the current Spot market price is less than the price in the template specification \(0\.05\)\.

#### JSON<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_Spot_Price--json"></a>

```
{
  "myLaunchConfig":{
    "Type":"AWS::AutoScaling::LaunchConfiguration",
    "Properties":{
      "KeyName":{
        "Ref":"KeyName"
      },
      "ImageId":{
        "Fn::FindInMap":[
          "AWSRegionArch2AMI",
          {
            "Ref":"AWS::Region"
          },
          {
            "Fn::FindInMap":[
              "AWSInstanceType2Arch",
              {
                "Ref":"InstanceType"
              },
              "Arch"
            ]
          }
        ]
      },
      "SecurityGroups":[
        {
          "Ref":"InstanceSecurityGroup"
        }
      ],
      "SpotPrice":"0.05",
      "InstanceType":{
        "Ref":"InstanceType"
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_Spot_Price--yaml"></a>

```
myLaunchConfig: 
  Type: AWS::AutoScaling::LaunchConfiguration
  Properties: 
    KeyName: 
      Ref: "KeyName"
    ImageId: 
      Fn::FindInMap: 
        - "AWSRegionArch2AMI"
        - Ref: "AWS::Region"
        - Fn::FindInMap: 
            - "AWSInstanceType2Arch"
            - Ref: "InstanceType"
            - "Arch"
    SecurityGroups: 
      - Ref: "InstanceSecurityGroup"
    SpotPrice: "0.05"
    InstanceType: 
      Ref: "InstanceType"
```

### Launch Configuration with IAM Instance Profile<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_IAM_Instance_Profile"></a>

This example demonstrates a launch configuration that uses the `IamInstanceProfile` property\. Only the `AWS::AutoScaling::LaunchConfiguration` specification is shown\. For an example of the full template, including the definition of, and further references from the [AWS::IAM::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html) object referenced here as `RootInstanceProfile`, see [auto\_scaling\_with\_instance\_profile\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/auto_scaling_with_instance_profile.template)\.

#### JSON<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_IAM_Instance_Profile--json"></a>

```
{
  "myLaunchConfig":{
    "Type":"AWS::AutoScaling::LaunchConfiguration",
    "Properties":{
      "ImageId":{
        "Fn::FindInMap":[
          "AWSRegionArch2AMI",
          {
            "Ref":"AWS::Region"
          },
          {
            "Fn::FindInMap":[
              "AWSInstanceType2Arch",
              {
                "Ref":"InstanceType"
              },
              "Arch"
            ]
          }
        ]
      },
      "InstanceType":{
        "Ref":"InstanceType"
      },
      "IamInstanceProfile":{
        "Ref":"RootInstanceProfile"
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-launchconfig--examples--Launch_Configuration_with_IAM_Instance_Profile--yaml"></a>

```
myLaunchConfig: 
  Type: AWS::AutoScaling::LaunchConfiguration
  Properties: 
    ImageId: 
      Fn::FindInMap: 
        - "AWSRegionArch2AMI"
        - Ref: "AWS::Region"
        - Fn::FindInMap: 
            - "AWSInstanceType2Arch"
            - Ref: "InstanceType"
            - "Arch"
    InstanceType: 
      Ref: "InstanceType"
    IamInstanceProfile: 
      Ref: "RootInstanceProfile"
```

### EBS\-Optimized Volume with Specified PIOPS<a name="aws-properties-as-launchconfig--examples--EBS-Optimized_Volume_with_Specified_PIOPS"></a>

You can create an AWS CloudFormation stack with Auto Scaling instances that contain EBS\-optimized volumes with a specified PIOPS\. This can increase the performance of your EBS\-backed instances as explained in [Amazon EBS Volume Performance on Linux Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSPerformance.html) in the *Amazon Elastic Compute Cloud User Guide*\.

When you create a launch configuration such as this one, be sure to set the `InstanceType` to at least `m1.large` and set `EbsOptimized` to `true`\. Your launched instances will contain optimized EBS root volumes with the PIOPS that you selected when creating the AMI\.

**Important**  
Additional fees are incurred when using EBS\-optimized instances\. For more information, see [Amazon EBS\-Optimized Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon Elastic Compute Cloud User Guide*\.

Because you cannot override PIOPS settings in a launch configuration, the AMI in your launch configuration must have been configured with a block device mapping that specifies the desired PIOPS\. You can do this by creating your own EC2 AMI with the following characteristics:
+ An instance type of `m1.large` or greater\. This is required for EBS optimization\.
+ An EBS\-backed AMI with a volume type of "io1" and the number of IOPS you want for the Auto Scaling\-launched instances\.
+ The size of the EBS volume must accommodate the IOPS you need\. There is a 10 : 1 ratio between IOPS and Gibibytes \(GiB\) of storage, so for 100 PIOPS, you need at least 10 GiB storage on the root volume\.

Use this AMI in your launch configuration\. For example, an EBS\-optimized AMI with PIOPS that has the AMI ID `ami-7430ba44` would be used in your launch configuration like this:

#### JSON<a name="aws-properties-as-launchconfig--examples--EBS-Optimized_Volume_with_Specified_PIOPS--json"></a>

```
{
  "myLaunchConfig":{
    "Type":"AWS::AutoScaling::LaunchConfiguration",
    "Properties":{
      "KeyName":{
        "Ref":"KeyName"
      },
      "ImageId":"ami-7430ba44",
      "UserData":{
        "Fn::Base64":{
          "Ref":"WebServerPort"
        }
      },
      "SecurityGroups":[
        {
          "Ref":"InstanceSecurityGroup"
        }
      ],
      "InstanceType":"m1.large",
      "EbsOptimized":"true"
    }
  }
}
```

#### YAML<a name="aws-properties-as-launchconfig--examples--EBS-Optimized_Volume_with_Specified_PIOPS--yaml"></a>

```
myLaunchConfig: 
  Type: AWS::AutoScaling::LaunchConfiguration
  Properties: 
    KeyName: 
      Ref: "KeyName"
    ImageId: "ami-7430ba44"
    UserData: 
      Fn::Base64: 
        Ref: "WebServerPort"
    SecurityGroups: 
      - Ref: "InstanceSecurityGroup"
    InstanceType: "m1.large"
    EbsOptimized: "true"
```
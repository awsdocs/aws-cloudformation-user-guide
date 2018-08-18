# AWS::AutoScaling::LaunchConfiguration<a name="aws-properties-as-launchconfig"></a>

Creates an Auto Scaling launch configuration that can be used by an Auto Scaling group to configure Auto Scaling instances\.

**Important**  
When you update a property of the `LaunchConfiguration` resource, AWS CloudFormation deletes that resource and creates a new launch configuration with the updated properties and a new name\. This update action does not deploy any change across the running Amazon EC2 instances in the auto scaling group\. In other words, an update simply replaces the `LaunchConfiguration` so that when the auto scaling group launches new instances, they will get the updated configuration, but existing instances continue to run with the configuration that they were originally launched with\. This works the same way as if you made similar changes manually to an auto scaling group\.  
If you want to update existing instances when you update the `LaunchConfiguration` resource, you must specify an update policy attribute for the `AWS::AutoScaling::AutoScalingGroup` resource\. For more information, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.

**Topics**
+ [Syntax](#aws-resource-autoscaling-launchconfig-syntax)
+ [Properties](#w3ab2c21c10d135c11)
+ [Return Value](#aws-properties-as-launchconfig-ref)
+ [Template Examples](#w3ab2c21c10d135c15)
+ [See Also](#w3ab2c21c10d135c17)

## Syntax<a name="aws-resource-autoscaling-launchconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-launchconfig-syntax.json"></a>

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
      "[PlacementTenancy](#cfn-as-launchconfig-placementtenancy)" : String,
      "[RamDiskId](#cfn-as-launchconfig-ramdiskid)" : String,
      "[SecurityGroups](#cfn-as-launchconfig-securitygroups)" : [ SecurityGroup, ... ],
      "[SpotPrice](#cfn-as-launchconfig-spotprice)" : String,
      "[UserData](#cfn-as-launchconfig-userdata)" : String
   }
}
```

### YAML<a name="aws-resource-autoscaling-launchconfig-syntax.yaml"></a>

```
Type: "AWS::AutoScaling::LaunchConfiguration"
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
  [PlacementTenancy](#cfn-as-launchconfig-placementtenancy): String
  [RamDiskId](#cfn-as-launchconfig-ramdiskid): String
  [SecurityGroups](#cfn-as-launchconfig-securitygroups):
    - SecurityGroup
  [SpotPrice](#cfn-as-launchconfig-spotprice): String
  [UserData](#cfn-as-launchconfig-userdata): String
```

## Properties<a name="w3ab2c21c10d135c11"></a>

`AssociatePublicIpAddress`  <a name="cf-as-launchconfig-associatepubip"></a>
For Amazon EC2 instances in a VPC, indicates whether instances in the Auto Scaling group receive public IP addresses\. If you specify `true`, each instance in the Auto Scaling receives a unique public IP address\.  
If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the `DependsOn` attribute to declare a dependency on the VPC\-gateway attachment\. For more information, see [DependsOn Attribute](aws-attribute-dependson.md)\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`BlockDeviceMappings`  <a name="cfn-as-launchconfig-blockdevicemappings"></a>
Specifies how block devices are exposed to the instance\. You can specify virtual devices and EBS volumes\.  
*Required*: No  
*Type*: A list of [BlockDeviceMappings](aws-properties-as-launchconfig-blockdev-mapping.md)\.  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ClassicLinkVPCId`  <a name="cfn-as-launchconfig-classiclinkvpcid"></a>
The ID of a ClassicLink\-enabled VPC to link your EC2\-Classic instances to\. You can specify this property only for EC2\-Classic instances\. For more information, see [ClassicLink](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/vpc-classiclink.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ClassicLinkVPCSecurityGroups`  <a name="cfn-as-launchconfig-classiclinkvpcsecuritygroups"></a>
The IDs of one or more security groups for the VPC that you specified in the `ClassicLinkVPCId` property\.  
*Required*: Conditional\. If you specified the `ClassicLinkVPCId` property, you must specify this property\.  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EbsOptimized`  <a name="cfn-as-launchconfig-ebsoptimized"></a>
Specifies whether the launch configuration is optimized for EBS I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal EBS I/O performance\.  
Additional fees are incurred when using EBS\-optimized instances\. For more information about fees and supported instance types, see [EBS\-Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No If this property is not specified, "false" is used\.  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`IamInstanceProfile`  <a name="cfn-as-launchconfig-iaminstanceprofile"></a>
Provides the name or the Amazon Resource Name \(ARN\) of the instance profile associated with the IAM role for the instance\. The instance profile contains the IAM role\.  
*Required*: No  
*Type*: String \(1–1600 chars\)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ImageId`  <a name="cfn-as-launchconfig-imageid"></a>
Provides the unique ID of the Amazon Machine Image \(AMI\) that was assigned during registration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceId`  <a name="cfn-as-launchconfig-instanceid"></a>
The ID of the Amazon EC2 instance you want to use to create the launch configuration\. Use this property if you want the launch configuration to use settings from an existing Amazon EC2 instance\.  
When you use an instance to create a launch configuration, all properties are derived from the instance with the exception of `BlockDeviceMapping` and `AssociatePublicIpAddress`\. You can override any properties from the instance by specifying them in the launch configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceMonitoring`  <a name="cfn-as-launchconfig-instancemonitoring"></a>
Indicates whether detailed instance monitoring is enabled for the Auto Scaling group\. By default, this property is set to `true` \(enabled\)\.  
When detailed monitoring is enabled, Amazon CloudWatch \(CloudWatch\) generates metrics every minute and your account is charged a fee\. When you disable detailed monitoring, CloudWatch generates metrics every 5 minutes\. For more information, see [Monitor Your Auto Scaling Groups and Instances Using Amazon CloudWatch](http://docs.aws.amazon.com/autoscaling/latest/userguide/as-instance-monitoring.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceType`  <a name="cfn-as-launchconfig-instancetype"></a>
Specifies the instance type of the EC2 instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KernelId`  <a name="cfn-as-launchconfig-kernelid"></a>
Provides the ID of the kernel associated with the EC2 AMI\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KeyName`  <a name="cfn-as-launchconfig-keyname"></a>
Provides the name of the EC2 key pair\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LaunchConfigurationName`  <a name="cfn-autoscaling-launchconfig-launchconfigurationname"></a>
The name of the launch configuration\. This name must be unique within the scope of your AWS account\.  
Length Constraints: Minimum length of 1\. Maximum length of 255\.  
Pattern: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PlacementTenancy`  <a name="cfn-as-launchconfig-placementtenancy"></a>
The tenancy of the instance\. An instance with a tenancy of `dedicated` runs on single\-tenant hardware and can only be launched in a VPC\. You must set the value of this parameter to `dedicated` if want to launch dedicated instances in a shared tenancy VPC \(a VPC with the instance placement tenancy attribute set to default\)\. For more information, see [CreateLaunchConfiguration](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CreateLaunchConfiguration.html) in the *Amazon EC2 Auto Scaling API Reference*\.  
If you specify this property, you must specify at least one subnet in the VPCZoneIdentifier property of the [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RamDiskId`  <a name="cfn-as-launchconfig-ramdiskid"></a>
The ID of the RAM disk to select\. Some kernels require additional drivers at launch\. Check the kernel requirements for information about whether you need to specify a RAM disk\. To find kernel requirements, refer to the AWS Resource Center and search for the kernel ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SecurityGroups`  <a name="cfn-as-launchconfig-securitygroups"></a>
A list that contains the EC2 security groups to assign to the instances in the Auto Scaling group\. The list can contain the IDs of existing EC2 security groups or references to `AWS::EC2::SecurityGroup` resources created in the template\.  
*Required*: No  
*Type*: A list of security groups\.  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SpotPrice`  <a name="cfn-as-launchconfig-spotprice"></a>
The spot price for this Auto Scaling group\. If a spot price is set, then the Auto Scaling group will launch when the current spot price is less than the amount specified in the template\.  
When you have specified a spot price for an auto scaling group, the group will only launch when the spot price has been met, regardless of the setting in the Auto Scaling group's `DesiredCapacity`\.  
For more information about configuring a spot price for an Auto Scaling group, see [Launching Spot Instances in your Auto Scaling Group](http://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-launch-spot-instances.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
When you change your bid price by creating a new launch configuration, running instances will continue to run as long as the bid price for those running instances is higher than the current Spot price\.

`UserData`  <a name="cfn-as-launchconfig-userdata"></a>
The user data available to the launched EC2 instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-properties-as-launchconfig-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "LaunchConfig" }
```

For the resource with the logical ID `LaunchConfig`, `Ref` will return the Auto Scaling launch configuration name, such as `mystack-mylaunchconfig-1DDYF1E3B3I`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Template Examples<a name="w3ab2c21c10d135c15"></a>

### LaunchConfig with block device<a name="w3ab2c21c10d135c15b2"></a>

This example shows a launch configuration that describes two Amazon Elastic Block Store mappings\.

#### JSON<a name="aws-resource-autoscaling-launchconfig-example1.json"></a>

```
"LaunchConfig" : {
   "Type" : "AWS::AutoScaling::LaunchConfiguration",
   "Properties" : {
      "KeyName" : { "Ref" : "KeyName" },
      "ImageId" : {
         "Fn::FindInMap" : [
            "AWSRegionArch2AMI",
            { "Ref" : "AWS::Region" },
            {
               "Fn::FindInMap" : [
                  "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch"
               ]
            }
         ]
      },
      "UserData" : { "Fn::Base64" : { "Ref" : "WebServerPort" }},
      "SecurityGroups" : [ { "Ref" : "InstanceSecurityGroup" } ],
      "InstanceType" : { "Ref" : "InstanceType" },
      "BlockDeviceMappings" : [
         {
           "DeviceName" : "/dev/sda1",
           "Ebs" : { "VolumeSize" : "50", "VolumeType" : "io1", "Iops" : 200 } 
         },
         {
           "DeviceName" : "/dev/sdm",
           "Ebs" : { "VolumeSize" : "100", "DeleteOnTermination" : "true"}
         }
      ]
   }
}
```

#### YAML<a name="aws-resource-autoscaling-launchconfig-example1.yaml"></a>

```
LaunchConfig: 
  Type: "AWS::AutoScaling::LaunchConfiguration"
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
          DeleteOnTermination: "true"
```

### LaunchConfig with Spot Price in Autoscaling Group<a name="w3ab2c21c10d135c15b4"></a>

This example shows a launch configuration that features a spot price in the AutoScaling group\. This launch configuration will only be active if the current spot price is less than the amount in the template specification \(0\.05\)\.

#### JSON<a name="aws-resource-autoscaling-launchconfig-example2.json"></a>

```
"LaunchConfig" : {
   "Type" : "AWS::AutoScaling::LaunchConfiguration",
   "Properties" : {
      "KeyName" : { "Ref" : "KeyName" },
      "ImageId" : {
         "Fn::FindInMap" : [
            "AWSRegionArch2AMI",
            { "Ref" : "AWS::Region" },
            {
               "Fn::FindInMap" : [
                  "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch"
               ]
            }
         ]
      },
      "SecurityGroups" : [ { "Ref" : "InstanceSecurityGroup" } ],
      "SpotPrice" :  "0.05",
      "InstanceType" : { "Ref" : "InstanceType" }
   }
}
```

#### YAML<a name="aws-resource-autoscaling-launchconfig-example2.yaml"></a>

```
LaunchConfig: 
  Type: "AWS::AutoScaling::LaunchConfiguration"
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

### LaunchConfig with IAM Instance Profile<a name="w3ab2c21c10d135c15b6"></a>

Here's a launch configuration using the [IamInstanceProfile](#cfn-as-launchconfig-iaminstanceprofile) property\.

Only the `AWS::AutoScaling::LaunchConfiguration` specification is shown\. For the full template, including the definition of, and further references from the [AWS::IAM::InstanceProfile](aws-resource-iam-instanceprofile.md) object referenced here as "RootInstanceProfile", see: [auto\_scaling\_with\_instance\_profile\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/auto_scaling_with_instance_profile.template)\.

#### JSON<a name="aws-resource-autoscaling-launchconfig-example3.json"></a>

```
"myLCOne": {
   "Type": "AWS::AutoScaling::LaunchConfiguration",
   "Properties": {
      "ImageId": {
         "Fn::FindInMap": [
            "AWSRegionArch2AMI",
            { "Ref": "AWS::Region" },
            {
               "Fn::FindInMap": [
                  "AWSInstanceType2Arch", { "Ref": "InstanceType" }, "Arch"
               ]
            }
         ]
      },
      "InstanceType": { "Ref": "InstanceType" },
      "IamInstanceProfile": { "Ref": "RootInstanceProfile" }
   }
}
```

#### YAML<a name="aws-resource-autoscaling-launchconfig-example3.yaml"></a>

```
myLCOne: 
  Type: "AWS::AutoScaling::LaunchConfiguration"
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

### EBS\-optimized volume with specified PIOPS<a name="example-ebs-optimized-piops-autoscaling"></a>

You can create an AWS CloudFormation stack with auto scaled instances that contain EBS\-optimized volumes with a specified PIOPS\. This can increase the performance of your EBS\-backed instances as explained in [Increasing EBS Performance](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSPerformance.html) in the *Amazon Elastic Compute Cloud User Guide*\.

When you create a launch configuration such as this one, be sure to set the `InstanceType` to at least `m1.large` and set `EbsOptimized` to `true`\. Your launched instances will contain optimized EBS root volumes with the PIOPS that you selected when creating the AMI\.

**Warning**  
Additional fees are incurred when using EBS\-optimized instances\. For more information, see [ EBS\-Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#EBSOptimized) in the *Amazon Elastic Compute Cloud User Guide*\.

Because you cannot override PIOPS settings in an auto scaling launch configuration, the AMI in your launch configuration must have been configured with a block device mapping that specifies the desired PIOPS\. You can do this by creating your own EC2 AMI with the following characteristics:
+ An instance type of `m1.large` or greater\. This is required for EBS optimization\.
+ An EBS\-backed AMI with a volume type of "io1" and the number of IOPS you want for the Auto Scaling\-launched instances\.
+ The size of the EBS volume must accommodate the IOPS you need\. There is a 10 : 1 ratio between IOPS and Gibibytes \(GiB\) of storage, so for 100 PIOPS, you need at least 10 GiB storage on the root volume\.

Use this AMI in your Auto Scaling launch configuration\. For example, an EBS\-optimized AMI with PIOPS that has the AMI ID `ami-7430ba44` would be used in your launch configuration like this:

#### JSON<a name="aws-resource-autoscaling-launchconfig-example4.json"></a>

```
"LaunchConfig" : {
   "Type" : "AWS::AutoScaling::LaunchConfiguration",
   "Properties" : {
      "KeyName" : { "Ref" : "KeyName" },
      "ImageId" : "ami-7430ba44",
      "UserData" : { "Fn::Base64" : { "Ref" : "WebServerPort" } },
      "SecurityGroups" : [ { "Ref" : "InstanceSecurityGroup" } ],
      "InstanceType" : "m1.large",
      "EbsOptimized" : "true"
   }
}
```

#### YAML<a name="aws-resource-autoscaling-launchconfig-example4.yaml"></a>

```
LaunchConfig: 
  Type: "AWS::AutoScaling::LaunchConfiguration"
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

## See Also<a name="w3ab2c21c10d135c17"></a>
+ [Creating Your Own AMIs](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/creating-an-ami.html) in the *Amazon Elastic Compute Cloud User Guide*\.
+ [Block Device Mapping](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/block-device-mapping-concepts.html) in the *Amazon Elastic Compute Cloud User Guide*\.
+ To view more LaunchConfiguration snippets, see [Auto Scaling Launch Configuration Resource](quickref-autoscaling.md#scenario-as-launch-config)\.
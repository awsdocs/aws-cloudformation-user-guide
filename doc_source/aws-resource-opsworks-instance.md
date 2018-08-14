# AWS::OpsWorks::Instance<a name="aws-resource-opsworks-instance"></a>

Creates an Amazon Elastic Compute Cloud \(Amazon EC2\) instance for an AWS OpsWorks stack\. Instances for AWS OpsWorks stacks handle the work of serving applications and balancing traffic, for example\.

**Topics**
+ [Syntax](#aws-resource-opsworks-instance-syntax)
+ [Properties](#w3ab2c21c10d921b9)
+ [Return Values](#w3ab2c21c10d921c11)
+ [Examples](#w3ab2c21c10d921c13)
+ [More Info](#w3ab2c21c10d921c15)

## Syntax<a name="aws-resource-opsworks-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-instance-syntax.json"></a>

```
{
  "Type": "AWS::OpsWorks::Instance",
  "Properties": {
    "[AgentVersion](#cfn-opsworks-instance-agentversion)" : String,
    "[AmiId](#cfn-opsworks-instance-amiid)" : String,
    "[Architecture](#cfn-opsworks-instance-architecture)" : String,
    "[AutoScalingType](#cfn-opsworks-instance-autoscalingtype)" : String,
    "[AvailabilityZone](#cfn-opsworks-instance-availabilityzone)" : String,
    "[BlockDeviceMappings](#cfn-opsworks-instance-blockdevicemappings)" : [ [BlockDeviceMapping](aws-properties-opsworks-instance-blockdevicemapping.md), ... ],
    "[EbsOptimized](#cfn-opsworks-instance-ebsoptimized)" : Boolean,
    "[ElasticIps](#cfn-opsworks-instance-elasticips)" : [ String, ... ],
    "[Hostname](#cfn-opsworks-instance-hostname)" : String,
    "[InstallUpdatesOnBoot](#cfn-opsworks-instance-installupdatesonboot)" : Boolean,
    "[InstanceType](#cfn-opsworks-instance-instancetype)" : String,
    "[LayerIds](#cfn-opsworks-instance-layerids)" :  [ String, ... ],
    "[Os](#cfn-opsworks-instance-os)" : String,
    "[RootDeviceType](#cfn-opsworks-instance-rootdevicetype)" : String,
    "[SshKeyName](#cfn-opsworks-instance-sshkeyname)" : String,
    "[StackId](#cfn-opsworks-instance-stackid)" : String,
    "[SubnetId](#cfn-opsworks-instance-subnetid)" : String,
    "[Tenancy](#cfn-opsworks-instance-tenancy)" : String,
    "[TimeBasedAutoScaling](#cfn-opsworks-instance-timebasedautoscaling)" : [TimeBasedAutoScaling](aws-properties-opsworks-instance-timebasedautoscaling.md),
    "[VirtualizationType](#cfn-opsworks-instance-virtualizationtype)" : String,
    "[Volumes](#cfn-opsworks-instance-volumes)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-opsworks-instance-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::Instance"
Properties:
  [AgentVersion](#cfn-opsworks-instance-agentversion): String
  [AmiId](#cfn-opsworks-instance-amiid): String
  [Architecture](#cfn-opsworks-instance-architecture): String
  [AutoScalingType](#cfn-opsworks-instance-autoscalingtype): String
  [AvailabilityZone](#cfn-opsworks-instance-availabilityzone): String
  [BlockDeviceMappings](#cfn-opsworks-instance-blockdevicemappings): 
  - [BlockDeviceMapping](aws-properties-opsworks-instance-blockdevicemapping.md)
  [EbsOptimized](#cfn-opsworks-instance-ebsoptimized): Boolean
  [ElasticIps](#cfn-opsworks-instance-elasticips): 
  - String
  [Hostname](#cfn-opsworks-instance-hostname): String
  [InstallUpdatesOnBoot](#cfn-opsworks-instance-installupdatesonboot): Boolean
  [InstanceType](#cfn-opsworks-instance-instancetype): String
  [LayerIds](#cfn-opsworks-instance-layerids): 
  - String
  [Os](#cfn-opsworks-instance-os): String
  [RootDeviceType](#cfn-opsworks-instance-rootdevicetype): String
  [SshKeyName](#cfn-opsworks-instance-sshkeyname): String
  [StackId](#cfn-opsworks-instance-stackid): String
  [SubnetId](#cfn-opsworks-instance-subnetid): String
  [Tenancy](#cfn-opsworks-instance-tenancy): String
  [TimeBasedAutoScaling](#cfn-opsworks-instance-timebasedautoscaling):
  [TimeBasedAutoScaling](aws-properties-opsworks-instance-timebasedautoscaling.md)
  [VirtualizationType](#cfn-opsworks-instance-virtualizationtype): String
  [Volumes](#cfn-opsworks-instance-volumes): 
  - String
```

## Properties<a name="w3ab2c21c10d921b9"></a>

`AgentVersion`  <a name="cfn-opsworks-instance-agentversion"></a>
The version of the AWS OpsWorks agent that AWS OpsWorks installs on each instance\. AWS OpsWorks sends commands to the agent to performs tasks on your instances, such as starting Chef runs\. For valid values, see the `AgentVersion` parameter for the [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) action in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AmiId`  <a name="cfn-opsworks-instance-amiid"></a>
The ID of the custom Amazon Machine Image \(AMI\) to be used to create the instance\. For more information about custom AMIs, see [Using Custom AMIs](http://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-custom-ami.html) in the *AWS OpsWorks User Guide*\.  
If you specify this property, you must set the `Os` property to `Custom`\.
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Architecture`  <a name="cfn-opsworks-instance-architecture"></a>
The instance architecture\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`AutoScalingType`  <a name="cfn-opsworks-instance-autoscalingtype"></a>
For scaling instances, the type of scaling\. If you specify load\-based scaling, do not specify a time\-based scaling configuration\. For valid values, see [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`AvailabilityZone`  <a name="cfn-opsworks-instance-availabilityzone"></a>
The instance Availability Zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`BlockDeviceMappings`  <a name="cfn-opsworks-instance-blockdevicemappings"></a>
A list of block devices that are mapped to the AWS OpsWorks instance\. For more information, see the `BlockDeviceMappings` parameter for the [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) action in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: List of [AWS OpsWorks Instance BlockDeviceMapping](aws-properties-opsworks-instance-blockdevicemapping.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EbsOptimized`  <a name="cfn-opsworks-instance-ebsoptimized"></a>
Whether the instance is optimized for Amazon Elastic Block Store \(Amazon EBS\) I/O\. If you specify an Amazon EBS\-optimized instance type, AWS OpsWorks enables EBS optimization by default\. For more information, see [Amazon EBS–Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ElasticIps`  <a name="cfn-opsworks-instance-elasticips"></a>
A list of Elastic IP addresses to associate with the instance\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Hostname`  <a name="cfn-opsworks-instance-hostname"></a>
The name of the instance host\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstallUpdatesOnBoot`  <a name="cfn-opsworks-instance-installupdatesonboot"></a>
Whether to install operating system and package updates when the instance boots\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`InstanceType`  <a name="cfn-opsworks-instance-instancetype"></a>
The instance type, which must be supported by AWS OpsWorks\. For more information, see [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) in the *AWS OpsWorks Stacks API Reference*\.  
If you specify an Amazon EBS\-optimized instance type, AWS OpsWorks enables EBS optimization by default\. For more information about Amazon EBS\-optimized instance types, see [Amazon EBS–Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`LayerIds`  <a name="cfn-opsworks-instance-layerids"></a>
The IDs of the AWS OpsWorks layers to associate with this instance\.  
*Required*: Yes  
*Type*: List of String values  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`Os`  <a name="cfn-opsworks-instance-os"></a>
The instance operating system\. For more information, see [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RootDeviceType`  <a name="cfn-opsworks-instance-rootdevicetype"></a>
The root device type of the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SshKeyName`  <a name="cfn-opsworks-instance-sshkeyname"></a>
The SSH key name of the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`StackId`  <a name="cfn-opsworks-instance-stackid"></a>
The ID of the AWS OpsWorks stack that this instance will be associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SubnetId`  <a name="cfn-opsworks-instance-subnetid"></a>
The ID of the instance's subnet\. If the stack is running in a VPC, you can use this parameter to override the stack's default subnet ID value and direct AWS OpsWorks to launch the instance in a different subnet\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tenancy`  <a name="cfn-opsworks-instance-tenancy"></a>
The tenancy of the instance\. For more information, see the `Tenancy` parameter for the [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) action in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TimeBasedAutoScaling`  <a name="cfn-opsworks-instance-timebasedautoscaling"></a>
The time\-based scaling configuration for the instance\.  
*Required*: No  
*Type*: [AWS OpsWorks TimeBasedAutoScaling Type](aws-properties-opsworks-instance-timebasedautoscaling.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VirtualizationType`  <a name="cfn-opsworks-instance-virtualizationtype"></a>
The instance's virtualization type, `paravirtual` or `hvm`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Volumes`  <a name="cfn-opsworks-instance-volumes"></a>
A list of AWS OpsWorks volume IDs to associate with the instance\. For more information, see [AWS::OpsWorks::Volume](aws-resource-opsworks-volume.md)\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d921c11"></a>

### Ref<a name="w3ab2c21c10d921c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myInstance1" }
```

For the AWS OpsWorks instance `myInstance1`, `Ref` returns the AWS OpsWorks instance ID\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d921c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.
+ `AvailabilityZone`

  The Availability Zone of the AWS OpsWorks instance, such as `us-east-2a`\.
+ `PrivateDnsName`

  The private DNS name of the AWS OpsWorks instance\.
+ `PrivateIp`

  The private IP address of the AWS OpsWorks instance, such as `192.0.2.0`\.
+ `PublicDnsName`

  The public DNS name of the AWS OpsWorks instance\.
+ `PublicIp`

  The public IP address of the AWS OpsWorks instance, such as `192.0.2.0`\.
**Note**  
Use this attribute only when the AWS OpsWorks instance is in an AWS OpsWorks layer that auto\-assigns public IP addresses\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d921c13"></a>

### Create Basic AWS OpsWorks Instances<a name="w3ab2c21c10d921c13b2"></a>

The following example creates two AWS OpsWorks instances that are associated with the `myStack` AWS OpsWorks stack and the `myLayer` AWS OpsWorks layer:

#### JSON<a name="aws-resource-opsworks-instance-example1.json"></a>

```
"myInstance1" : {
  "Type" : "AWS::OpsWorks::Instance",
  "Properties" : {
    "StackId" : {"Ref":"myStack"},
    "LayerIds" : [{"Ref":"myLayer"}],
    "InstanceType" : "m1.small"
  }
},
 
"myInstance2" : {
  "Type" : "AWS::OpsWorks::Instance",
  "Properties" : {
    "StackId" : {"Ref":"myStack"},
    "LayerIds" : [{"Ref":"myLayer"}],
    "InstanceType" : "m1.small"
  }
}
```

#### YAML<a name="aws-resource-opsworks-instance-example1.yaml"></a>

```
myInstance1: 
  Type: "AWS::OpsWorks::Instance"
  Properties: 
    StackId: 
      Ref: "myStack"
    LayerIds: 
      - 
        Ref: "myLayer"
    InstanceType: "m1.small"
myInstance2: 
  Type: "AWS::OpsWorks::Instance"
  Properties: 
    StackId: 
      Ref: "myStack"
    LayerIds: 
      - 
        Ref: "myLayer"
    InstanceType: "m1.small"
```

### Define a Time\-based Auto Scaling Instance<a name="w3ab2c21c10d921c13b4"></a>

In the following example, the `DBInstance` instance is online for four hours from UTC 1200\-1600 on Friday, Saturday, and Sunday\. The instance is offline for all other times and days\.

#### JSON<a name="aws-resource-opsworks-instance-example2.json"></a>

```
"DBInstance" : {
  "Type" : "AWS::OpsWorks::Instance",
  "Properties" : {
    "AutoScalingType" : "timer",
    "StackId" : {"Ref":"Stack"},
    "LayerIds" : [{"Ref":"DBLayer"}],
    "InstanceType" : "m1.small",
    "TimeBasedAutoScaling" : {
      "Friday" : { "12" : "on", "13" : "on", "14" : "on", "15" : "on" },
      "Saturday" : { "12" : "on", "13" : "on", "14" : "on", "15" : "on" },
      "Sunday" : { "12" : "on", "13" : "on", "14" : "on", "15" : "on" }
    }
  }
}
```

#### YAML<a name="aws-resource-opsworks-instance-example2.yaml"></a>

```
DBInstance: 
  Type: "AWS::OpsWorks::Instance"
  Properties: 
    AutoScalingType: "timer"
    StackId: 
      Ref: "Stack"
    LayerIds: 
      - Ref: "DBLayer"
    InstanceType: "m1.small"
    TimeBasedAutoScaling: 
      Friday: 
        12: "on"
        13: "on"
        14: "on"
        15: "on"
      Saturday: 
        12: "on"
        13: "on"
        14: "on"
        15: "on"
      Sunday: 
        12: "on"
        13: "on"
        14: "on"
        15: "on"
```

## More Info<a name="w3ab2c21c10d921c15"></a>
+ [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)
+ [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)
+ [AWS::OpsWorks::App](aws-resource-opsworks-app.md)
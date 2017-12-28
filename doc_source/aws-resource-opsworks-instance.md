# AWS::OpsWorks::Instance<a name="aws-resource-opsworks-instance"></a>

Creates an Amazon Elastic Compute Cloud \(Amazon EC2\) instance for an AWS OpsWorks stack\. Instances for AWS OpsWorks stacks handle the work of serving applications and balancing traffic, for example\.


+ [Syntax](#aws-resource-opsworks-instance-syntax)
+ [Properties](#w3ab2c21c10d849b9)
+ [Return Values](#w3ab2c21c10d849c11)
+ [Examples](#w3ab2c21c10d849c13)
+ [More Info](#w3ab2c21c10d849c15)

## Syntax<a name="aws-resource-opsworks-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-instance-syntax.json"></a>

```
{
  "Type": "AWS::OpsWorks::Instance",
  "Properties": {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-agentversion)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-amiid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-architecture)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-autoscalingtype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-availabilityzone)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemappings)" : [ BlockDeviceMapping, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-ebsoptimized)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-elasticips)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-hostname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-installupdatesonboot)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-instancetype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-layerids)" :  [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-os)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-rootdevicetype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-sshkeyname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-stackid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-subnetid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-tenancy)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling)" : TimeBasedAutoScaling,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-virtualizationtype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-volumes)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-opsworks-instance-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::Instance"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-agentversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-amiid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-architecture): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-autoscalingtype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-availabilityzone): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemappings): 
  - BlockDeviceMapping
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-ebsoptimized): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-elasticips): 
  - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-hostname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-installupdatesonboot): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-instancetype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-layerids): 
  - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-os): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-rootdevicetype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-sshkeyname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-stackid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-subnetid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-tenancy): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling):
  TimeBasedAutoScaling
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-virtualizationtype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-volumes): 
  - String
```

## Properties<a name="w3ab2c21c10d849b9"></a>

`AgentVersion`  
The version of the AWS OpsWorks agent that AWS OpsWorks installs on each instance\. AWS OpsWorks sends commands to the agent to performs tasks on your instances, such as starting Chef runs\. For valid values, see the `AgentVersion` parameter for the [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) action in the *AWS OpsWorks Stacks API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`AmiId`  
The ID of the custom Amazon Machine Image \(AMI\) to be used to create the instance\. For more information about custom AMIs, see [Using Custom AMIs](http://docs.aws.amazon.com/opsworks/latest/userguide/workinginstances-custom-ami.html) in the *AWS OpsWorks User Guide*\.  
If you specify this property, you must set the `Os` property to `Custom`\.
*Required: *No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Architecture`  
The instance architecture\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`AutoScalingType`  
For scaling instances, the type of scaling\. If you specify load\-based scaling, do not specify a time\-based scaling configuration\. For valid values, see [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`AvailabilityZone`  
The instance Availability Zone\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`BlockDeviceMappings`  
A list of block devices that are mapped to the AWS OpsWorks instance\. For more information, see the `BlockDeviceMappings` parameter for the [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) action in the *AWS OpsWorks Stacks API Reference*\.  
*Required: *No  
*Type*: List of [AWS OpsWorks Instance BlockDeviceMapping](aws-properties-opsworks-instance-blockdevicemapping.md)  
*Update requires*: Replacement

`EbsOptimized`  
Whether the instance is optimized for Amazon Elastic Block Store \(Amazon EBS\) I/O\. If you specify an Amazon EBS\-optimized instance type, AWS OpsWorks enables EBS optimization by default\. For more information, see [Amazon EBS–Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`ElasticIps`  
A list of Elastic IP addresses to associate with the instance\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Hostname`  
The name of the instance host\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`InstallUpdatesOnBoot`  
Whether to install operating system and package updates when the instance boots\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Some interruptions

`InstanceType`  
The instance type, which must be supported by AWS OpsWorks\. For more information, see [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) in the *AWS OpsWorks Stacks API Reference*\.  
If you specify an Amazon EBS\-optimized instance type, AWS OpsWorks enables EBS optimization by default\. For more information about Amazon EBS\-optimized instance types, see [Amazon EBS–Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Some interruptions

`LayerIds`  
The IDs of the AWS OpsWorks layers to associate with this instance\.  
*Required: *Yes  
*Type*: List of String values  
*Update requires*: Some interruptions

`Os`  
The instance operating system\. For more information, see [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`RootDeviceType`  
The root device type of the instance\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`SshKeyName`  
The SSH key name of the instance\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`StackId`  
The ID of the AWS OpsWorks stack that this instance will be associated with\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`SubnetId`  
The ID of the instance's subnet\. If the stack is running in a VPC, you can use this parameter to override the stack's default subnet ID value and direct AWS OpsWorks to launch the instance in a different subnet\.   
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Tenancy`  
The tenancy of the instance\. For more information, see the `Tenancy` parameter for the [CreateInstance](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateInstance.html) action in the *AWS OpsWorks Stacks API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`TimeBasedAutoScaling`  
The time\-based scaling configuration for the instance\.  
*Required: *No  
*Type*: [AWS OpsWorks TimeBasedAutoScaling Type](aws-properties-opsworks-instance-timebasedautoscaling.md)  
*Update requires*: Replacement

`VirtualizationType`  
The instance's virtualization type, `paravirtual` or `hvm`\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Volumes`  
A list of AWS OpsWorks volume IDs to associate with the instance\. For more information, see [AWS::OpsWorks::Volume](aws-resource-opsworks-volume.md)\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

## Return Values<a name="w3ab2c21c10d849c11"></a>

### Ref<a name="w3ab2c21c10d849c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myInstance1" }
```

For the AWS OpsWorks instance `myInstance1`, `Ref` returns the AWS OpsWorks instance ID\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d849c11b4"></a>

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

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Examples<a name="w3ab2c21c10d849c13"></a>

### Create Basic AWS OpsWorks Instances<a name="w3ab2c21c10d849c13b2"></a>

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

### Define a Time\-based Auto Scaling Instance<a name="w3ab2c21c10d849c13b4"></a>

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

## More Info<a name="w3ab2c21c10d849c15"></a>

+ [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)

+ [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)

+ [AWS::OpsWorks::App](aws-resource-opsworks-app.md)
# AWS::AutoScaling::AutoScalingGroup MemoryMiBRequest<a name="aws-properties-autoscaling-autoscalinggroup-memorymibrequest"></a>

`MemoryMiBRequest` is a property of the `InstanceRequirements` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property type that describes the minimum and maximum instance memory size for an instance type, in MiB\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-memorymibrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-memorymibrequest-syntax.json"></a>

```
{
  "[Max](#cfn-autoscaling-autoscalinggroup-memorymibrequest-max)" : Integer,
  "[Min](#cfn-autoscaling-autoscalinggroup-memorymibrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-memorymibrequest-syntax.yaml"></a>

```
  [Max](#cfn-autoscaling-autoscalinggroup-memorymibrequest-max): Integer
  [Min](#cfn-autoscaling-autoscalinggroup-memorymibrequest-min): Integer
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-memorymibrequest-properties"></a>

`Max`  <a name="cfn-autoscaling-autoscalinggroup-memorymibrequest-max"></a>
The memory maximum in MiB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-autoscaling-autoscalinggroup-memorymibrequest-min"></a>
The memory minimum in MiB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
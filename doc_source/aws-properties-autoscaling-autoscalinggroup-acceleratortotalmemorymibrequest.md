# AWS::AutoScaling::AutoScalingGroup AcceleratorTotalMemoryMiBRequest<a name="aws-properties-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest"></a>

`AcceleratorTotalMemoryMiBRequest` is a property of the `InstanceRequirements` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property type that describes the minimum and maximum total memory size for the accelerators for an instance type, in MiB\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-syntax.json"></a>

```
{
  "[Max](#cfn-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-max)" : Integer,
  "[Min](#cfn-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-syntax.yaml"></a>

```
  [Max](#cfn-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-max): Integer
  [Min](#cfn-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-min): Integer
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-properties"></a>

`Max`  <a name="cfn-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-max"></a>
The memory maximum in MiB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-autoscaling-autoscalinggroup-acceleratortotalmemorymibrequest-min"></a>
The memory minimum in MiB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
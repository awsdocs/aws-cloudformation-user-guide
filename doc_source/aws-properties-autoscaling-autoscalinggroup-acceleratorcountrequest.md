# AWS::AutoScaling::AutoScalingGroup AcceleratorCountRequest<a name="aws-properties-autoscaling-autoscalinggroup-acceleratorcountrequest"></a>

`AcceleratorCountRequest` is a property of the `InstanceRequirements` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property type that describes the minimum and maximum number of accelerators for an instance type\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-acceleratorcountrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-acceleratorcountrequest-syntax.json"></a>

```
{
  "[Max](#cfn-autoscaling-autoscalinggroup-acceleratorcountrequest-max)" : Integer,
  "[Min](#cfn-autoscaling-autoscalinggroup-acceleratorcountrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-acceleratorcountrequest-syntax.yaml"></a>

```
  [Max](#cfn-autoscaling-autoscalinggroup-acceleratorcountrequest-max): Integer
  [Min](#cfn-autoscaling-autoscalinggroup-acceleratorcountrequest-min): Integer
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-acceleratorcountrequest-properties"></a>

`Max`  <a name="cfn-autoscaling-autoscalinggroup-acceleratorcountrequest-max"></a>
The maximum value\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-autoscaling-autoscalinggroup-acceleratorcountrequest-min"></a>
The minimum value\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
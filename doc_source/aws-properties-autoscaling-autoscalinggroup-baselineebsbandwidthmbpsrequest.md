# AWS::AutoScaling::AutoScalingGroup BaselineEbsBandwidthMbpsRequest<a name="aws-properties-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest"></a>

`BaselineEbsBandwidthMbpsRequest` is a property of the `InstanceRequirements` property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property type that describes the minimum and maximum baseline bandwidth performance for an instance type, in Mbps\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-syntax.json"></a>

```
{
  "[Max](#cfn-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-max)" : Integer,
  "[Min](#cfn-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-syntax.yaml"></a>

```
  [Max](#cfn-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-max): Integer
  [Min](#cfn-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-min): Integer
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-properties"></a>

`Max`  <a name="cfn-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-max"></a>
The maximum value in Mbps\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-autoscaling-autoscalinggroup-baselineebsbandwidthmbpsrequest-min"></a>
The minimum value in Mbps\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# Amazon EC2 Auto Scaling AutoScalingGroup LaunchTemplateOverrides<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides"></a>

<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-description"></a>The `LaunchTemplateOverrides` property type describes an override for a launch template\.

<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-inheritance"></a> `LaunchTemplateOverrides` is a property of the [LaunchTemplate](aws-properties-autoscaling-autoscalinggroup-launchtemplate.md) property type\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.json"></a>

```
{
  "[InstanceType](#cfn-as-mixedinstancespolicy-instancetype)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.yaml"></a>

```
[InstanceType](#cfn-as-mixedinstancespolicy-instancetype): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-properties"></a>

`InstanceType`  <a name="cfn-as-mixedinstancespolicy-instancetype"></a>
The instance type\.  
For information about available instance types, see [Available Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableInstanceTypes) in the *Amazon EC2 User Guide for Linux Instances\.*  
*Required*: No  
*Type*: String  
*Length constraints*: Minimum length of 1\. Maximum length of 255\.  
Pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## See Also<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-seealso"></a>
+ [LaunchTemplateOverrides](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_LaunchTemplateOverrides.html) in the *Amazon EC2 Auto Scaling API Reference*
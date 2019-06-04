# AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides"></a>

 `LaunchTemplateOverrides` is a subproperty of [LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html) that describes an override for a launch template\. 

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.json"></a>

```
{
  "[InstanceType](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.yaml"></a>

```
  [InstanceType](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-properties"></a>

`InstanceType`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype"></a>
The instance type\. For more information, see [Available Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableInstanceTypes) in the *Amazon EC2 User Guide for Linux Instances\.*   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
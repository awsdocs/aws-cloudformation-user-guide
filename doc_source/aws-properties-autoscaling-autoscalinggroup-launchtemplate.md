# Amazon EC2 Auto Scaling AutoScalingGroup LaunchTemplate<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate"></a>

<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-description"></a>The `LaunchTemplate` property type describes a launch template and overrides\.

The overrides are used to override the instance type specified by the launch template with multiple instance types that can be used to launch On\-Demand Instances and Spot Instances\.

<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-inheritance"></a> `LaunchTemplate` is a property of the [MixedInstancesPolicy](aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.md) property type\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-syntax.json"></a>

```
{
  "[LaunchTemplateSpecification](#cfn-as-group-mixedinstancespolicy-launchtemplate)" : [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md),
  "[Overrides](#cfn-as-mixedinstancespolicy-overrides)" : [ [LaunchTemplateOverrides](aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.md), ... ]
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-syntax.yaml"></a>

```
[LaunchTemplateSpecification](#cfn-as-group-mixedinstancespolicy-launchtemplate): 
  [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)
[Overrides](#cfn-as-mixedinstancespolicy-overrides): 
  - [LaunchTemplateOverrides](aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.md)
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-properties"></a>

`LaunchTemplateSpecification`  <a name="cfn-as-group-mixedinstancespolicy-launchtemplate"></a>
The launch template to use\. You must specify either the launch template ID or launch template name in the request\.  
*Required*: Yes  
*Type*: [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Overrides`  <a name="cfn-as-mixedinstancespolicy-overrides"></a>
Any parameters that you specify override the same parameters in the launch template\. Currently, the only supported override is instance type\.  
You must specify between 2 and 20 overrides\.  
*Required*: Yes  
*Type*: List of [LaunchTemplateOverrides](aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-seealso"></a>
+ [LaunchTemplate](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_LaunchTemplate.html) in the *Amazon EC2 Auto Scaling API Reference*
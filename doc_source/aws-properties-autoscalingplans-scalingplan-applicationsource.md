# AWS Auto Scaling ScalingPlan ApplicationSource<a name="aws-properties-autoscalingplans-scalingplan-applicationsource"></a>

<a name="aws-properties-autoscalingplans-scalingplan-applicationsource-description"></a>The `ApplicationSource` property type specifies the application source for an AWS Auto Scaling scaling plan\. You can create one scaling plan per application source\.

<a name="aws-properties-autoscalingplans-scalingplan-applicationsource-inheritance"></a> `ApplicationSource` is a property of the [AWS::AutoScalingPlans::ScalingPlan](aws-resource-autoscalingplans-scalingplan.md) resource\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-applicationsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-applicationsource-syntax.json"></a>

```
{
  "[CloudFormationStackARN](#cfn-autoscalingplans-scalingplan-applicationsource-cloudformationstackarn)" : String,
  "[TagFilters](#cfn-autoscalingplans-scalingplan-applicationsource-tagfilters)" : [ [*TagFilter*](aws-properties-autoscalingplans-scalingplan-tagfilter.md), ... ]
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-applicationsource-syntax.yaml"></a>

```
[CloudFormationStackARN](#cfn-autoscalingplans-scalingplan-applicationsource-cloudformationstackarn): String
[TagFilters](#cfn-autoscalingplans-scalingplan-applicationsource-tagfilters): 
  - [*TagFilter*](aws-properties-autoscalingplans-scalingplan-tagfilter.md)
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-applicationsource-properties"></a>

`CloudFormationStackARN`  <a name="cfn-autoscalingplans-scalingplan-applicationsource-cloudformationstackarn"></a>
The Amazon Resource Name \(ARN\) of a CloudFormation stack\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TagFilters`  <a name="cfn-autoscalingplans-scalingplan-applicationsource-tagfilters"></a>
A set of tags \(up to 50\)\.  
 *Required*: No  
 *Type*: List of [AWS Auto Scaling ScalingPlan TagFilter](aws-properties-autoscalingplans-scalingplan-tagfilter.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
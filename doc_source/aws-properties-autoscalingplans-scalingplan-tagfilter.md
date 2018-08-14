# AWS Auto Scaling ScalingPlan TagFilter<a name="aws-properties-autoscalingplans-scalingplan-tagfilter"></a>

<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-description"></a>The `TagFilter` property type specifies a tag for an application source for an AWS Auto Scaling scaling plan\.

<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-inheritance"></a> `TagFilter` is a property of the [AWS Auto Scaling ScalingPlan ApplicationSource](aws-properties-autoscalingplans-scalingplan-applicationsource.md) property type\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-syntax.json"></a>

```
{
  "[Values](#cfn-autoscalingplans-scalingplan-tagfilter-values)" : [ String, ... ],
  "[Key](#cfn-autoscalingplans-scalingplan-tagfilter-key)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-syntax.yaml"></a>

```
[Values](#cfn-autoscalingplans-scalingplan-tagfilter-values): 
  - String
[Key](#cfn-autoscalingplans-scalingplan-tagfilter-key): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-properties"></a>

`Key`  <a name="cfn-autoscalingplans-scalingplan-tagfilter-key"></a>
The tag key\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Values`  <a name="cfn-autoscalingplans-scalingplan-tagfilter-values"></a>
The tag values \(0 to 20\)\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
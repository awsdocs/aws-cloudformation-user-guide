# AWS Auto Scaling ScalingPlan MetricDimension<a name="aws-properties-autoscalingplans-scalingplan-metricdimension"></a>

<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-description"></a>The `MetricDimension` property type specifies a dimension for a customized metric for an AWS Auto Scaling scaling plan\.

<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-inheritance"></a> `MetricDimension` is a property of the [AWS Auto Scaling ScalingPlan CustomizedScalingMetricSpecification](aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification.md) property type\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-syntax.json"></a>

```
{
  "[Value](#cfn-autoscalingplans-scalingplan-metricdimension-value)" : String,
  "[Name](#cfn-autoscalingplans-scalingplan-metricdimension-name)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-syntax.yaml"></a>

```
[Value](#cfn-autoscalingplans-scalingplan-metricdimension-value): String
[Name](#cfn-autoscalingplans-scalingplan-metricdimension-name): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-properties"></a>

`Name`  <a name="cfn-autoscalingplans-scalingplan-metricdimension-name"></a>
The name of the dimension\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-autoscalingplans-scalingplan-metricdimension-value"></a>
The value of the dimension\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
# AWS Auto Scaling ScalingPlan CustomizedScalingMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification"></a>

<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-description"></a>The `CustomizedScalingMetricSpecification` property type specifies a customized metric for a target tracking policy for an AWS Auto Scaling scaling plan\.

<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-inheritance"></a> `CustomizedScalingMetricSpecification` is a property of the [AWS Auto Scaling ScalingPlan TargetTrackingConfiguration](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md) property type\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-syntax.json"></a>

```
{
  "[MetricName](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-metricname)" : String,
  "[Statistic](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-statistic)" : String,
  "[Dimensions](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-dimensions)" : [ [*MetricDimension*](aws-properties-autoscalingplans-scalingplan-metricdimension.md), ... ],
  "[Unit](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-unit)" : String,
  "[Namespace](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-namespace)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-syntax.yaml"></a>

```
[MetricName](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-metricname): String
[Statistic](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-statistic): String
[Dimensions](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-dimensions): 
  - [*MetricDimension*](aws-properties-autoscalingplans-scalingplan-metricdimension.md)
[Unit](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-unit): String
[Namespace](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-namespace): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-dimensions"></a>
The dimensions of the metric\.  
 *Required*: No  
 *Type*: List of [AWS Auto Scaling ScalingPlan MetricDimension](aws-properties-autoscalingplans-scalingplan-metricdimension.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MetricName`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-metricname"></a>
The name of the metric\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Namespace`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-namespace"></a>
The namespace of the metric\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Statistic`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-statistic"></a>
The statistic of the metric\.  
 *Required*: Yes  
 *Type*: String  
 *Valid Values*: `Average` \| `Minimum` \| `Maximum` \| `SampleCount` \| `Sum`   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Unit`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-unit"></a>
The unit of the metric\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
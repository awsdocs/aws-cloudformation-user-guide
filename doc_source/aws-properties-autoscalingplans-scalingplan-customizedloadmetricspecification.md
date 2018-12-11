# AWS Auto Scaling ScalingPlan CustomizedLoadMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification"></a>

<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-description"></a>The `CustomizedLoadMetricSpecification` property type specifies a customized load metric \(an Amazon CloudWatch metric of your choosing\) for predictive scaling to use with AWS Auto Scaling\.

<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-inheritance"></a> `CustomizedLoadMetricSpecification` is a property of the [ScalingInstruction](aws-properties-autoscalingplans-scalingplan-scalinginstruction.md) property type\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions)" : [ [*MetricDimension*](aws-properties-autoscalingplans-scalingplan-metricdimension.md), ... ],
  "[MetricName](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname)" : String,
  "[Namespace](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace)" : String,
  "[Statistic](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic)" : String,
  "[Unit](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit)" : String,
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax.yaml"></a>

```
[Dimensions](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions): 
  - [*MetricDimension*](aws-properties-autoscalingplans-scalingplan-metricdimension.md)
[MetricName](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname): String
[Namespace](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace): String
[Statistic](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic): String
[Unit](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions"></a>
The dimensions of the metric\.  
 *Required*: No  
 *Type*: List of [MetricDimension](aws-properties-autoscalingplans-scalingplan-metricdimension.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MetricName`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname"></a>
The name of the metric\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Namespace`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace"></a>
The namespace of the metric\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Statistic`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic"></a>
The statistic of the metric\.   
For valid values, see [CustomizedLoadMetricSpecification](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_CustomizedLoadMetricSpecification.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Unit`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit"></a>
The unit of the metric\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-seealso"></a>
+ [CustomizedLoadMetricSpecification](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_CustomizedLoadMetricSpecification.html) in the *AWS Auto Scaling API Reference*
+ [Amazon CloudWatch Concepts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html) in the *Amazon CloudWatch User Guide*
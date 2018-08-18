# Application Auto Scaling ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification"></a>

The `CustomizedMetricSpecification` property configures a customized metric for a target tracking policy in Application Auto Scaling\. `CustomizedMetricSpecification` is a subproperty of the [Application Auto Scaling ScalingPolicy TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md) property\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ [MetricDimension](aws-properties-applicationautoscaling-scalingpolicy-metricdimension.md), ...],
  "[MetricName](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[Namespace](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[Statistic](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[Unit](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
[Dimensions](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions):
  - [MetricDimension](aws-properties-applicationautoscaling-scalingpolicy-metricdimension.md)
[MetricName](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname): String
[Namespace](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace): String
[Statistic](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic): String
[Unit](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions"></a>
The dimensions of the metric\. Duplicates not allowed\.  
*Required*: No  
*Type*: List of [Application Auto Scaling ScalingPolicy MetricDimension](aws-properties-applicationautoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricName`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Namespace`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Statistic`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic"></a>
The statistic of the metric\.  
For valid values, see [CustomizedMetricSpecification](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_CustomizedMetricSpecification.html) in the *Application Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Unit`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit"></a>
The unit of the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
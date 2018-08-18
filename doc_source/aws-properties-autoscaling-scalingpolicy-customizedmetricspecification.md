# Amazon EC2 Auto Scaling ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification"></a>

The `CustomizedMetricSpecification` property configures a customized metric for a target tracking policy in Amazon EC2 Auto Scaling\. `CustomizedMetricSpecification` is a subproperty of the [Amazon EC2 Auto Scaling ScalingPolicy TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md) property\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ [*MetricDimension*](aws-properties-autoscaling-scalingpolicy-metricdimension.md), ...],
  "[MetricName](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[Namespace](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[Statistic](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[Unit](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
[Dimensions](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions):
  - [*MetricDimension*](aws-properties-autoscaling-scalingpolicy-metricdimension.md)
[MetricName](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname): String
[Namespace](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace): String
[Statistic](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic): String
[Unit](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions"></a>
The dimensions of the metric\. Duplicates not allowed\.  
*Required*: No  
*Type*: List of [Amazon EC2 Auto Scaling ScalingPolicy MetricDimension](aws-properties-autoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricName`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Namespace`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Statistic`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic"></a>
The statistic of the metric\.  
For valid values, see [CustomizedMetricSpecification](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CustomizedMetricSpecification.html) in the *Amazon EC2 Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Unit`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit"></a>
The unit of the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
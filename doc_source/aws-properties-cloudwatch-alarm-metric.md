# Amazon CloudWatch Alarm Metric<a name="aws-properties-cloudwatch-alarm-metric"></a>

<a name="aws-properties-cloudwatch-alarm-metric-description"></a>The `Metric` property type represents a specific metric\.

<a name="aws-properties-cloudwatch-alarm-metric-inheritance"></a> `Metric` is a property of the [MetricStat](aws-properties-cloudwatch-alarm-metricstat.md) property type\.

## Syntax<a name="aws-properties-cloudwatch-alarm-metric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-alarm-metric-syntax.json"></a>

```
{
  "[Dimensions](#cfn-cloudwatch-alarm-metric-dimensions)" : [ [Dimension](aws-properties-cw-dimension.md), ... ],
  "[MetricName](#cfn-cloudwatch-alarm-metric-metricname)" : String,
  "[Namespace](#cfn-cloudwatch-alarm-metric-namespace)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-alarm-metric-syntax.yaml"></a>

```
[Dimensions](#cfn-cloudwatch-alarm-metric-dimensions): 
  - [Dimension](aws-properties-cw-dimension.md)
[MetricName](#cfn-cloudwatch-alarm-metric-metricname): String
[Namespace](#cfn-cloudwatch-alarm-metric-namespace): String
```

## Properties<a name="aws-properties-cloudwatch-alarm-metric-properties"></a>

`Dimensions`  <a name="cfn-cloudwatch-alarm-metric-dimensions"></a>
The dimensions for the metric\. You can specify a maximum of 10 items\.  
*Required*: No  
*Type*: List of [Dimension](aws-properties-cw-dimension.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricName`  <a name="cfn-cloudwatch-alarm-metric-metricname"></a>
The name of the metric\.  
*Required*: No  
*Type*: String  
*Length constraints*: Minimum of 1\. Maximum of 255\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Namespace`  <a name="cfn-cloudwatch-alarm-metric-namespace"></a>
The namespace of the metric\.  
*Required*: No  
*Type*: String  
*Length constraints*: Minimum of 1\. Maximum of 255\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-cloudwatch-alarm-metric-seealso"></a>
+ [Metric](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_Metric.html) in the *Amazon CloudWatch API Reference*
# Amazon CloudWatch Alarm MetricStat<a name="aws-properties-cloudwatch-alarm-metricstat"></a>

<a name="aws-properties-cloudwatch-alarm-metricstat-description"></a>The `MetricStat` property type defines the metric to be returned, along with the statistics, period, and units\.

<a name="aws-properties-cloudwatch-alarm-metricstat-inheritance"></a> `MetricStat` is a property of the [MetricDataQuery](aws-properties-cloudwatch-alarm-metricdataquery.md) property type\.

## Syntax<a name="aws-properties-cloudwatch-alarm-metricstat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-alarm-metricstat-syntax.json"></a>

```
{
  "[Metric](#cfn-cloudwatch-alarm-metricstat-metric)" : [Metric](aws-properties-cloudwatch-alarm-metric.md),
  "[Period](#cfn-cloudwatch-alarm-metricstat-period)" : Integer,
  "[Stat](#cfn-cloudwatch-alarm-metricstat-stat)" : String,
  "[Unit](#cfn-cloudwatch-alarm-metricstat-unit)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-alarm-metricstat-syntax.yaml"></a>

```
[Metric](#cfn-cloudwatch-alarm-metricstat-metric): 
  [Metric](aws-properties-cloudwatch-alarm-metric.md)
[Period](#cfn-cloudwatch-alarm-metricstat-period): Integer
[Stat](#cfn-cloudwatch-alarm-metricstat-stat): String
[Unit](#cfn-cloudwatch-alarm-metricstat-unit): String
```

## Properties<a name="aws-properties-cloudwatch-alarm-metricstat-properties"></a>

`Metric`  <a name="cfn-cloudwatch-alarm-metricstat-metric"></a>
The metric to return, including the metric name, namespace, and dimensions\.  
*Required*: Yes  
*Type*: [Metric](aws-properties-cloudwatch-alarm-metric.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Period`  <a name="cfn-cloudwatch-alarm-metricstat-period"></a>
The period, in seconds, to use when retrieving the metric\. Minimum value of `1`\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Stat`  <a name="cfn-cloudwatch-alarm-metricstat-stat"></a>
The statistic to return\. It can include any CloudWatch statistic or extended statistic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Unit`  <a name="cfn-cloudwatch-alarm-metricstat-unit"></a>
The unit to use for the returned data points\.  
*Required*: No  
*Type*: String  
*Valid values*: `Seconds` \| `Microseconds` \| `Milliseconds` \| `Bytes` \| `Kilobytes` \| `Megabytes` \| `Gigabytes` \| `Terabytes` \| `Bits` \| `Kilobits` \| `Megabits` \| `Gigabits` \| `Terabits` \| `Percent` \| `Count` \| `Bytes/Second` \| `Kilobytes/Second` \| `Megabytes/Second` \| `Gigabytes/Second` \| `Terabytes/Second` \| `Bits/Second` \| `Kilobits/Second` \| `Megabits/Second` \| `Gigabits/Second` \| `Terabits/Second` \| `Count/Second` \| `None`  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-cloudwatch-alarm-metricstat-seealso"></a>
+ [MetricStat](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_MetricStat.html) in the *Amazon CloudWatch API Reference*
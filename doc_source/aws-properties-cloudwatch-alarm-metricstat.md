# AWS::CloudWatch::Alarm MetricStat<a name="aws-properties-cloudwatch-alarm-metricstat"></a>

This structure defines the metric to be returned, along with the statistics, period, and units\.

 `MetricStat` is a property of the [MetricDataQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudwatch-alarm-metricdataquery.html) property type\.

## Syntax<a name="aws-properties-cloudwatch-alarm-metricstat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-alarm-metricstat-syntax.json"></a>

```
{
  "[Metric](#cfn-cloudwatch-alarm-metricstat-metric)" : Metric,
  "[Period](#cfn-cloudwatch-alarm-metricstat-period)" : Integer,
  "[Stat](#cfn-cloudwatch-alarm-metricstat-stat)" : String,
  "[Unit](#cfn-cloudwatch-alarm-metricstat-unit)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-alarm-metricstat-syntax.yaml"></a>

```
  [Metric](#cfn-cloudwatch-alarm-metricstat-metric): 
    Metric
  [Period](#cfn-cloudwatch-alarm-metricstat-period): Integer
  [Stat](#cfn-cloudwatch-alarm-metricstat-stat): String
  [Unit](#cfn-cloudwatch-alarm-metricstat-unit): String
```

## Properties<a name="aws-properties-cloudwatch-alarm-metricstat-properties"></a>

`Metric`  <a name="cfn-cloudwatch-alarm-metricstat-metric"></a>
The metric to return, including the metric name, namespace, and dimensions\.  
*Required*: Yes  
*Type*: [Metric](aws-properties-cloudwatch-alarm-metric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Period`  <a name="cfn-cloudwatch-alarm-metricstat-period"></a>
The granularity, in seconds, of the returned data points\. For metrics with regular resolution, a period can be as short as one minute \(60 seconds\) and must be a multiple of 60\. For high\-resolution metrics that are collected at intervals of less than one minute, the period can be 1, 5, 10, 30, 60, or any multiple of 60\. High\-resolution metrics are those metrics stored by a `PutMetricData` call that includes a `StorageResolution` of 1 second\.  
If the `StartTime` parameter specifies a time stamp that is greater than 3 hours ago, you must specify the period as follows or no data points in that time range is returned:  
+ Start time between 3 hours and 15 days ago \- Use a multiple of 60 seconds \(1 minute\)\.
+ Start time between 15 and 63 days ago \- Use a multiple of 300 seconds \(5 minutes\)\.
+ Start time greater than 63 days ago \- Use a multiple of 3600 seconds \(1 hour\)\.
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stat`  <a name="cfn-cloudwatch-alarm-metricstat-stat"></a>
The statistic to return\. It can include any CloudWatch statistic or extended statistic\. For a list of valid values, see the table in [ Statistics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#Statistic) in the *Amazon CloudWatch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-cloudwatch-alarm-metricstat-unit"></a>
The unit to use for the returned data points\.   
Valid values are: Seconds, Microseconds, Milliseconds, Bytes, Kilobytes, Megabytes, Gigabytes, Terabytes, Bits, Kilobits, Megabits, Gigabits, Terabits, Percent, Count, Bytes/Second, Kilobytes/Second, Megabytes/Second, Gigabytes/Second, Terabytes/Second, Bits/Second, Kilobits/Second, Megabits/Second, Gigabits/Second, Terabits/Second, Count/Second, or None\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Bits | Bits/Second | Bytes | Bytes/Second | Count | Count/Second | Gigabits | Gigabits/Second | Gigabytes | Gigabytes/Second | Kilobits | Kilobits/Second | Kilobytes | Kilobytes/Second | Megabits | Megabits/Second | Megabytes | Megabytes/Second | Microseconds | Milliseconds | None | Percent | Seconds | Terabits | Terabits/Second | Terabytes | Terabytes/Second`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
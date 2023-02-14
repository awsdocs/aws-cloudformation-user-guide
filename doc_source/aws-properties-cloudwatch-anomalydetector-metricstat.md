# AWS::CloudWatch::AnomalyDetector MetricStat<a name="aws-properties-cloudwatch-anomalydetector-metricstat"></a>

This structure defines the metric to be returned, along with the statistics, period, and units\.

## Syntax<a name="aws-properties-cloudwatch-anomalydetector-metricstat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-anomalydetector-metricstat-syntax.json"></a>

```
{
  "[Metric](#cfn-cloudwatch-anomalydetector-metricstat-metric)" : Metric,
  "[Period](#cfn-cloudwatch-anomalydetector-metricstat-period)" : Integer,
  "[Stat](#cfn-cloudwatch-anomalydetector-metricstat-stat)" : String,
  "[Unit](#cfn-cloudwatch-anomalydetector-metricstat-unit)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-anomalydetector-metricstat-syntax.yaml"></a>

```
  [Metric](#cfn-cloudwatch-anomalydetector-metricstat-metric): 
    Metric
  [Period](#cfn-cloudwatch-anomalydetector-metricstat-period): Integer
  [Stat](#cfn-cloudwatch-anomalydetector-metricstat-stat): String
  [Unit](#cfn-cloudwatch-anomalydetector-metricstat-unit): String
```

## Properties<a name="aws-properties-cloudwatch-anomalydetector-metricstat-properties"></a>

`Metric`  <a name="cfn-cloudwatch-anomalydetector-metricstat-metric"></a>
The metric to return, including the metric name, namespace, and dimensions\.  
*Required*: Yes  
*Type*: [Metric](aws-properties-cloudwatch-anomalydetector-metric.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Period`  <a name="cfn-cloudwatch-anomalydetector-metricstat-period"></a>
The granularity, in seconds, of the returned data points\. For metrics with regular resolution, a period can be as short as one minute \(60 seconds\) and must be a multiple of 60\. For high\-resolution metrics that are collected at intervals of less than one minute, the period can be 1, 5, 10, 30, 60, or any multiple of 60\. High\-resolution metrics are those metrics stored by a `PutMetricData` call that includes a `StorageResolution` of 1 second\.  
If the `StartTime` parameter specifies a time stamp that is greater than 3 hours ago, you must specify the period as follows or no data points in that time range is returned:  
+ Start time between 3 hours and 15 days ago \- Use a multiple of 60 seconds \(1 minute\)\.
+ Start time between 15 and 63 days ago \- Use a multiple of 300 seconds \(5 minutes\)\.
+ Start time greater than 63 days ago \- Use a multiple of 3600 seconds \(1 hour\)\.
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Stat`  <a name="cfn-cloudwatch-anomalydetector-metricstat-stat"></a>
The statistic to return\. It can include any CloudWatch statistic or extended statistic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Unit`  <a name="cfn-cloudwatch-anomalydetector-metricstat-unit"></a>
When you are using a `Put` operation, this defines what unit you want to use when storing the metric\.  
In a `Get` operation, if you omit `Unit` then all data that was collected with any unit is returned, along with the corresponding units that were specified when the data was reported to CloudWatch\. If you specify a unit, the operation returns only data that was collected with that unit specified\. If you specify a unit that does not match the data collected, the results of the operation are null\. CloudWatch does not perform unit conversions\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Bits | Bits/Second | Bytes | Bytes/Second | Count | Count/Second | Gigabits | Gigabits/Second | Gigabytes | Gigabytes/Second | Kilobits | Kilobits/Second | Kilobytes | Kilobytes/Second | Megabits | Megabits/Second | Megabytes | Megabytes/Second | Microseconds | Milliseconds | None | Percent | Seconds | Terabits | Terabits/Second | Terabytes | Terabytes/Second`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
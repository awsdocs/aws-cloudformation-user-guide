# AWS::CloudWatch::Alarm MetricDataQuery<a name="aws-properties-cloudwatch-alarm-metricdataquery"></a>

The `MetricDataQuery` property type specifies the metric data to return, and whether this call is just retrieving a batch set of data for one metric, or is performing a math expression on metric data\. 

Any expression used must return a single time series\. For more information, see [Metric Math Syntax and Functions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/using-metric-math.html#metric-math-syntax) in the *Amazon CloudWatch User Guide*\.

## Syntax<a name="aws-properties-cloudwatch-alarm-metricdataquery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-alarm-metricdataquery-syntax.json"></a>

```
{
  "[Expression](#cfn-cloudwatch-alarm-metricdataquery-expression)" : String,
  "[Id](#cfn-cloudwatch-alarm-metricdataquery-id)" : String,
  "[Label](#cfn-cloudwatch-alarm-metricdataquery-label)" : String,
  "[MetricStat](#cfn-cloudwatch-alarm-metricdataquery-metricstat)" : MetricStat,
  "[Period](#cfn-cloudwatch-alarm-metricdataquery-period)" : Integer,
  "[ReturnData](#cfn-cloudwatch-alarm-metricdataquery-returndata)" : Boolean
}
```

### YAML<a name="aws-properties-cloudwatch-alarm-metricdataquery-syntax.yaml"></a>

```
  [Expression](#cfn-cloudwatch-alarm-metricdataquery-expression): String
  [Id](#cfn-cloudwatch-alarm-metricdataquery-id): String
  [Label](#cfn-cloudwatch-alarm-metricdataquery-label): String
  [MetricStat](#cfn-cloudwatch-alarm-metricdataquery-metricstat): 
    MetricStat
  [Period](#cfn-cloudwatch-alarm-metricdataquery-period): Integer
  [ReturnData](#cfn-cloudwatch-alarm-metricdataquery-returndata): Boolean
```

## Properties<a name="aws-properties-cloudwatch-alarm-metricdataquery-properties"></a>

`Expression`  <a name="cfn-cloudwatch-alarm-metricdataquery-expression"></a>
The math expression to be performed on the returned data, if this object is performing a math expression\. This expression can use the `Id` of the other metrics to refer to those metrics, and can also use the `Id` of other expressions to use the result of those expressions\. For more information about metric math expressions, see [Metric Math Syntax and Functions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/using-metric-math.html#metric-math-syntax) in the *Amazon CloudWatch User Guide*\.  
Within each MetricDataQuery object, you must specify either `Expression` or `MetricStat` but not both\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-cloudwatch-alarm-metricdataquery-id"></a>
A short name used to tie this object to the results in the response\. This name must be unique within a single call to `GetMetricData`\. If you are performing math expressions on this set of data, this name represents that data and can serve as a variable in the mathematical expression\. The valid characters are letters, numbers, and underscore\. The first character must be a lowercase letter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Label`  <a name="cfn-cloudwatch-alarm-metricdataquery-label"></a>
A human\-readable label for this metric or expression\. This is especially useful if this is an expression, so that you know what the value represents\. If the metric or expression is shown in a CloudWatch dashboard widget, the label is shown\. If `Label` is omitted, CloudWatch generates a default\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricStat`  <a name="cfn-cloudwatch-alarm-metricdataquery-metricstat"></a>
The metric to be returned, along with statistics, period, and units\. Use this parameter only if this object is retrieving a metric and not performing a math expression on returned data\.  
Within one MetricDataQuery object, you must specify either `Expression` or `MetricStat` but not both\.  
*Required*: No  
*Type*: [MetricStat](aws-properties-cloudwatch-alarm-metricstat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Period`  <a name="cfn-cloudwatch-alarm-metricdataquery-period"></a>
The granularity, in seconds, of the returned data points\. For metrics with regular resolution, a period can be as short as one minute \(60 seconds\) and must be a multiple of 60\. For high\-resolution metrics that are collected at intervals of less than one minute, the period can be 1, 5, 10, 30, 60, or any multiple of 60\. High\-resolution metrics are those metrics stored by a `PutMetricData` operation that includes a `StorageResolution of 1 second`\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReturnData`  <a name="cfn-cloudwatch-alarm-metricdataquery-returndata"></a>
This option indicates whether to return the timestamps and raw data values of this metric\.  
When you create an alarm based on a metric math expression, specify `True` for this value for only the one math expression that the alarm is based on\. You must specify `False` for `ReturnData` for all the other metrics and expressions used in the alarm\.  
This field is required\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# Amazon CloudWatch Alarm MetricDataQuery<a name="aws-properties-cloudwatch-alarm-metricdataquery"></a>

<a name="aws-properties-cloudwatch-alarm-metricdataquery-description"></a>The `MetricDataQuery` property type specifies the metric data to return, and whether this call is just retrieving a batch set of data for one metric, or is performing a math expression on metric data\. 

<a name="aws-properties-cloudwatch-alarm-metricdataquery-inheritance"></a> `MetricDataQuery` is a property of the [AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md) resource type\.

## Syntax<a name="aws-properties-cloudwatch-alarm-metricdataquery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-alarm-metricdataquery-syntax.json"></a>

```
{
  "[Expression](#cfn-cloudwatch-alarm-metricdataquery-expression)" : String,
  "[Id](#cfn-cloudwatch-alarm-metricdataquery-id)" : String,
  "[Label](#cfn-cloudwatch-alarm-metricdataquery-label)" : String,
  "[MetricStat](#cfn-cloudwatch-alarm-metricdataquery-metricstat)" : [MetricStat](aws-properties-cloudwatch-alarm-metricstat.md),
  "[ReturnData](#cfn-cloudwatch-alarm-metricdataquery-returndata)" : Boolean
}
```

### YAML<a name="aws-properties-cloudwatch-alarm-metricdataquery-syntax.yaml"></a>

```
[Expression](#cfn-cloudwatch-alarm-metricdataquery-expression): String
[Id](#cfn-cloudwatch-alarm-metricdataquery-id): String
[Label](#cfn-cloudwatch-alarm-metricdataquery-label): String
[MetricStat](#cfn-cloudwatch-alarm-metricdataquery-metricstat): 
  [MetricStat](aws-properties-cloudwatch-alarm-metricstat.md)
[ReturnData](#cfn-cloudwatch-alarm-metricdataquery-returndata): Boolean
```

## Properties<a name="aws-properties-cloudwatch-alarm-metricdataquery-properties"></a>

`Expression`  <a name="cfn-cloudwatch-alarm-metricdataquery-expression"></a>
The math expression to be performed on the returned data, if this structure is performing a math expression\. For more information about metric math expressions, see [Metric Math Syntax and Functions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/using-metric-math.html#metric-math-syntax) in the *Amazon CloudWatch User Guide*\.  
Within one MetricDataQuery structure, you must specify either `Expression` or `MetricStat`, but not both\.  
*Required*: No  
*Type*: String  
*Length constraints*: Minimum of 1\. Maximum of 1024\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Id`  <a name="cfn-cloudwatch-alarm-metricdataquery-id"></a>
A short name used to tie this structure to the results in the response\. This name must be unique within a single call to `GetMetricData`\. If you are performing math expressions on this set of data, this name represents that data and can serve as a variable in the mathematical expression\. The valid characters are letters, numbers, and underscore\. The first character must be a lowercase letter\.   
*Required*: Yes  
*Type*: String  
*Length constraints*: Minimum of 1\. Maximum of 255\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Label`  <a name="cfn-cloudwatch-alarm-metricdataquery-label"></a>
A human\-readable label for this metric or expression\. This is especially useful if this is an expression, so that you know what the value represents\. If the metric or expression is shown in a CloudWatch dashboard widget, the label is shown\. If `Label` is omitted, CloudWatch generates a default\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricStat`  <a name="cfn-cloudwatch-alarm-metricdataquery-metricstat"></a>
The metric to be returned, along with statistics, period, and units\. Use this parameter only if this structure is performing a data retrieval and not performing a math expression on the returned data\.  
Within one MetricDataQuery structure, you must specify either `Expression` or `MetricStat`, but not both\.  
*Required*: No  
*Type*: [](aws-properties-cloudwatch-alarm-metricstat.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReturnData`  <a name="cfn-cloudwatch-alarm-metricdataquery-returndata"></a>
Indicates whether to return the time stamps and raw data values of this metric\. If you are performing this call just to do math expressions and do not also need the raw data returned, you can specify `False`\. If you omit this, the default of `True` is used\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-cloudwatch-alarm-metricdataquery-seealso"></a>
+ [MetricDataQuery](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_MetricDataQuery.html) in the *Amazon CloudWatch API Reference*
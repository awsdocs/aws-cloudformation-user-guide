# AWS::AutoScaling::ScalingPolicy MetricDataQuery<a name="aws-properties-autoscaling-scalingpolicy-metricdataquery"></a>

The metric data to return\. Also defines whether this call is returning data for one metric only, or whether it is performing a math expression on the values of returned metric statistics to create a new time series\. A time series is a series of data points, each of which is associated with a timestamp\.

`MetricDataQuery` is a property of the following property types:
+ [AWS::AutoScaling::ScalingPolicy PredictiveScalingCustomizedScalingMetric](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-predictivescalingcustomizedscalingmetric.html)
+ [AWS::AutoScaling::ScalingPolicy PredictiveScalingCustomizedLoadMetric](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-predictivescalingcustomizedloadmetric.html)
+ [AWS::AutoScaling::ScalingPolicy PredictiveScalingCustomizedCapacityMetric](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-predictivescalingcustomizedcapacitymetric.html)

Predictive scaling uses the time series data received from CloudWatch to understand how to schedule capacity based on your historical workload patterns\. 

You can call for a single metric or perform math expressions on multiple metrics\. Any expressions used in a metric specification must eventually return a single time series\.

For more information and examples, see [Advanced predictive scaling policy configurations using custom metrics](https://docs.aws.amazon.com/autoscaling/ec2/userguide/predictive-scaling-customized-metric-specification.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-metricdataquery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-metricdataquery-syntax.json"></a>

```
{
  "[Expression](#cfn-autoscaling-scalingpolicy-metricdataquery-expression)" : String,
  "[Id](#cfn-autoscaling-scalingpolicy-metricdataquery-id)" : String,
  "[Label](#cfn-autoscaling-scalingpolicy-metricdataquery-label)" : String,
  "[MetricStat](#cfn-autoscaling-scalingpolicy-metricdataquery-metricstat)" : MetricStat,
  "[ReturnData](#cfn-autoscaling-scalingpolicy-metricdataquery-returndata)" : Boolean
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-metricdataquery-syntax.yaml"></a>

```
  [Expression](#cfn-autoscaling-scalingpolicy-metricdataquery-expression): String
  [Id](#cfn-autoscaling-scalingpolicy-metricdataquery-id): String
  [Label](#cfn-autoscaling-scalingpolicy-metricdataquery-label): String
  [MetricStat](#cfn-autoscaling-scalingpolicy-metricdataquery-metricstat): 
    MetricStat
  [ReturnData](#cfn-autoscaling-scalingpolicy-metricdataquery-returndata): Boolean
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-metricdataquery-properties"></a>

`Expression`  <a name="cfn-autoscaling-scalingpolicy-metricdataquery-expression"></a>
The math expression to perform on the returned data, if this object is performing a math expression\. This expression can use the `Id` of the other metrics to refer to those metrics, and can also use the `Id` of other expressions to use the result of those expressions\.   
Conditional: Within each `MetricDataQuery` object, you must specify either `Expression` or `MetricStat`, but not both\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-autoscaling-scalingpolicy-metricdataquery-id"></a>
A short name that identifies the object's results in the response\. This name must be unique among all `MetricDataQuery` objects specified for a single scaling policy\. If you are performing math expressions on this set of data, this name represents that data and can serve as a variable in the mathematical expression\. The valid characters are letters, numbers, and underscores\. The first character must be a lowercase letter\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Label`  <a name="cfn-autoscaling-scalingpolicy-metricdataquery-label"></a>
A human\-readable label for this metric or expression\. This is especially useful if this is a math expression, so that you know what the value represents\.  
*Required*: No  
*Type*: String  
*Maximum*: `2047`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricStat`  <a name="cfn-autoscaling-scalingpolicy-metricdataquery-metricstat"></a>
Information about the metric data to return\.  
Conditional: Within each `MetricDataQuery` object, you must specify either `Expression` or `MetricStat`, but not both\.  
*Required*: No  
*Type*: [MetricStat](aws-properties-autoscaling-scalingpolicy-metricstat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReturnData`  <a name="cfn-autoscaling-scalingpolicy-metricdataquery-returndata"></a>
Indicates whether to return the timestamps and raw data values of this metric\.   
If you use any math expressions, specify `true` for this value for only the final math expression that the metric specification is based on\. You must specify `false` for `ReturnData` for all the other metrics and expressions used in the metric specification\.  
If you are only retrieving metrics and not performing any math expressions, do not specify anything for `ReturnData`\. This sets it to its default \(`true`\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
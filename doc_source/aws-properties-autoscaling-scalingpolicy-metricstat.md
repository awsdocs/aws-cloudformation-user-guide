# AWS::AutoScaling::ScalingPolicy MetricStat<a name="aws-properties-autoscaling-scalingpolicy-metricstat"></a>

 `MetricStat` is a property of the [AWS::AutoScaling::ScalingPolicy MetricDataQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-metricdataquery.html) property type\.

This structure defines the CloudWatch metric to return, along with the statistic, period, and unit\.

For more information about the CloudWatch terminology below, see [Amazon CloudWatch concepts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html) in the *Amazon CloudWatch User Guide*\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-metricstat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-metricstat-syntax.json"></a>

```
{
  "[Metric](#cfn-autoscaling-scalingpolicy-metricstat-metric)" : Metric,
  "[Stat](#cfn-autoscaling-scalingpolicy-metricstat-stat)" : String,
  "[Unit](#cfn-autoscaling-scalingpolicy-metricstat-unit)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-metricstat-syntax.yaml"></a>

```
  [Metric](#cfn-autoscaling-scalingpolicy-metricstat-metric): 
    Metric
  [Stat](#cfn-autoscaling-scalingpolicy-metricstat-stat): String
  [Unit](#cfn-autoscaling-scalingpolicy-metricstat-unit): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-metricstat-properties"></a>

`Metric`  <a name="cfn-autoscaling-scalingpolicy-metricstat-metric"></a>
The CloudWatch metric to return, including the metric name, namespace, and dimensions\. To get the exact metric name, namespace, and dimensions, inspect the [Metric](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_Metric.html) object that is returned by a call to [ListMetrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_ListMetrics.html)\.  
*Required*: Yes  
*Type*: [Metric](aws-properties-autoscaling-scalingpolicy-metric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stat`  <a name="cfn-autoscaling-scalingpolicy-metricstat-stat"></a>
The statistic to return\. It can include any CloudWatch statistic or extended statistic\. For a list of valid values, see the table in [Statistics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#Statistic) in the *Amazon CloudWatch User Guide*\.  
The most commonly used metrics for predictive scaling are `Average` and `Sum`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-autoscaling-scalingpolicy-metricstat-unit"></a>
The unit to use for the returned data points\. For a complete list of the units that CloudWatch supports, see the [MetricDatum](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_MetricDatum.html) data type in the *Amazon CloudWatch API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
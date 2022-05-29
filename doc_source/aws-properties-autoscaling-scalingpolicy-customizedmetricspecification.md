# AWS::AutoScaling::ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification"></a>

Contains customized metric specification information for a target tracking scaling policy for Amazon EC2 Auto Scaling\.

To create your customized metric specification:
+ Add values for each required property from CloudWatch\. You can use an existing metric, or a new metric that you create\. To use your own metric, you must first publish the metric to CloudWatch\. For more information, see [Publish Custom Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/publishingMetrics.html) in the *Amazon CloudWatch User Guide*\.
+ Choose a metric that changes proportionally with capacity\. The value of the metric should increase or decrease in inverse proportion to the number of capacity units\. That is, the value of the metric should decrease when capacity increases\.

For more information about CloudWatch, see [Amazon CloudWatch Concepts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html)\.

 `CustomizedMetricSpecification` is a property of the [AWS::AutoScaling::ScalingPolicy TargetTrackingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.html) property type\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ MetricDimension, ... ],
  "[MetricName](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[Namespace](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[Statistic](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[Unit](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
  [Dimensions](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions): 
    - MetricDimension
  [MetricName](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname): String
  [Namespace](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace): String
  [Statistic](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic): String
  [Unit](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions"></a>
The dimensions of the metric\.  
Conditional: If you published your metric with dimensions, you must specify the same dimensions in your scaling policy\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-autoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname"></a>
The name of the metric\. To get the exact metric name, namespace, and dimensions, inspect the [Metric](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_Metric.html) object that is returned by a call to [ListMetrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_ListMetrics.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic"></a>
The statistic of the metric\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Average | Maximum | Minimum | SampleCount | Sum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit"></a>
The unit of the metric\. For a complete list of the units that CloudWatch supports, see the [MetricDatum](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_MetricDatum.html) data type in the *Amazon CloudWatch API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
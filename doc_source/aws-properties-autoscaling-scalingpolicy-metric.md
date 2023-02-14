# AWS::AutoScaling::ScalingPolicy Metric<a name="aws-properties-autoscaling-scalingpolicy-metric"></a>

Represents a specific metric\. 

 `Metric` is a property of the [AWS::AutoScaling::ScalingPolicy MetricStat](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-metricstat.html) property type\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-metric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-metric-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscaling-scalingpolicy-metric-dimensions)" : [ MetricDimension, ... ],
  "[MetricName](#cfn-autoscaling-scalingpolicy-metric-metricname)" : String,
  "[Namespace](#cfn-autoscaling-scalingpolicy-metric-namespace)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-metric-syntax.yaml"></a>

```
  [Dimensions](#cfn-autoscaling-scalingpolicy-metric-dimensions): 
    - MetricDimension
  [MetricName](#cfn-autoscaling-scalingpolicy-metric-metricname): String
  [Namespace](#cfn-autoscaling-scalingpolicy-metric-namespace): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-metric-properties"></a>

`Dimensions`  <a name="cfn-autoscaling-scalingpolicy-metric-dimensions"></a>
The dimensions for the metric\. For the list of available dimensions, see the AWS documentation available from the table in [AWS services that publish CloudWatch metrics ](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/aws-services-cloudwatch-metrics.html) in the *Amazon CloudWatch User Guide*\.   
Conditional: If you published your metric with dimensions, you must specify the same dimensions in your scaling policy\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-autoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-autoscaling-scalingpolicy-metric-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-autoscaling-scalingpolicy-metric-namespace"></a>
The namespace of the metric\. For more information, see the table in [AWS services that publish CloudWatch metrics ](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/aws-services-cloudwatch-metrics.html) in the *Amazon CloudWatch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::ApplicationAutoScaling::ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification"></a>

Contains customized metric specification information for a target tracking scaling policy for Application Auto Scaling\. 

For information about the available metrics for a service, see [AWS services that publish CloudWatch metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/aws-services-cloudwatch-metrics.html) in the *Amazon CloudWatch User Guide*\.

To create your customized metric specification:
+ Add values for each required parameter from CloudWatch\. You can use an existing metric, or a new metric that you create\. To use your own metric, you must first publish the metric to CloudWatch\. For more information, see [Publish custom metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/publishingMetrics.html) in the *Amazon CloudWatch User Guide*\.
+ Choose a metric that changes proportionally with capacity\. The value of the metric should increase or decrease in inverse proportion to the number of capacity units\. That is, the value of the metric should decrease when capacity increases, and increase when capacity decreases\. 

For an example of how creating new metrics can be useful, see [Scaling based on Amazon SQS](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html) in the *Amazon EC2 Auto Scaling User Guide*\. This topic mentions Auto Scaling groups, but the same scenario for Amazon SQS can apply to the target tracking scaling policies that you create for a Spot Fleet by using Application Auto Scaling\.

For more information about the CloudWatch terminology below, see [Amazon CloudWatch concepts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html)\. 

`CustomizedMetricSpecification` is a property of the [AWS::ApplicationAutoScaling::ScalingPolicy TargetTrackingScalingPolicyConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.html) property type\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ MetricDimension, ... ],
  "[MetricName](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[Namespace](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[Statistic](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[Unit](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
  [Dimensions](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions): 
    - MetricDimension
  [MetricName](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname): String
  [Namespace](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace): String
  [Statistic](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic): String
  [Unit](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions"></a>
The dimensions of the metric\.   
Conditional: If you published your metric with dimensions, you must specify the same dimensions in your scaling policy\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-applicationautoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname"></a>
The name of the metric\. To get the exact metric name, namespace, and dimensions, inspect the [Metric](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_Metric.html) object that is returned by a call to [ListMetrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_ListMetrics.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic"></a>
The statistic of the metric\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Average | Maximum | Minimum | SampleCount | Sum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit"></a>
The unit of the metric\. For a complete list of the units that CloudWatch supports, see the [MetricDatum](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_MetricDatum.html) data type in the *Amazon CloudWatch API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification--seealso"></a>
+ [Application Auto Scaling template examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html#scenario-app-as-template-examples)
+ [Getting started](https://docs.aws.amazon.com/autoscaling/application/userguide/getting-started.html) in the *Application Auto Scaling User Guide*


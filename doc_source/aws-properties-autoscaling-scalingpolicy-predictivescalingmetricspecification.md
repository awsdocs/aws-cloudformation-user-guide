# AWS::AutoScaling::ScalingPolicy PredictiveScalingMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification"></a>

A structure that specifies a metric specification for the `MetricSpecifications` property of the [AWS::AutoScaling::ScalingPolicy PredictiveScalingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration.html) property type\.

You must specify either a metric pair, or a load metric and a scaling metric individually\. Specifying a metric pair instead of individual metrics provides a simpler way to configure metrics for a scaling policy\. You choose the metric pair, and the policy automatically knows the correct sum and average statistics to use for the load metric and the scaling metric\.

Example
+ You create a predictive scaling policy and specify `ALBRequestCount` as the value for the metric pair and `1000.0` as the target value\. For this type of metric, you must provide the metric dimension for the corresponding target group, so you also provide a resource label for the Application Load Balancer target group that is attached to your Auto Scaling group\.
+ The number of requests the target group receives per minute provides the load metric, and the request count averaged between the members of the target group provides the scaling metric\. In CloudWatch, this refers to the `RequestCount` and `RequestCountPerTarget` metrics, respectively\.
+ For optimal use of predictive scaling, you adhere to the best practice of using a dynamic scaling policy to automatically scale between the minimum capacity and maximum capacity in response to real\-time changes in resource utilization\.
+ Amazon EC2 Auto Scaling consumes data points for the load metric over the last 14 days and creates an hourly load forecast for predictive scaling\. \(A minimum of 24 hours of data is required\.\)
+ After creating the load forecast, Amazon EC2 Auto Scaling determines when to reduce or increase the capacity of your Auto Scaling group in each hour of the forecast period so that the average number of requests received by each instance is as close to 1000 requests per minute as possible at all times\.

For information about using custom metrics with predictive scaling, see [Advanced predictive scaling policy configurations using custom metrics](https://docs.aws.amazon.com/autoscaling/ec2/userguide/predictive-scaling-customized-metric-specification.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-syntax.json"></a>

```
{
  "[CustomizedCapacityMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedcapacitymetricspecification)" : PredictiveScalingCustomizedCapacityMetric,
  "[CustomizedLoadMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedloadmetricspecification)" : PredictiveScalingCustomizedLoadMetric,
  "[CustomizedScalingMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedscalingmetricspecification)" : PredictiveScalingCustomizedScalingMetric,
  "[PredefinedLoadMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedloadmetricspecification)" : PredictiveScalingPredefinedLoadMetric,
  "[PredefinedMetricPairSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedmetricpairspecification)" : PredictiveScalingPredefinedMetricPair,
  "[PredefinedScalingMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedscalingmetricspecification)" : PredictiveScalingPredefinedScalingMetric,
  "[TargetValue](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-syntax.yaml"></a>

```
  [CustomizedCapacityMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedcapacitymetricspecification): 
    PredictiveScalingCustomizedCapacityMetric
  [CustomizedLoadMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedloadmetricspecification): 
    PredictiveScalingCustomizedLoadMetric
  [CustomizedScalingMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedscalingmetricspecification): 
    PredictiveScalingCustomizedScalingMetric
  [PredefinedLoadMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedloadmetricspecification): 
    PredictiveScalingPredefinedLoadMetric
  [PredefinedMetricPairSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedmetricpairspecification): 
    PredictiveScalingPredefinedMetricPair
  [PredefinedScalingMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedscalingmetricspecification): 
    PredictiveScalingPredefinedScalingMetric
  [TargetValue](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-targetvalue): Double
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-properties"></a>

`CustomizedCapacityMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedcapacitymetricspecification"></a>
The customized capacity metric specification\.  
*Required*: No  
*Type*: [PredictiveScalingCustomizedCapacityMetric](aws-properties-autoscaling-scalingpolicy-predictivescalingcustomizedcapacitymetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomizedLoadMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedloadmetricspecification"></a>
The customized load metric specification\.  
*Required*: No  
*Type*: [PredictiveScalingCustomizedLoadMetric](aws-properties-autoscaling-scalingpolicy-predictivescalingcustomizedloadmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomizedScalingMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-customizedscalingmetricspecification"></a>
The customized scaling metric specification\.  
*Required*: No  
*Type*: [PredictiveScalingCustomizedScalingMetric](aws-properties-autoscaling-scalingpolicy-predictivescalingcustomizedscalingmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedLoadMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedloadmetricspecification"></a>
The predefined load metric specification\.  
*Required*: No  
*Type*: [PredictiveScalingPredefinedLoadMetric](aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedloadmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedMetricPairSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedmetricpairspecification"></a>
The predefined metric pair specification from which Amazon EC2 Auto Scaling determines the appropriate scaling metric and load metric to use\.  
*Required*: No  
*Type*: [PredictiveScalingPredefinedMetricPair](aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedScalingMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedscalingmetricspecification"></a>
The predefined scaling metric specification\.  
*Required*: No  
*Type*: [PredictiveScalingPredefinedScalingMetric](aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-targetvalue"></a>
Specifies the target utilization\.  
Some metrics are based on a count instead of a percentage, such as the request count for an Application Load Balancer or the number of messages in an SQS queue\. If the scaling policy specifies one of these metrics, specify the target utilization as the optimal average request or message count per instance during any one\-minute interval\. 
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
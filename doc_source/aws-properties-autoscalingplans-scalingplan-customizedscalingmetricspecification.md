# AWS::AutoScalingPlans::ScalingPlan CustomizedScalingMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification"></a>

 `CustomizedScalingMetricSpecification` is a subproperty of [TargetTrackingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.html) that specifies a customized scaling metric for a target tracking configuration to use with AWS Auto Scaling\. 

To create your customized scaling metric specification:
+ Add values for each required property from CloudWatch\. You can use an existing metric, or a new metric that you create\. To use your own metric, you must first publish the metric to CloudWatch\. For more information, see [Publish Custom Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/publishingMetrics.html) in the *Amazon CloudWatch User Guide*\. 
+ Choose a metric that changes proportionally with capacity\. The value of the metric should increase or decrease in inverse proportion to the number of capacity units\. That is, the value of the metric should decrease when capacity increases\. 

For information about terminology, available metrics, or how to publish new metrics, see [Amazon CloudWatch Concepts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html) in the *Amazon CloudWatch User Guide*\. 

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-dimensions)" : [ MetricDimension, ... ],
  "[MetricName](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-metricname)" : String,
  "[Namespace](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-namespace)" : String,
  "[Statistic](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-statistic)" : String,
  "[Unit](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-syntax.yaml"></a>

```
  [Dimensions](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-dimensions): 
    - MetricDimension
  [MetricName](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-metricname): String
  [Namespace](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-namespace): String
  [Statistic](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-statistic): String
  [Unit](#cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-unit): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-dimensions"></a>
The dimensions of the metric\.  
Conditional: If you published your metric with dimensions, you must specify the same dimensions in your customized scaling metric specification\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-autoscalingplans-scalingplan-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-statistic"></a>
The statistic of the metric\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Average | Maximum | Minimum | SampleCount | Sum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-autoscalingplans-scalingplan-customizedscalingmetricspecification-unit"></a>
The unit of the metric\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification--seealso"></a>
+ [AWS Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html)
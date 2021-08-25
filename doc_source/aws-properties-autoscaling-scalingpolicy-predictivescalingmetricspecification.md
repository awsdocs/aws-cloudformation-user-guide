# AWS::AutoScaling::ScalingPolicy PredictiveScalingMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification"></a>

A structure that specifies a metric specification for the `MetricSpecifications` property of the [AWS::AutoScaling::ScalingPolicy PredictiveScalingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration.html) property type\.

For more information, see [Predictive scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-predictive-scaling.html) in the *Amazon EC2 Auto Scaling User Guide*\. 

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-syntax.json"></a>

```
{
  "[PredefinedLoadMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedloadmetricspecification)" : PredictiveScalingPredefinedLoadMetric,
  "[PredefinedMetricPairSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedmetricpairspecification)" : PredictiveScalingPredefinedMetricPair,
  "[PredefinedScalingMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedscalingmetricspecification)" : PredictiveScalingPredefinedScalingMetric,
  "[TargetValue](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-syntax.yaml"></a>

```
  [PredefinedLoadMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedloadmetricspecification): 
    PredictiveScalingPredefinedLoadMetric
  [PredefinedMetricPairSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedmetricpairspecification): 
    PredictiveScalingPredefinedMetricPair
  [PredefinedScalingMetricSpecification](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedscalingmetricspecification): 
    PredictiveScalingPredefinedScalingMetric
  [TargetValue](#cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-targetvalue): Double
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification-properties"></a>

`PredefinedLoadMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedloadmetricspecification"></a>
The load metric specification\.  
If you specify `PredefinedMetricPairSpecification`, don't specify this property\.  
*Required*: No  
*Type*: [PredictiveScalingPredefinedLoadMetric](aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedloadmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedMetricPairSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedmetricpairspecification"></a>
The metric pair specification from which Amazon EC2 Auto Scaling determines the appropriate scaling metric and load metric to use\.  
With predictive scaling, you must specify either a metric pair, or a load metric and a scaling metric individually\. Specifying a metric pair instead of individual metrics provides a simpler way to configure metrics for a scaling policy\. You choose the metric pair, and the policy automatically knows the correct sum and average statistics to use for the load metric and the scaling metric\.
*Required*: No  
*Type*: [PredictiveScalingPredefinedMetricPair](aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedScalingMetricSpecification`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-predefinedscalingmetricspecification"></a>
The scaling metric specification\.  
If you specify `PredefinedMetricPairSpecification`, don't specify this property\.  
*Required*: No  
*Type*: [PredictiveScalingPredefinedScalingMetric](aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingmetricspecification-targetvalue"></a>
Specifies the target utilization\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
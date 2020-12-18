# AWS::ApplicationAutoScaling::ScalingPolicy StepAdjustment<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment"></a>

 `StepAdjustment` is a subproperty of [StepScalingPolicyConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration.html) that represents a step adjustment for a step scaling policy\. 

For the following examples, suppose that you have an alarm with a breach threshold of 50: 
+ To trigger a step adjustment when the metric is greater than or equal to 50 and less than 60, specify a lower bound of 0 and an upper bound of 10\. 
+ To trigger a step adjustment when the metric is greater than 40 and less than or equal to 50, specify a lower bound of \-10 and an upper bound of 0\. 

For more information, see [Step adjustments](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-step-scaling-policies.html#as-scaling-steps) in the *Application Auto Scaling User Guide*\.

You can find a sample template snippet in the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html#aws-resource-applicationautoscaling-scalingpolicy--examples) section of the `AWS::ApplicationAutoScaling::ScalingPolicy` documentation\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-syntax.json"></a>

```
{
  "[MetricIntervalLowerBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervallowerbound)" : Double,
  "[MetricIntervalUpperBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervalupperbound)" : Double,
  "[ScalingAdjustment](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-scalingadjustment)" : Integer
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-syntax.yaml"></a>

```
  [MetricIntervalLowerBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervallowerbound): Double
  [MetricIntervalUpperBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervalupperbound): Double
  [ScalingAdjustment](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-scalingadjustment): Integer
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-properties"></a>

`MetricIntervalLowerBound`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervallowerbound"></a>
The lower bound for the difference between the alarm threshold and the CloudWatch metric\. If the metric value is above the breach threshold, the lower bound is inclusive \(the metric must be greater than or equal to the threshold plus the lower bound\)\. Otherwise, it is exclusive \(the metric must be greater than the threshold plus the lower bound\)\. A null value indicates negative infinity\.  
You must specify at least one upper or lower bound\.  
*Required*: Conditional  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricIntervalUpperBound`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervalupperbound"></a>
The upper bound for the difference between the alarm threshold and the CloudWatch metric\. If the metric value is above the breach threshold, the upper bound is exclusive \(the metric must be less than the threshold plus the upper bound\)\. Otherwise, it is inclusive \(the metric must be less than or equal to the threshold plus the upper bound\)\. A null value indicates positive infinity\.  
You must specify at least one upper or lower bound\.  
*Required*: Conditional  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingAdjustment`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-scalingadjustment"></a>
The amount by which to scale\. The adjustment is based on the value that you specified in the `AdjustmentType` property \(either an absolute number or a percentage\)\. A positive value adds to the current capacity and a negative number subtracts from the current capacity\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
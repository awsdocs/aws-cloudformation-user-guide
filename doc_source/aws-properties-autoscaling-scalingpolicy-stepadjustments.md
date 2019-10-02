# AWS::AutoScaling::ScalingPolicy StepAdjustment<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments"></a>

 `StepAdjustments` is a subproperty of [ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html) that represents a step adjustment for a step scaling policy\. 

For the following examples, suppose that you have an alarm with a breach threshold of 50: 
+ To trigger a step adjustment when the metric is greater than or equal to 50 and less than 60, specify a lower bound of 0 and an upper bound of 10\. 
+ To trigger a step adjustment when the metric is greater than 40 and less than or equal to 50, specify a lower bound of \-10 and an upper bound of 0\. 

For more information, see [Step Adjustments](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html#as-scaling-steps) in the *Amazon EC2 Auto Scaling User Guide*\. 

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments-syntax.json"></a>

```
{
  "[MetricIntervalLowerBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervallowerbound)" : Double,
  "[MetricIntervalUpperBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervalupperbound)" : Double,
  "[ScalingAdjustment](#cfn-autoscaling-scalingpolicy-stepadjustment-scalingadjustment)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments-syntax.yaml"></a>

```
  [MetricIntervalLowerBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervallowerbound): Double
  [MetricIntervalUpperBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervalupperbound): Double
  [ScalingAdjustment](#cfn-autoscaling-scalingpolicy-stepadjustment-scalingadjustment): Integer
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments-properties"></a>

`MetricIntervalLowerBound`  <a name="cfn-autoscaling-scalingpolicy-stepadjustment-metricintervallowerbound"></a>
The lower bound for the difference between the alarm threshold and the CloudWatch metric\. If the metric value is above the breach threshold, the lower bound is inclusive \(the metric must be greater than or equal to the threshold plus the lower bound\)\. Otherwise, it is exclusive \(the metric must be greater than the threshold plus the lower bound\)\. A null value indicates negative infinity\.  
You must specify at least one upper or lower bound\.   
*Required*: Conditional  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricIntervalUpperBound`  <a name="cfn-autoscaling-scalingpolicy-stepadjustment-metricintervalupperbound"></a>
The upper bound for the difference between the alarm threshold and the CloudWatch metric\. If the metric value is above the breach threshold, the upper bound is exclusive \(the metric must be less than the threshold plus the upper bound\)\. Otherwise, it is inclusive \(the metric must be less than or equal to the threshold plus the upper bound\)\. A null value indicates positive infinity\.  
You must specify at least one upper or lower bound\.   
*Required*: Conditional  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingAdjustment`  <a name="cfn-autoscaling-scalingpolicy-stepadjustment-scalingadjustment"></a>
The amount by which to scale\. The adjustment is based on the value that you specified in the `AdjustmentType` property \(either an absolute number or a percentage\)\. A positive value adds to the current capacity and a negative number subtracts from the current capacity\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by ***all*** regions.
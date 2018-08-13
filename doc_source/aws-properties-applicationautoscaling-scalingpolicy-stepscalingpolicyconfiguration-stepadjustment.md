# Application Auto Scaling ScalingPolicy StepScalingPolicyConfiguration StepAdjustment<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment"></a>

`StepAdjustment` is a property of the [Application Auto Scaling ScalingPolicy StepScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration.md) property that configures a scaling adjustment based on the difference between the value of the aggregated CloudWatch metric and the breach threshold that you've defined for the alarm \(the size of the breach\)\. For more information, see [Step Adjustments](http://docs.aws.amazon.com/autoscaling/latest/userguide/as-scale-based-on-demand.html#as-scaling-steps) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="w3ab2c21c14c61b5"></a>

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-syntax.json"></a>

```
{
  "[MetricIntervalLowerBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervallowerbound)" : Number,
  "[MetricIntervalUpperBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervalupperbound)" : Number,
  "[ScalingAdjustment](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-scalingadjustment)" : Integer
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-syntax.yaml"></a>

```
[MetricIntervalLowerBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervallowerbound): Number
[MetricIntervalUpperBound](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervalupperbound): Number
[ScalingAdjustment](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-scalingadjustment): Integer
```

## Properties<a name="w3ab2c21c14c61b7"></a>

`MetricIntervalLowerBound`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervallowerbound"></a>
The lower bound of the breach size\. The lower bound is the difference between the breach threshold and the aggregated CloudWatch metric value\. If the metric value is within the lower and upper bounds, Application Auto Scaling triggers this step adjustment\.  
If the metric value is above the breach threshold, the metric must be greater than or equal to the threshold plus the lower bound to trigger this step adjustment \(the metric value is inclusive\)\. If the metric value is below the breach threshold, the metric must be greater than the threshold plus the lower bound to trigger this step adjustment \(the metric value is exclusive\)\. A null value indicates negative infinity\.  
*Required*: Conditional\. You must specify at least one upper or lower bound\.  
*Type*: Number

`MetricIntervalUpperBound`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-metricintervalupperbound"></a>
The upper bound of the breach size\. The upper bound is the difference between the breach threshold and the CloudWatch metric value\. If the metric value is within the lower and upper bounds, Application Auto Scaling triggers this step adjustment\.  
If the metric value is above the breach threshold, the metric must be less than the threshold plus the upper bound to trigger this step adjustment \(the metric value is exclusive\)\. If the metric value is below the breach threshold, the metric must be less than or equal to the threshold plus the upper bound to trigger this step adjustment \(the metric value is inclusive\)\. A null value indicates positive infinity\.  
*Required*: Conditional\. You must specify at least one upper or lower bound\.  
*Type*: Number

`ScalingAdjustment`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment-scalingadjustment"></a>
The amount by which to scale\. The adjustment is based on the value that you specified in the `AdjustmentType` property \(either an absolute number or a percentage\)\. A positive value adds to the current capacity and a negative number subtracts from the current capacity\.  
*Required*: Yes  
*Type*: Integer
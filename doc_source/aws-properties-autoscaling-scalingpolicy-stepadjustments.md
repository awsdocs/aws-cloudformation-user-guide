# Amazon EC2 Auto Scaling ScalingPolicy StepAdjustments<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments"></a>

`StepAdjustments` is a property of the [AWS::AutoScaling::ScalingPolicy](aws-properties-as-policy.md) resource that describes a scaling adjustment based on the difference between the value of the aggregated CloudWatch metric and the breach threshold that you've defined for the alarm\. For more information, see [StepAdjustment](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_StepAdjustment.html) in the *Amazon EC2 Auto Scaling API Reference*\.

## Syntax<a name="w3ab2c21c14d125b5"></a>

### JSON<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments-syntax.json"></a>

```
{
  "[MetricIntervalLowerBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervallowerbound)" : Number,
  "[MetricIntervalUpperBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervalupperbound)" : Number,
  "[ScalingAdjustment](#cfn-autoscaling-scalingpolicy-stepadjustment-scalingadjustment)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-stepadjustments-syntax.yaml"></a>

```
[MetricIntervalLowerBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervallowerbound): Number
[MetricIntervalUpperBound](#cfn-autoscaling-scalingpolicy-stepadjustment-metricintervalupperbound): Number
[ScalingAdjustment](#cfn-autoscaling-scalingpolicy-stepadjustment-scalingadjustment): Integer
```

## Properties<a name="w3ab2c21c14d125b7"></a>

`MetricIntervalLowerBound`  <a name="cfn-autoscaling-scalingpolicy-stepadjustment-metricintervallowerbound"></a>
The lower bound of the breach size\. The lower bound is the difference between the breach threshold and the aggregated CloudWatch metric value\. If the metric value is within the lower and upper bounds, Auto Scaling triggers this step adjustment\.  
If the metric value is above the breach threshold, the metric must be greater than or equal to the threshold plus the lower bound to trigger this step adjustment \(the metric value is inclusive\)\. If the metric value is below the breach threshold, the metric must be greater than the threshold plus the lower bound to trigger this step adjustment \(the metric value is exclusive\)\. A null value indicates negative infinity\.  
*Required*: Conditional\. You must specify at least one upper or lower bound\.  
*Type*: Number

`MetricIntervalUpperBound`  <a name="cfn-autoscaling-scalingpolicy-stepadjustment-metricintervalupperbound"></a>
The upper bound of the breach size\. The upper bound is the difference between the breach threshold and the CloudWatch metric value\. If the metric value is within the lower and upper bounds, Auto Scaling triggers this step adjustment\.  
If the metric value is above the breach threshold, the metric must be less than the threshold plus the upper bound to trigger this step adjustment \(the metric value is exclusive\)\. If the metric value is below the breach threshold, the metric must be less than or equal to the threshold plus the upper bound to trigger this step adjustment \(the metric value is inclusive\)\. A null value indicates positive infinity\.  
*Required*: Conditional\. You must specify at least one upper or lower bound\.  
*Type*: Number

`ScalingAdjustment`  <a name="cfn-autoscaling-scalingpolicy-stepadjustment-scalingadjustment"></a>
The amount by which to scale\. The adjustment is based on the value that you specified in the `AdjustmentType` property \(either an absolute number or a percentage\)\. A positive value adds to the current capacity and a negative number subtracts from the current capacity\.  
*Required*: Yes  
*Type*: Integer
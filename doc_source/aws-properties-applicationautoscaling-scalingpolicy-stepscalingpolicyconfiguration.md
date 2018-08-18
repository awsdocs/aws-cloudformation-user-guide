# Application Auto Scaling ScalingPolicy StepScalingPolicyConfiguration<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration"></a>

`StepScalingPolicyConfiguration` is a property of the [AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md) resource that configures when Application Auto Scaling scales resources up or down, and by how much\.

## Syntax<a name="w3ab2c21c14c59b5"></a>

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-syntax.json"></a>

```
{
  "[AdjustmentType](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-adjustmenttype)" : String,
  "[Cooldown](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-cooldown)" : Integer,
  "[MetricAggregationType](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-metricaggregationtype)" : String,
  "[MinAdjustmentMagnitude](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-minadjustmentmagnitude)" : Integer,
  "[StepAdjustments](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustments)" : [ [StepAdjustment](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment.md), ... ]
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-syntax.yaml"></a>

```
[AdjustmentType](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-adjustmenttype): String
[Cooldown](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-cooldown): Integer
[MetricAggregationType](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-metricaggregationtype): String
[MinAdjustmentMagnitude](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-minadjustmentmagnitude): Integer
[StepAdjustments](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustments):
  StepAdjustment
```

## Properties<a name="w3ab2c21c14c59b7"></a>

`AdjustmentType`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-adjustmenttype"></a>
Specifies whether the `ScalingAdjustment` value in the `StepAdjustment` property is an absolute number or a percentage of the current capacity\. For valid values, see the `AdjustmentType` content for the [StepScalingPolicyConfiguration](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_StepScalingPolicyConfiguration.html) data type in the *Application Auto Scaling API Reference*\.  
*Required*: No  
*Type*: String

`Cooldown`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-cooldown"></a>
The amount of time, in seconds, after a scaling activity completes before any further trigger\-related scaling activities can start\. For more information, see the `Cooldown` content for the [StepScalingPolicyConfiguration](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_StepScalingPolicyConfiguration.html) data type in the *Application Auto Scaling API Reference*\.  
*Required*: No  
*Type*: Integer

`MetricAggregationType`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-metricaggregationtype"></a>
The aggregation type for the CloudWatch metrics\. You can specify `Minimum`, `Maximum`, or `Average`\. By default, AWS CloudFormation specifies `Average`\. For more information, see [Aggregation](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/cloudwatch_concepts.html#CloudWatchAggregation) in the *Amazon CloudWatch User Guide*\.  
*Required*: No  
*Type*: String

`MinAdjustmentMagnitude`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-minadjustmentmagnitude"></a>
The minimum number of resources to adjust when a scaling activity is triggered\. If you specify `PercentChangeInCapacity` for the adjustment type, the scaling policy scales the target by this amount\.  
*Required*: No  
*Type*: Integer

`StepAdjustments`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustments"></a>
A set of adjustments that enable you to scale based on the size of the alarm breach\.  
*Required*: No  
*Type*: List of [Application Auto Scaling ScalingPolicy StepScalingPolicyConfiguration StepAdjustment](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment.md)
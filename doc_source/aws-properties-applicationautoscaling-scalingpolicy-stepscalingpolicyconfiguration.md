# AWS::ApplicationAutoScaling::ScalingPolicy StepScalingPolicyConfiguration<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration"></a>

 `StepScalingPolicyConfiguration` is a property of [ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) that specifies a step scaling policy configuration to use with Application Auto Scaling\. 

For more information, see [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\. For more information about step scaling policies, see [Step Scaling Policies](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-step-scaling-policies.html) in the *Application Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
﻿  [AdjustmentType](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-adjustmenttype) : String
﻿  [Cooldown](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-cooldown) : Integer
﻿  [MetricAggregationType](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-metricaggregationtype) : String
﻿  [MinAdjustmentMagnitude](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-minadjustmentmagnitude) : Integer
﻿  [StepAdjustments](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustments) : 
    - [StepAdjustment](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment.md)
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-properties"></a>

`AdjustmentType`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-adjustmenttype"></a>
Specifies whether the `ScalingAdjustment` value in the `StepAdjustment` property is an absolute number or a percentage of the current capacity\.   
*Required*: No  
*Type*: String  
*Allowed Values*: `ChangeInCapacity | ExactCapacity | PercentChangeInCapacity`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cooldown`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-cooldown"></a>
The amount of time, in seconds, after a scaling activity completes where previous trigger\-related scaling activities can influence future scaling events\.  
For scale\-out policies, while the cooldown period is in effect, the capacity that has been added by the previous scale\-out event that initiated the cooldown is calculated as part of the desired capacity for the next scale out\. The intention is to continuously \(but not excessively\) scale out\. For example, an alarm triggers a step scaling policy to scale out an Amazon ECS service by 2 tasks, the scaling activity completes successfully, and a cooldown period of 5 minutes starts\. During the cooldown period, if the alarm triggers the same policy again but at a more aggressive step adjustment to scale out the service by 3 tasks, the 2 tasks that were added in the previous scale\-out event are considered part of that capacity and only 1 additional task is added to the desired count\.  
For scale\-in policies, the cooldown period is used to block subsequent scale\-in requests until it has expired\. The intention is to scale in conservatively to protect your application's availability\. However, if another alarm triggers a scale\-out policy during the cooldown period after a scale\-in, Application Auto Scaling scales out your scalable target immediately\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricAggregationType`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-metricaggregationtype"></a>
The aggregation type for the CloudWatch metrics\. Valid values are `Minimum`, `Maximum`, and `Average`\. If the aggregation type is null, the value is treated as `Average`\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `Average | Maximum | Minimum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinAdjustmentMagnitude`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-minadjustmentmagnitude"></a>
The minimum number to adjust your scalable dimension as a result of a scaling activity\. If the adjustment type is `PercentChangeInCapacity`, the scaling policy changes the scalable dimension of the scalable target by this amount\.  
For example, suppose that you create a step scaling policy to scale out an Amazon ECS service by 25 percent and you specify a `MinAdjustmentMagnitude` of 2\. If the service has 4 tasks and the scaling policy is performed, 25 percent of 4 is 1\. However, because you specified a `MinAdjustmentMagnitude` of 2, Application Auto Scaling scales out the service by 2 tasks\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepAdjustments`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustments"></a>
A set of adjustments that enable you to scale based on the size of the alarm breach\.  
*Required*: No  
*Type*: List of [StepAdjustment](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration-stepadjustment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
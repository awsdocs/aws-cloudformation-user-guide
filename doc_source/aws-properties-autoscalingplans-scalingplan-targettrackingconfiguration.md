# AWS Auto Scaling ScalingPlan TargetTrackingConfiguration<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration"></a>

<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-description"></a>The `TargetTrackingConfiguration` property type specifies a target tracking policy for an AWS Auto Scaling scaling plan\.

<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-inheritance"></a> `TargetTrackingConfiguration` is a property of the [AWS Auto Scaling ScalingPlan ScalingInstruction](aws-properties-autoscalingplans-scalingplan-scalinginstruction.md) property type\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-syntax.json"></a>

```
{
  "[ScaleOutCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleoutcooldown)" : Integer,
  "[TargetValue](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-targetvalue)" : Double,
  "[PredefinedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-predefinedscalingmetricspecification)" : [*PredefinedScalingMetricSpecification*](aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification.md),
  "[DisableScaleIn](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-disablescalein)" : Boolean,
  "[ScaleInCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleincooldown)" : Integer,
  "[EstimatedInstanceWarmup](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-estimatedinstancewarmup)" : Integer,
  "[CustomizedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-customizedscalingmetricspecification)" : [*CustomizedScalingMetricSpecification*](aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification.md)
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-syntax.yaml"></a>

```
[ScaleOutCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleoutcooldown): Integer
[TargetValue](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-targetvalue): Double
[PredefinedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-predefinedscalingmetricspecification): [*PredefinedScalingMetricSpecification*](aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification.md)
[DisableScaleIn](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-disablescalein): Boolean
[ScaleInCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleincooldown): Integer
[EstimatedInstanceWarmup](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-estimatedinstancewarmup): Integer
[CustomizedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-customizedscalingmetricspecification): [*CustomizedScalingMetricSpecification*](aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification.md)
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-properties"></a>

`CustomizedScalingMetricSpecification`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-customizedscalingmetricspecification"></a>
A customized metric\.  
 *Required*: No  
 *Type*: [AWS Auto Scaling ScalingPlan CustomizedScalingMetricSpecification](aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DisableScaleIn`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-disablescalein"></a>
Indicates whether scale in by the target tracking policy is disabled\. If the value is true, scale in is disabled and the target tracking policy won't remove capacity from the scalable resource\. Otherwise, scale in is enabled and the target tracking policy can remove capacity from the scalable resource\. The default value is false\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`EstimatedInstanceWarmup`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-estimatedinstancewarmup"></a>
The estimated time, in seconds, until a newly launched instance can contribute to the CloudWatch metrics\. This value is used only if the resource is an Auto Scaling group\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PredefinedScalingMetricSpecification`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-predefinedscalingmetricspecification"></a>
A predefined metric\.  
 *Required*: No  
 *Type*: [AWS Auto Scaling ScalingPlan PredefinedScalingMetricSpecification](aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScaleInCooldown`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleincooldown"></a>
The amount of time, in seconds, after a scale in activity completes before another scale in activity can start\. This value is not used if the scalable resource is an Auto Scaling group\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScaleOutCooldown`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleoutcooldown"></a>
The amount of time, in seconds, after a scale out activity completes before another scale out activity can start\. This value is not used if the scalable resource is an Auto Scaling group\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetValue`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-targetvalue"></a>
The target value for the metric\. The range is 8\.515920e\-109 to 1\.174271e\+108 \(Base 10\) or 2e\-360 to 2e360 \(Base 2\)\.  
 *Required*: Yes  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
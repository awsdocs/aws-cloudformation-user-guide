# Application Auto Scaling ScalingPolicy TargetTrackingScalingPolicyConfiguration<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration"></a>

Use the `TargetTrackingScalingPolicyConfiguration` property to configure a target tracking scaling policy\. Use it to adjust upward or downward in response to actual workloads, so that capacity utilization remains at or near your target utilization\. `TargetTrackingScalingPolicyConfiguration` is a property of the [AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md) resource\. For more information, see [PutScalingPolicy](http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax.json"></a>

```
{
  "[CustomizedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification)" : [CustomizedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification.md),
  "[DisableScaleIn](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-disablescalein)" : Boolean,
  "[PredefinedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification)" : [PredefinedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification.md),
  "[ScaleInCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown)" : Integer,
  "[ScaleOutCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown)" : Integer,
  "[TargetValue](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax.yaml"></a>

```
[CustomizedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification):
  [CustomizedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification.md)
[PredefinedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification):
  [PredefinedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification.md)
[DisableScaleIn](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-disablescalein): Boolean
[ScaleInCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown): Integer
[ScaleOutCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown): Integer
[TargetValue](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-properties"></a>

For more information about each property, including constraints and valid values, see [TargetTrackingScalingPolicyConfiguration](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_TargetTrackingScalingPolicyConfiguration.html) in the *Application Auto Scaling API Reference*\.

`CustomizedMetricSpecification`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification"></a>
This property is reserved for future use\.  
*Required*: No  
*Type*: [Application Auto Scaling ScalingPolicy CustomizedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DisableScaleIn`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-disablescalein"></a>
Indicates whether scale in by the target tracking policy is disabled\. If the value is `true`, scale in is disabled and the target tracking policy won't remove capacity from the scalable resource\. Otherwise, scale in is enabled and the target tracking policy can remove capacity from the scalable resource\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PredefinedMetricSpecification`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification"></a>
A predefined metric\.  
*Required*: No  
*Type*: [Application Auto Scaling ScalingPolicy PredefinedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ScaleInCooldown`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown"></a>
The amount of time, in seconds, after a scale in activity completes before another scale in activity can start\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ScaleOutCooldown`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown"></a>
The amount of time, in seconds, after a scale out activity completes before another scale out activity can start\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetValue`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue"></a>
The target value for the metric\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
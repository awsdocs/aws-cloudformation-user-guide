# AWS::ApplicationAutoScaling::ScalingPolicy TargetTrackingScalingPolicyConfiguration<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration"></a>

 `TargetTrackingScalingPolicyConfiguration` is a property of the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource that specifies a target tracking scaling policy configuration for Application Auto Scaling\. Use a target tracking scaling policy to adjust the capacity of the specified scalable target in response to actual workloads, so that resource utilization remains at or near the target utilization value\. 

For more information, see [Target tracking scaling policies](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html) in the *Application Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax.json"></a>

```
{
  "[CustomizedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification)" : CustomizedMetricSpecification,
  "[DisableScaleIn](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-disablescalein)" : Boolean,
  "[PredefinedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification)" : PredefinedMetricSpecification,
  "[ScaleInCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown)" : Integer,
  "[ScaleOutCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown)" : Integer,
  "[TargetValue](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax.yaml"></a>

```
  [CustomizedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification): 
    CustomizedMetricSpecification
  [DisableScaleIn](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-disablescalein): Boolean
  [PredefinedMetricSpecification](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification): 
    PredefinedMetricSpecification
  [ScaleInCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown): Integer
  [ScaleOutCooldown](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown): Integer
  [TargetValue](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-properties"></a>

`CustomizedMetricSpecification`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification"></a>
A customized metric\. You can specify either a predefined metric or a customized metric\.  
*Required*: No  
*Type*: [CustomizedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableScaleIn`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-disablescalein"></a>
Indicates whether scale in by the target tracking scaling policy is disabled\. If the value is `true`, scale in is disabled and the target tracking scaling policy won't remove capacity from the scalable target\. Otherwise, scale in is enabled and the target tracking scaling policy can remove capacity from the scalable target\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedMetricSpecification`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification"></a>
A predefined metric\. You can specify either a predefined metric or a customized metric\.  
*Required*: No  
*Type*: [PredefinedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleInCooldown`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown"></a>
The amount of time, in seconds, after a scale\-in activity completes before another scale\-in activity can start\. For more information and for default values, see [Define cooldown periods](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html#target-tracking-cooldown) in the *Application Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleOutCooldown`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown"></a>
The amount of time, in seconds, to wait for a previous scale\-out activity to take effect\. For more information and for default values, see [Define cooldown periods](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html#target-tracking-cooldown) in the *Application Auto Scaling User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue"></a>
The target value for the metric\. Although this property accepts numbers of type Double, it won't accept values that are either too small or too large\. Values must be in the range of \-2^360 to 2^360\. The value must be a valid number based on the choice of metric\. For example, if the metric is CPU utilization, then the target value is a percent value that represents how much of the CPU can be used before scaling out\.   
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration--seealso"></a>
+ [Application Auto Scaling template examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html#scenario-app-as-template-examples)
+ [Getting started](https://docs.aws.amazon.com/autoscaling/application/userguide/getting-started.html) in the *Application Auto Scaling User Guide*


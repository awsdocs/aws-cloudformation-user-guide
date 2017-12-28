# Application Auto Scaling ScalingPolicy TargetTrackingScalingPolicyConfiguration<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration"></a>

Use the `TargetTrackingScalingPolicyConfiguration` property to configure a target tracking scaling policy\. Use it to adjust upward or downward in response to actual workloads, so that capacity utilization remains at or near your target utilization\. `TargetTrackingScalingPolicyConfiguration` is a property of the [AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md) resource\. For more information, see [PutScalingPolicy](http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification)" : CustomizedMetricSpecification,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification)" : PredefinedMetricSpecification,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-customizedmetricspecification):
  CustomizedMetricSpecification
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-predefinedmetricspecification):
  PredefinedMetricSpecification
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleincooldown): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-properties"></a>

For more information about each property, including constraints and valid values, see [TargetTrackingScalingPolicyConfiguration](http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_TargetTrackingScalingPolicyConfiguration.html) in the *Application Auto Scaling API Reference*\.

`CustomizedMetricSpecification`  
This property is reserved for future use\.  
*Required: *No  
*Type*: [Application Auto Scaling ScalingPolicy CustomizedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification.md)  
*Update requires*: No interruption

`PredefinedMetricSpecification`  
A predefined metric\.  
*Required: *No  
*Type*: [Application Auto Scaling ScalingPolicy PredefinedMetricSpecification](aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification.md)  
*Update requires*: No interruption

`ScaleInCooldown`  
The amount of time, in seconds, after a scale in activity completes before another scale in activity can start\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`ScaleOutCooldown`  
The amount of time, in seconds, after a scale out activity completes before another scale out activity can start\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`TargetValue`  
The target value for the metric\.  
*Required: *Yes  
*Type*: Double  
*Update requires*: No interruption
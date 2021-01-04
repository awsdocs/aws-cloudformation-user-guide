# AWS::AutoScalingPlans::ScalingPlan TargetTrackingConfiguration<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration"></a>

 `TargetTrackingConfiguration` is a subproperty of [ScalingInstruction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-scalinginstruction.html) that specifies a target tracking configuration to use with AWS Auto Scaling\. 

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-syntax.json"></a>

```
{
  "[CustomizedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-customizedscalingmetricspecification)" : CustomizedScalingMetricSpecification,
  "[DisableScaleIn](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-disablescalein)" : Boolean,
  "[EstimatedInstanceWarmup](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-estimatedinstancewarmup)" : Integer,
  "[PredefinedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-predefinedscalingmetricspecification)" : PredefinedScalingMetricSpecification,
  "[ScaleInCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleincooldown)" : Integer,
  "[ScaleOutCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleoutcooldown)" : Integer,
  "[TargetValue](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-syntax.yaml"></a>

```
  [CustomizedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-customizedscalingmetricspecification): 
    CustomizedScalingMetricSpecification
  [DisableScaleIn](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-disablescalein): Boolean
  [EstimatedInstanceWarmup](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-estimatedinstancewarmup): Integer
  [PredefinedScalingMetricSpecification](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-predefinedscalingmetricspecification): 
    PredefinedScalingMetricSpecification
  [ScaleInCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleincooldown): Integer
  [ScaleOutCooldown](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleoutcooldown): Integer
  [TargetValue](#cfn-autoscalingplans-scalingplan-targettrackingconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration-properties"></a>

`CustomizedScalingMetricSpecification`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-customizedscalingmetricspecification"></a>
A customized metric\. You can specify either a predefined metric or a customized metric\.   
*Required*: No  
*Type*: [CustomizedScalingMetricSpecification](aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableScaleIn`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-disablescalein"></a>
Indicates whether scale in by the target tracking scaling policy is disabled\. If the value is `true`, scale in is disabled and the target tracking scaling policy doesn't remove capacity from the scalable resource\. Otherwise, scale in is enabled and the target tracking scaling policy can remove capacity from the scalable resource\.   
The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EstimatedInstanceWarmup`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-estimatedinstancewarmup"></a>
The estimated time, in seconds, until a newly launched instance can contribute to the CloudWatch metrics\. This value is used only if the resource is an Auto Scaling group\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedScalingMetricSpecification`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-predefinedscalingmetricspecification"></a>
A predefined metric\. You can specify either a predefined metric or a customized metric\.  
*Required*: No  
*Type*: [PredefinedScalingMetricSpecification](aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleInCooldown`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleincooldown"></a>
The amount of time, in seconds, after a scale\-in activity completes before another scale in activity can start\. This value is not used if the scalable resource is an Auto Scaling group\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleOutCooldown`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-scaleoutcooldown"></a>
The amount of time, in seconds, after a scale\-out activity completes before another scale\-out activity can start\. This value is not used if the scalable resource is an Auto Scaling group\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-autoscalingplans-scalingplan-targettrackingconfiguration-targetvalue"></a>
The target value for the metric\. Although this property accepts numbers of type Double, it won't accept values that are either too small or too large\. Values must be in the range of \-2^360 to 2^360\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration--seealso"></a>
+ [AWS Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html)
# AWS::ApplicationAutoScaling::ScalingPolicy TargetTrackingScalingPolicyConfiguration<a name="aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration"></a>

 `TargetTrackingScalingPolicyConfiguration` is a property of [ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) that specifies a target tracking scaling policy to use with Application Auto Scaling\. Use a target tracking scaling policy to adjust the capacity of the specified scalable target in response to actual workloads, so that resource utilization remains at or near the target utilization value\. 

For more information, see [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\. For more information about target tracking scaling policies, see [Target tracking scaling policies](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html) in the *Application Auto Scaling User Guide*\.

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
The amount of time, in seconds, after a scale\-in activity completes before another scale\-in activity can start\.  
With the *scale\-in cooldown period*, the intention is to scale in conservatively to protect your application’s availability, so scale\-in activities are blocked until the cooldown period has expired\. However, if another alarm triggers a scale\-out activity during the scale\-in cooldown period, Application Auto Scaling scales out the target immediately\. In this case, the scale\-in cooldown period stops and doesn't complete\.  
Application Auto Scaling provides a default value of 300 for the following scalable targets:  
+ ECS services
+ Spot Fleet requests
+ EMR clusters
+ AppStream 2\.0 fleets
+ Aurora DB clusters
+ Amazon SageMaker endpoint variants
+ Custom resources
For all other scalable targets, the default value is 0:  
+ DynamoDB tables
+ DynamoDB global secondary indexes
+ Amazon Comprehend document classification and entity recognizer endpoints
+ Lambda provisioned concurrency
+ Amazon Keyspaces tables
+ Amazon MSK cluster storage
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleOutCooldown`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-scaleoutcooldown"></a>
The amount of time, in seconds, to wait for a previous scale\-out activity to take effect\.  
With the *scale\-out cooldown period*, the intention is to continuously \(but not excessively\) scale out\. After Application Auto Scaling successfully scales out using a target tracking scaling policy, it starts to calculate the cooldown time\. The scaling policy won't increase the desired capacity again unless either a larger scale out is triggered or the cooldown period ends\. While the cooldown period is in effect, the capacity added by the initiating scale\-out activity is calculated as part of the desired capacity for the next scale\-out activity\.  
Application Auto Scaling provides a default value of 300 for the following scalable targets:  
+ ECS services
+ Spot Fleet requests
+ EMR clusters
+ AppStream 2\.0 fleets
+ Aurora DB clusters
+ Amazon SageMaker endpoint variants
+ Custom resources
For all other scalable targets, the default value is 0:  
+ DynamoDB tables
+ DynamoDB global secondary indexes
+ Amazon Comprehend document classification and entity recognizer endpoints
+ Lambda provisioned concurrency
+ Amazon Keyspaces tables
+ Amazon MSK cluster storage
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration-targetvalue"></a>
The target value for the metric\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
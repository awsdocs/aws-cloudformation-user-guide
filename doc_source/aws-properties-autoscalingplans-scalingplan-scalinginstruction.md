# AWS Auto Scaling ScalingPlan ScalingInstruction<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction"></a>

<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-description"></a>The `ScalingInstruction` property type specifies the scaling configuration for a scalable resource in an AWS Auto Scaling scaling plan\.

<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-inheritance"></a> `ScalingInstruction` is a property of the [AWS::AutoScalingPlans::ScalingPlan](aws-resource-autoscalingplans-scalingplan.md) resource\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-syntax.json"></a>

```
{
  "[CustomizedLoadMetricSpecification](#cfn-autoscalingplans-scalingplan-scalinginstruction-customizedloadmetricspecification)" : [*CustomizedLoadMetricSpecification*](aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification.md),
  "[DisableDynamicScaling](#cfn-autoscalingplans-scalingplan-scalinginstruction-disabledynamicscaling)" : Boolean,
  "[MaxCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-maxcapacity)" : Integer,
  "[MinCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-mincapacity)" : Integer,
  "[PredefinedLoadMetricSpecification](#cfn-autoscalingplans-scalingplan-scalinginstruction-predefinedloadmetricspecification)" : [*PredefinedLoadMetricSpecification*](aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification.md),
  "[PredictiveScalingMaxCapacityBehavior](#cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmaxcapacitybehavior)" : String,
  "[PredictiveScalingMaxCapacityBuffer](#cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmaxcapacitybuffer)" : Integer,
  "[PredictiveScalingMode](#cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmode)" : String,
  "[ResourceId](#cfn-autoscalingplans-scalingplan-scalinginstruction-resourceid)" : String,
  "[ScalableDimension](#cfn-autoscalingplans-scalingplan-scalinginstruction-scalabledimension)" : String,
  "[ScalingPolicyUpdateBehavior](#cfn-autoscalingplans-scalingplan-scalinginstruction-scalingpolicyupdatebehavior)" : String,
  "[ScheduledActionBufferTime](#cfn-autoscalingplans-scalingplan-scalinginstruction-scheduledactionbuffertime)" : Integer,
  "[ServiceNamespace](#cfn-autoscalingplans-scalingplan-scalinginstruction-servicenamespace)" : String,
  "[TargetTrackingConfigurations](#cfn-autoscalingplans-scalingplan-scalinginstruction-targettrackingconfigurations)" : [ [*TargetTrackingConfiguration*](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md), ... ]
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-syntax.yaml"></a>

```
[CustomizedLoadMetricSpecification](#cfn-autoscalingplans-scalingplan-scalinginstruction-customizedloadmetricspecification): 
  [*CustomizedLoadMetricSpecification*](aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification.md)
[DisableDynamicScaling](#cfn-autoscalingplans-scalingplan-scalinginstruction-disabledynamicscaling): Boolean
[MaxCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-maxcapacity): Integer
[MinCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-mincapacity): Integer
[PredefinedLoadMetricSpecification](#cfn-autoscalingplans-scalingplan-scalinginstruction-predefinedloadmetricspecification): 
  [*PredefinedLoadMetricSpecification*](aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification.md)
[PredictiveScalingMaxCapacityBehavior](#cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmaxcapacitybehavior): String
[PredictiveScalingMaxCapacityBuffer](#cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmaxcapacitybuffer): Integer
[PredictiveScalingMode](#cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmode): String
[ResourceId](#cfn-autoscalingplans-scalingplan-scalinginstruction-resourceid): String
[ScalableDimension](#cfn-autoscalingplans-scalingplan-scalinginstruction-scalabledimension): String
[ScalingPolicyUpdateBehavior](#cfn-autoscalingplans-scalingplan-scalinginstruction-scalingpolicyupdatebehavior): String
[ScheduledActionBufferTime](#cfn-autoscalingplans-scalingplan-scalinginstruction-scheduledactionbuffertime): Integer
[ServiceNamespace](#cfn-autoscalingplans-scalingplan-scalinginstruction-servicenamespace): String
[TargetTrackingConfigurations](#cfn-autoscalingplans-scalingplan-scalinginstruction-targettrackingconfigurations): 
  - [*TargetTrackingConfiguration*](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md)
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-properties"></a>

For more information about each property, including constraints and valid values, see [ScalingInstruction](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_ScalingInstruction.html) in the *AWS Auto Scaling API Reference*\.

`CustomizedLoadMetricSpecification`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-customizedloadmetricspecification"></a>
The customized load metric to use for predictive scaling\. This parameter or a **PredefinedLoadMetricSpecification** is required when configuring predictive scaling, and cannot be used otherwise\.   
 *Required*: No  
 *Type*: [CustomizedLoadMetricSpecification](aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DisableDynamicScaling`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-disabledynamicscaling"></a>
Controls whether dynamic scaling by AWS Auto Scaling is disabled\. When dynamic scaling is enabled, AWS Auto Scaling creates target tracking scaling policies based on the specified target tracking configurations\.   
The default is enabled \(`false`\)\.   
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxCapacity`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-maxcapacity"></a>
The maximum capacity of the resource\. The exception to this upper limit is if you specify a non\-default setting for **PredictiveScalingMaxCapacityBehavior**\.   
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MinCapacity`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-mincapacity"></a>
The minimum capacity of the resource\.   
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PredefinedLoadMetricSpecification`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-predefinedloadmetricspecification"></a>
The predefined load metric to use for predictive scaling\. This parameter or a **CustomizedLoadMetricSpecification** is required when configuring predictive scaling, and cannot be used otherwise\.   
 *Required*: No  
 *Type*: [PredefinedLoadMetricSpecification](aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification.md)   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PredictiveScalingMaxCapacityBehavior`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmaxcapacitybehavior"></a>
Defines the behavior that should be applied if the forecast capacity approaches or exceeds the maximum capacity specified for the resource\. The default value is `SetForecastCapacityToMaxCapacity`\.  
The following are possible values:  
+ `SetForecastCapacityToMaxCapacity` \- AWS Auto Scaling cannot scale resource capacity higher than the maximum capacity\. The maximum capacity is enforced as a hard limit\. 
+ `SetMaxCapacityToForecastCapacity` \- AWS Auto Scaling may scale resource capacity higher than the maximum capacity to equal but not exceed forecast capacity\.
+ `SetMaxCapacityAboveForecastCapacity` \- AWS Auto Scaling may scale resource capacity higher than the maximum capacity by a specified buffer value\. The intention is to give the target tracking scaling policy extra capacity if unexpected traffic occurs\. 
Only valid when configuring predictive scaling\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PredictiveScalingMaxCapacityBuffer`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmaxcapacitybuffer"></a>
The size of the capacity buffer to use when the forecast capacity is close to or exceeds the maximum capacity\. The value is specified as a percentage relative to the forecast capacity\. For example, if the buffer is 10, this means a 10 percent buffer, such that if the forecast capacity is 50, and the maximum capacity is 40, then the effective maximum capacity is 55\.  
Only valid when configuring predictive scaling\. Required if the **PredictiveScalingMaxCapacityBehavior** is set to `SetMaxCapacityAboveForecastCapacity`, and cannot be used otherwise\.  
The range is 1\-100\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PredictiveScalingMode`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-predictivescalingmode"></a>
The predictive scaling mode\. The default value is `ForecastAndScale`\. Otherwise, AWS Auto Scaling forecasts capacity but does not create any scheduled scaling actions based on the capacity forecast\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResourceId`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-resourceid"></a>
The ID of the resource\. For examples, see [ScalingInstruction](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_ScalingInstruction.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScalableDimension`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-scalabledimension"></a>
The scalable dimension associated with the resource\. For a list of values, see [ScalingInstruction](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_ScalingInstruction.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScalingPolicyUpdateBehavior`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-scalingpolicyupdatebehavior"></a>
Controls whether a resource's externally created scaling policies are kept or replaced\.   
The default value is `KeepExternalPolicies`\. If the parameter is set to `ReplaceExternalPolicies`, any scaling policies that are external to AWS Auto Scaling are deleted and new target tracking scaling policies created\.   
Only valid when configuring dynamic scaling\.   
Condition: The number of existing policies to be replaced must be less than or equal to 50\. If there are more than 50 policies to be replaced, AWS Auto Scaling keeps all existing policies and does not create new ones\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScheduledActionBufferTime`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-scheduledactionbuffertime"></a>
The amount of time, in seconds, to buffer the run time of scheduled scaling actions when scaling out\. For example, if the forecast says to add capacity at 10:00 AM, and the buffer time is 5 minutes, then the run time of the corresponding scheduled scaling action will be 9:55 AM\. The intention is to give resources time to be provisioned\. For example, it can take a few minutes to launch an EC2 instance\. The actual amount of time required depends on several factors, such as the size of the instance and whether there are startup scripts to complete\.   
The value must be less than forecast interval duration of 3600 seconds \(60 minutes\)\. The default is 300 seconds\.   
Only valid when configuring predictive scaling\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceNamespace`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-servicenamespace"></a>
The namespace of the AWS service\. For a list of values, see [ScalingInstruction](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_ScalingInstruction.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetTrackingConfigurations`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-targettrackingconfigurations"></a>
The structure that defines new target tracking configurations \(up to 10\)\. Each of these structures includes a specific scaling metric and a target value for the metric, along with various parameters to use with dynamic scaling\.   
With predictive scaling and dynamic scaling, the resource scales based on the target tracking configuration that provides the largest capacity for both scale in and scale out\.   
Condition: The scaling metric must be unique across target tracking configurations\.  
 *Required*: Yes  
 *Type*: List of [TargetTrackingConfiguration](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
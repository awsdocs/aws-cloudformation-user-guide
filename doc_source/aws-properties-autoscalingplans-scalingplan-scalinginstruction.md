# AWS Auto Scaling ScalingPlan ScalingInstruction<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction"></a>

<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-description"></a>The `ScalingInstruction` property type specifies the scaling configuration for a scalable resource in an AWS Auto Scaling scaling plan\.

<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-inheritance"></a> `ScalingInstruction` is a property of the [AWS::AutoScalingPlans::ScalingPlan](aws-resource-autoscalingplans-scalingplan.md) resource\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-syntax.json"></a>

```
{
  "[ResourceId](#cfn-autoscalingplans-scalingplan-scalinginstruction-resourceid)" : String,
  "[ServiceNamespace](#cfn-autoscalingplans-scalingplan-scalinginstruction-servicenamespace)" : String,
  "[ScalableDimension](#cfn-autoscalingplans-scalingplan-scalinginstruction-scalabledimension)" : String,
  "[MinCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-mincapacity)" : Integer,
  "[TargetTrackingConfigurations](#cfn-autoscalingplans-scalingplan-scalinginstruction-targettrackingconfigurations)" : [ [*TargetTrackingConfiguration*](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md), ... ],
  "[MaxCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-maxcapacity)" : Integer
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-syntax.yaml"></a>

```
[ResourceId](#cfn-autoscalingplans-scalingplan-scalinginstruction-resourceid): String
[ServiceNamespace](#cfn-autoscalingplans-scalingplan-scalinginstruction-servicenamespace): String
[ScalableDimension](#cfn-autoscalingplans-scalingplan-scalinginstruction-scalabledimension): String
[MinCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-mincapacity): Integer
[TargetTrackingConfigurations](#cfn-autoscalingplans-scalingplan-scalinginstruction-targettrackingconfigurations): 
  - [*TargetTrackingConfiguration*](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md)
[MaxCapacity](#cfn-autoscalingplans-scalingplan-scalinginstruction-maxcapacity): Integer
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-scalinginstruction-properties"></a>

`MaxCapacity`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-maxcapacity"></a>
The maximum value to scale to in response to a scale in event\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MinCapacity`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-mincapacity"></a>
The minimum value to scale to in response to a scale out event\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResourceId`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-resourceid"></a>
The ID of the resource\. For examples, see [ScalingInstruction](http://docs.aws.amazon.com/autoscaling/plans/APIReference/API_ScalingInstruction.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScalableDimension`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-scalabledimension"></a>
The scalable dimension associated with the resource\. For a list of values, see [ScalingInstruction](http://docs.aws.amazon.com/autoscaling/plans/APIReference/API_ScalingInstruction.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceNamespace`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-servicenamespace"></a>
The namespace of the AWS service\. For a list of values, see [ScalingInstruction](http://docs.aws.amazon.com/autoscaling/plans/APIReference/API_ScalingInstruction.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetTrackingConfigurations`  <a name="cfn-autoscalingplans-scalingplan-scalinginstruction-targettrackingconfigurations"></a>
The target tracking scaling policies \(up to 10\)\.  
 *Required*: Yes  
 *Type*: List of [AWS Auto Scaling ScalingPlan TargetTrackingConfiguration](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
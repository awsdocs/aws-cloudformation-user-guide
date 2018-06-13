# AWS::AutoScalingPlans::ScalingPlan<a name="aws-resource-autoscalingplans-scalingplan"></a>

Creates a scaling plan for AWS Auto Scaling\. For more information, see the [AWS Auto Scaling User Guide](http://docs.aws.amazon.com/autoscaling/plans/userguide/)\.

## Syntax<a name="aws-resource-autoscalingplans-scalingplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscalingplans-scalingplan-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScalingPlans::ScalingPlan",
  "Properties" : {
    "[ApplicationSource](#cfn-autoscalingplans-scalingplan-applicationsource)" : [*ApplicationSource*](aws-properties-autoscalingplans-scalingplan-applicationsource.md),
    "[ScalingInstructions](#cfn-autoscalingplans-scalingplan-scalinginstructions)" : [ [*ScalingInstruction*](aws-properties-autoscalingplans-scalingplan-scalinginstruction.md), ... ]
  }
}
```

### YAML<a name="aws-resource-autoscalingplans-scalingplan-syntax.yaml"></a>

```
Type: "AWS::AutoScalingPlans::ScalingPlan"
Properties:
  [ApplicationSource](#cfn-autoscalingplans-scalingplan-applicationsource): [*ApplicationSource*](aws-properties-autoscalingplans-scalingplan-applicationsource.md)
  [ScalingInstructions](#cfn-autoscalingplans-scalingplan-scalinginstructions): 
    - [*ScalingInstruction*](aws-properties-autoscalingplans-scalingplan-scalinginstruction.md)
```

## Properties<a name="aws-resource-autoscalingplans-scalingplan-properties"></a>

`ApplicationSource`  <a name="cfn-autoscalingplans-scalingplan-applicationsource"></a>
A CloudFormation stack or a set of tags\. You can create one scaling plan per application source\.  
 *Required*: Yes  
 *Type*: [AWS Auto Scaling ScalingPlan ApplicationSource](aws-properties-autoscalingplans-scalingplan-applicationsource.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScalingInstructions`  <a name="cfn-autoscalingplans-scalingplan-scalinginstructions"></a>
The scaling instructions\.  
 *Required*: Yes  
 *Type*: List of [AWS Auto Scaling ScalingPlan ScalingInstruction](aws-properties-autoscalingplans-scalingplan-scalinginstruction.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-autoscalingplans-scalingplan-returnvalues"></a>

### Ref<a name="aws-resource-autoscalingplans-scalingplan-ref"></a>

When you pass the logical ID of an `AWS::AutoScalingPlans::ScalingPlan` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the scaling plan\. The format of the ARN is as follows:

```
arn:aws:autoscaling:region:123456789012:scalingPlan:scalingPlanName/plan-name:scalingPlanVersion/plan-version
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 
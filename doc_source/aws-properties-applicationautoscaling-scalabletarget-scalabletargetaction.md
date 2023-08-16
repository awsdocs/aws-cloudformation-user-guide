# AWS::ApplicationAutoScaling::ScalableTarget ScalableTargetAction<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction"></a>

 `ScalableTargetAction` specifies the minimum and maximum capacity for the `ScalableTargetAction` property of the [AWS::ApplicationAutoScaling::ScalableTarget ScheduledAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalabletarget-scheduledaction.html) property type\.

## Syntax<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-syntax.json"></a>

```
{
  "[MaxCapacity](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-maxcapacity)" : Integer,
  "[MinCapacity](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-mincapacity)" : Integer
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-syntax.yaml"></a>

```
  [MaxCapacity](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-maxcapacity): Integer
  [MinCapacity](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-mincapacity): Integer
```

## Properties<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-properties"></a>

`MaxCapacity`  <a name="cfn-applicationautoscaling-scalabletarget-scalabletargetaction-maxcapacity"></a>
The maximum capacity\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacity`  <a name="cfn-applicationautoscaling-scalabletarget-scalabletargetaction-mincapacity"></a>
The minimum capacity\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction--seealso"></a>
+ [Application Auto Scaling template examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html#scenario-app-as-template-examples)
+ [Getting started](https://docs.aws.amazon.com/autoscaling/application/userguide/getting-started.html) in the *Application Auto Scaling User Guide*


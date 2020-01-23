# AWS::ApplicationAutoScaling::ScalableTarget ScalableTargetAction<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction"></a>

 `ScalableTargetAction` is a subproperty of [ScheduledAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalabletarget-scheduledaction.html) that represents the minimum and maximum capacity for a scheduled action\. 

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

## See Also<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction--seealso"></a>
+ [Application Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/application/userguide/what-is-application-auto-scaling.html) 
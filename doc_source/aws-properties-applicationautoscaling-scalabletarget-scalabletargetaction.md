# Application Auto Scaling ScalableTarget ScalableTargetAction<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction"></a>

<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-description"></a>The `ScalableTargetAction` property type specifies the minimum and maximum capacity of a scheduled action for an Application Auto Scaling scalable target\.

<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-inheritance"></a> `ScalableTargetAction` is a property of the [Application Auto Scaling ScalableTarget ScheduledAction](aws-properties-applicationautoscaling-scalabletarget-scheduledaction.md) property type\.

## Syntax<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-maxcapacity)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-mincapacity)" : Integer
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-maxcapacity): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalabletarget-scalabletargetaction-mincapacity): Integer
```

## Properties<a name="aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction-properties"></a>

`MaxCapacity`  
The maximum capacity\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: No interruption 

`MinCapacity`  
The minimum capacity\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: No interruption 
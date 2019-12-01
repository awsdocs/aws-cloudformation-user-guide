# AWS::ApplicationAutoScaling::ScalableTarget SuspendedState<a name="aws-properties-applicationautoscaling-scalabletarget-suspendedstate"></a>

Specifies whether the scaling activities for a scalable target are in a suspended state\. 

## Syntax<a name="aws-properties-applicationautoscaling-scalabletarget-suspendedstate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalabletarget-suspendedstate-syntax.json"></a>

```
{
  "[DynamicScalingInSuspended](#cfn-applicationautoscaling-scalabletarget-suspendedstate-dynamicscalinginsuspended)" : Boolean,
  "[DynamicScalingOutSuspended](#cfn-applicationautoscaling-scalabletarget-suspendedstate-dynamicscalingoutsuspended)" : Boolean,
  "[ScheduledScalingSuspended](#cfn-applicationautoscaling-scalabletarget-suspendedstate-scheduledscalingsuspended)" : Boolean
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalabletarget-suspendedstate-syntax.yaml"></a>

```
  [DynamicScalingInSuspended](#cfn-applicationautoscaling-scalabletarget-suspendedstate-dynamicscalinginsuspended): Boolean
  [DynamicScalingOutSuspended](#cfn-applicationautoscaling-scalabletarget-suspendedstate-dynamicscalingoutsuspended): Boolean
  [ScheduledScalingSuspended](#cfn-applicationautoscaling-scalabletarget-suspendedstate-scheduledscalingsuspended): Boolean
```

## Properties<a name="aws-properties-applicationautoscaling-scalabletarget-suspendedstate-properties"></a>

`DynamicScalingInSuspended`  <a name="cfn-applicationautoscaling-scalabletarget-suspendedstate-dynamicscalinginsuspended"></a>
Whether scale in by a target tracking scaling policy or a step scaling policy is suspended\. Set the value to `true` if you don't want Application Auto Scaling to remove capacity when a scaling policy is triggered\. The default is `false`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamicScalingOutSuspended`  <a name="cfn-applicationautoscaling-scalabletarget-suspendedstate-dynamicscalingoutsuspended"></a>
Whether scale out by a target tracking scaling policy or a step scaling policy is suspended\. Set the value to `true` if you don't want Application Auto Scaling to add capacity when a scaling policy is triggered\. The default is `false`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduledScalingSuspended`  <a name="cfn-applicationautoscaling-scalabletarget-suspendedstate-scheduledscalingsuspended"></a>
Whether scheduled scaling is suspended\. Set the value to `true` if you don't want Application Auto Scaling to add or remove capacity by initiating scheduled actions\. The default is `false`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
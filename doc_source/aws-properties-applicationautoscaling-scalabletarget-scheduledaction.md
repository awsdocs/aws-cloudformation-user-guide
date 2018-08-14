# Application Auto Scaling ScalableTarget ScheduledAction<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction"></a>

<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-description"></a>The `ScheduledAction` property type specifies a scheduled action for an Application Auto Scaling scalable target\.

<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-inheritance"></a> The `ScheduledActions` property of the [AWS::ApplicationAutoScaling::ScalableTarget](aws-resource-applicationautoscaling-scalabletarget.md) resource contains a list of `ScheduledAction` property types\.

## Syntax<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-syntax.json"></a>

```
{
  "[EndTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-endtime)" : Timestamp,
  "[ScalableTargetAction](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scalabletargetaction)" : [*ScalableTargetAction*](aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction.md),
  "[Schedule](#cfn-applicationautoscaling-scalabletarget-scheduledaction-schedule)" : String,
  "[ScheduledActionName](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scheduledactionname)" : String,
  "[StartTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-starttime)" : Timestamp
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-syntax.yaml"></a>

```
[EndTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-endtime): Timestamp
[ScalableTargetAction](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scalabletargetaction): 
  [*ScalableTargetAction*](aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction.md)
[Schedule](#cfn-applicationautoscaling-scalabletarget-scheduledaction-schedule): String
[ScheduledActionName](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scheduledactionname): String
[StartTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-starttime): Timestamp
```

## Properties<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-properties"></a>

`EndTime`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-endtime"></a>
The date and time that the action is scheduled to end\.  
 *Required*: No  
 *Type*: Timestamp  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScalableTargetAction`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-scalabletargetaction"></a>
The new minimum and maximum capacity\. You can set both values or just one\. During the scheduled time, if the current capacity is below the minimum capacity, Application Auto Scaling scales out to the minimum capacity\. If the current capacity is above the maximum capacity, Application Auto Scaling scales in to the maximum capacity\.  
 *Required*: No  
 *Type*: [Application Auto Scaling ScalableTarget ScalableTargetAction](aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Schedule`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-schedule"></a>
The schedule for this action\. The following formats are supported:  
+ At expressions \- `at(yyyy-mm-ddThh:mm:ss)`

  At expressions are useful for one\-time schedules\. Specify the time in UTC\.
+ Rate expressions \- `rate(value unit)`

  For rate expressions, `value` is a positive integer, and `unit` is `minute`, `minutes`, `hour`, `hours`, `day`, or `days`\.
+ Cron expressions \- `cron(fields)`

  For more information about cron expressions, see [ Cron](https://en.wikipedia.org/wiki/Cron)\.
For constraints, see the [ ScheduledAction](http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_ScheduledAction.html) data type in the *Application Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScheduledActionName`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-scheduledactionname"></a>
The name of the scheduled action\. For constraints, see the [ ScheduledAction](http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_ScheduledAction.html) data type in the *Application Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StartTime`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-starttime"></a>
The date and time that the action is scheduled to begin\.  
 *Required*: No  
 *Type*: Timestamp  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-seealso"></a>
+ [ ScheduledAction](http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_ScheduledAction.html) data type in the *Application Auto Scaling API Reference*
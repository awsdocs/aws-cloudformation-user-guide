# AWS::ApplicationAutoScaling::ScalableTarget ScheduledAction<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction"></a>

 `ScheduledAction` is a property of [ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) that specifies a scheduled action for a scalable target\. 

For more information, see [PutScheduledAction](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScheduledAction.html) in the *Application Auto Scaling API Reference*\.

## Syntax<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-syntax.json"></a>

```
{
  "[EndTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-endtime)" : Timestamp,
  "[ScalableTargetAction](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scalabletargetaction)" : ScalableTargetAction,
  "[Schedule](#cfn-applicationautoscaling-scalabletarget-scheduledaction-schedule)" : String,
  "[ScheduledActionName](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scheduledactionname)" : String,
  "[StartTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-starttime)" : Timestamp
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-syntax.yaml"></a>

```
  [EndTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-endtime): Timestamp
  [ScalableTargetAction](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scalabletargetaction): 
    ScalableTargetAction
  [Schedule](#cfn-applicationautoscaling-scalabletarget-scheduledaction-schedule): String
  [ScheduledActionName](#cfn-applicationautoscaling-scalabletarget-scheduledaction-scheduledactionname): String
  [StartTime](#cfn-applicationautoscaling-scalabletarget-scheduledaction-starttime): Timestamp
```

## Properties<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction-properties"></a>

`EndTime`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-endtime"></a>
The date and time for the recurring schedule to end\.  
*Required*: No  
*Type*: Timestamp  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalableTargetAction`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-scalabletargetaction"></a>
The new minimum and maximum capacity\. You can set both values or just one\. At the scheduled time, if the current capacity is below the minimum capacity, Application Auto Scaling scales out to the minimum capacity\. If the current capacity is above the maximum capacity, Application Auto Scaling scales in to the maximum capacity\.  
*Required*: No  
*Type*: [ScalableTargetAction](aws-properties-applicationautoscaling-scalabletarget-scalabletargetaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-schedule"></a>
The schedule for this action\. The following formats are supported:  
+ At expressions \- "`at(yyyy-mm-ddThh:mm:ss)`"
+ Rate expressions \- "`rate(value unit)`"
+ Cron expressions \- "`cron(fields)`"
At expressions are useful for one\-time schedules\. Specify the time in UTC\.  
For rate expressions, *value* is a positive integer and *unit* is `minute` \| `minutes` \| `hour` \| `hours` \| `day` \| `days`\.  
For more information about cron expressions, see [Cron expressions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/ScheduledEvents.html#CronExpressions) in the *Amazon CloudWatch Events User Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduledActionName`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-scheduledactionname"></a>
The name of the scheduled action\. This name must be unique among all other scheduled actions on the specified scalable target\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `(?!((^[ ]+.*)|(.*([\u0000-\u001f]|[\u007f-\u009f]|[:/|])+.*)|(.*[ ]+$))).+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledaction-starttime"></a>
The date and time that the action is scheduled to start\.  
*Required*: No  
*Type*: Timestamp  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-applicationautoscaling-scalabletarget-scheduledaction--seealso"></a>
+ [Application Auto Scaling template examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html#scenario-app-as-template-examples)
+ [Scheduled scaling](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-scheduled-scaling.html) in the *Application Auto Scaling User Guide* 
+ [Scheduling AWS Lambda Provisioned Concurrency for recurring peak usage](http://aws.amazon.com/blogs/compute/scheduling-aws-lambda-provisioned-concurrency-for-recurring-peak-usage/)


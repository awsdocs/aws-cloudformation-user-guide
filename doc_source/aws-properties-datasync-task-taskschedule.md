# AWS::DataSync::Task TaskSchedule<a name="aws-properties-datasync-task-taskschedule"></a>

Specifies the schedule you want your task to use for repeated executions\. For more information, see [Schedule Expressions for Rules](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/ScheduledEvents.html)\.

## Syntax<a name="aws-properties-datasync-task-taskschedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-taskschedule-syntax.json"></a>

```
{
  "[ScheduleExpression](#cfn-datasync-task-taskschedule-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-datasync-task-taskschedule-syntax.yaml"></a>

```
  [ScheduleExpression](#cfn-datasync-task-taskschedule-scheduleexpression): String
```

## Properties<a name="aws-properties-datasync-task-taskschedule-properties"></a>

`ScheduleExpression`  <a name="cfn-datasync-task-taskschedule-scheduleexpression"></a>
A cron expression that specifies when AWS DataSync initiates a scheduled transfer from a source to a destination location\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9\ \_\*\?\,\|\^\-\/\#\s\(\)\+]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
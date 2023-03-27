# AWS::Scheduler::Schedule<a name="aws-resource-scheduler-schedule"></a>

Creates the specified schedule\.

## Syntax<a name="aws-resource-scheduler-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-scheduler-schedule-syntax.json"></a>

```
{
  "Type" : "AWS::Scheduler::Schedule",
  "Properties" : {
      "[Description](#cfn-scheduler-schedule-description)" : String,
      "[EndDate](#cfn-scheduler-schedule-enddate)" : String,
      "[FlexibleTimeWindow](#cfn-scheduler-schedule-flexibletimewindow)" : FlexibleTimeWindow,
      "[GroupName](#cfn-scheduler-schedule-groupname)" : String,
      "[KmsKeyArn](#cfn-scheduler-schedule-kmskeyarn)" : String,
      "[Name](#cfn-scheduler-schedule-name)" : String,
      "[ScheduleExpression](#cfn-scheduler-schedule-scheduleexpression)" : String,
      "[ScheduleExpressionTimezone](#cfn-scheduler-schedule-scheduleexpressiontimezone)" : String,
      "[StartDate](#cfn-scheduler-schedule-startdate)" : String,
      "[State](#cfn-scheduler-schedule-state)" : String,
      "[Target](#cfn-scheduler-schedule-target)" : Target
    }
}
```

### YAML<a name="aws-resource-scheduler-schedule-syntax.yaml"></a>

```
Type: AWS::Scheduler::Schedule
Properties: 
  [Description](#cfn-scheduler-schedule-description): String
  [EndDate](#cfn-scheduler-schedule-enddate): String
  [FlexibleTimeWindow](#cfn-scheduler-schedule-flexibletimewindow): 
    FlexibleTimeWindow
  [GroupName](#cfn-scheduler-schedule-groupname): String
  [KmsKeyArn](#cfn-scheduler-schedule-kmskeyarn): String
  [Name](#cfn-scheduler-schedule-name): String
  [ScheduleExpression](#cfn-scheduler-schedule-scheduleexpression): String
  [ScheduleExpressionTimezone](#cfn-scheduler-schedule-scheduleexpressiontimezone): String
  [StartDate](#cfn-scheduler-schedule-startdate): String
  [State](#cfn-scheduler-schedule-state): String
  [Target](#cfn-scheduler-schedule-target): 
    Target
```

## Properties<a name="aws-resource-scheduler-schedule-properties"></a>

`Description`  <a name="cfn-scheduler-schedule-description"></a>
The description you specify for the schedule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndDate`  <a name="cfn-scheduler-schedule-enddate"></a>
The date, in UTC, before which the schedule can invoke its target\. Depending on the schedule's recurrence expression, invocations might stop on, or before, the `EndDate` you specify\. EventBridge Scheduler ignores `EndDate` for one\-time schedules\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlexibleTimeWindow`  <a name="cfn-scheduler-schedule-flexibletimewindow"></a>
Allows you to configure a time window during which EventBridge Scheduler invokes the schedule\.  
*Required*: Yes  
*Type*: [FlexibleTimeWindow](aws-properties-scheduler-schedule-flexibletimewindow.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupName`  <a name="cfn-scheduler-schedule-groupname"></a>
The name of the schedule group associated with this schedule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-scheduler-schedule-kmskeyarn"></a>
The Amazon Resource Name \(ARN\) for the customer managed KMS key that EventBridge Scheduler will use to encrypt and decrypt your data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-scheduler-schedule-name"></a>
The name of the schedule\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScheduleExpression`  <a name="cfn-scheduler-schedule-scheduleexpression"></a>
 The expression that defines when the schedule runs\. The following formats are supported\.   
+  `at` expression \- `at(yyyy-mm-ddThh:mm:ss)` 
+  `rate` expression \- `rate(unit value)` 
+  `cron` expression \- `cron(fields)` 
 You can use `at` expressions to create one\-time schedules that invoke a target once, at the time and in the time zone, that you specify\. You can use `rate` and `cron` expressions to create recurring schedules\. Rate\-based schedules are useful when you want to invoke a target at regular intervals, such as every 15 minutes or every five days\. Cron\-based schedules are useful when you want to invoke a target periodically at a specific time, such as at 8:00 am \(UTC\+0\) every 1st day of the month\.   
 A `cron` expression consists of six fields separated by white spaces: `(minutes hours day_of_month month day_of_week year)`\.   
 A `rate` expression consists of a *value* as a positive integer, and a *unit* with the following options: `minute` \| `minutes` \| `hour` \| `hours` \| `day` \| `days`   
 For more information and examples, see [Schedule types on EventBridge Scheduler](https://docs.aws.amazon.com/scheduler/latest/UserGuide/schedule-types.html) in the *EventBridge Scheduler User Guide*\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpressionTimezone`  <a name="cfn-scheduler-schedule-scheduleexpressiontimezone"></a>
The timezone in which the scheduling expression is evaluated\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartDate`  <a name="cfn-scheduler-schedule-startdate"></a>
The date, in UTC, after which the schedule can begin invoking its target\. Depending on the schedule's recurrence expression, invocations might occur on, or after, the `StartDate` you specify\. EventBridge Scheduler ignores `StartDate` for one\-time schedules\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-scheduler-schedule-state"></a>
Specifies whether the schedule is enabled or disabled\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-scheduler-schedule-target"></a>
The schedule's target details\.  
*Required*: Yes  
*Type*: [Target](aws-properties-scheduler-schedule-target.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-scheduler-schedule-return-values"></a>

### Ref<a name="aws-resource-scheduler-schedule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Name` attribute of theschedule\.

### Fn::GetAtt<a name="aws-resource-scheduler-schedule-return-values-fn--getatt"></a>

 The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes that `Fn::GetAtt` returns\. For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-scheduler-schedule-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the Amazon EventBridge Scheduler schedule\.
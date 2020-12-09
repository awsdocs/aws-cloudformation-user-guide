# AWS::DLM::LifecyclePolicy CreateRule<a name="aws-properties-dlm-lifecyclepolicy-createrule"></a>

Specifies when to create snapshots of EBS volumes\.

You must specify either a Cron expression or an interval, interval unit, and start time\. You cannot specify both\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.json"></a>

```
{
  "[CronExpression](#cfn-dlm-lifecyclepolicy-createrule-cronexpression)" : String,
  "[Interval](#cfn-dlm-lifecyclepolicy-createrule-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit)" : String,
  "[Times](#cfn-dlm-lifecyclepolicy-createrule-times)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.yaml"></a>

```
  [CronExpression](#cfn-dlm-lifecyclepolicy-createrule-cronexpression): String
  [Interval](#cfn-dlm-lifecyclepolicy-createrule-interval): Integer
  [IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit): String
  [Times](#cfn-dlm-lifecyclepolicy-createrule-times): 
    - String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-createrule-properties"></a>

`CronExpression`  <a name="cfn-dlm-lifecyclepolicy-createrule-cronexpression"></a>
The schedule, as a Cron expression\. The schedule interval must be between 1 hour and 1 year\. For more information, see [Cron expressions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/ScheduledEvents.html#CronExpressions) in the *Amazon CloudWatch User Guide*\.  
*Required*: No  
*Type*: String  
*Minimum*: `17`  
*Maximum*: `106`  
*Pattern*: `cron\([^\n]{11,100}\)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-dlm-lifecyclepolicy-createrule-interval"></a>
The interval between snapshots\. The supported values are 1, 2, 3, 4, 6, 8, 12, and 24\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-createrule-intervalunit"></a>
The interval unit\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HOURS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Times`  <a name="cfn-dlm-lifecyclepolicy-createrule-times"></a>
The time, in UTC, to start the operation\. The supported format is hh:mm\.  
The operation occurs within a one\-hour window following the specified time\. If you do not specify a time, Amazon DLM selects a time within the next 24 hours\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
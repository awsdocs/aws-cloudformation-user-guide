# AWS::DLM::LifecyclePolicy CreateRule<a name="aws-properties-dlm-lifecyclepolicy-createrule"></a>

 **\[Snapshot and AMI policies only\]** Specifies when the policy should create snapshots or AMIs\.

**Note**  
You must specify either **CronExpression**, or **Interval**, **IntervalUnit**, and **Times**\.
If you need to specify an [ArchiveRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dlm-lifecyclepolicy-schedule.html#cfn-dlm-lifecyclepolicy-schedule-archiverule) for the schedule, then you must specify a creation frequency of at least 28 days\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.json"></a>

```
{
  "[CronExpression](#cfn-dlm-lifecyclepolicy-createrule-cronexpression)" : String,
  "[Interval](#cfn-dlm-lifecyclepolicy-createrule-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit)" : String,
  "[Location](#cfn-dlm-lifecyclepolicy-createrule-location)" : String,
  "[Times](#cfn-dlm-lifecyclepolicy-createrule-times)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.yaml"></a>

```
  [CronExpression](#cfn-dlm-lifecyclepolicy-createrule-cronexpression): String
  [Interval](#cfn-dlm-lifecyclepolicy-createrule-interval): Integer
  [IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit): String
  [Location](#cfn-dlm-lifecyclepolicy-createrule-location): String
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

`Location`  <a name="cfn-dlm-lifecyclepolicy-createrule-location"></a>
 **\[Snapshot policies only\]** Specifies the destination for snapshots created by the policy\. To create snapshots in the same Region as the source resource, specify `CLOUD`\. To create snapshots on the same Outpost as the source resource, specify `OUTPOST_LOCAL`\. If you omit this parameter, `CLOUD` is used by default\.  
If the policy targets resources in an AWS Region, then you must create snapshots in the same Region as the source resource\. If the policy targets resources on an Outpost, then you can create snapshots on the same Outpost as the source resource, or in the Region of that Outpost\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CLOUD | OUTPOST_LOCAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Times`  <a name="cfn-dlm-lifecyclepolicy-createrule-times"></a>
The time, in UTC, to start the operation\. The supported format is hh:mm\.  
The operation occurs within a one\-hour window following the specified time\. If you do not specify a time, Amazon Data Lifecycle Manager selects a time within the next 24 hours\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
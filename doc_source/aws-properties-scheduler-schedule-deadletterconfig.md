# AWS::Scheduler::Schedule DeadLetterConfig<a name="aws-properties-scheduler-schedule-deadletterconfig"></a>

An object that contains information about an Amazon SQS queue that EventBridge Scheduler uses as a dead\-letter queue for your schedule\. If specified, EventBridge Scheduler delivers failed events that could not be successfully delivered to a target to the queue\.

## Syntax<a name="aws-properties-scheduler-schedule-deadletterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-deadletterconfig-syntax.json"></a>

```
{
  "[Arn](#cfn-scheduler-schedule-deadletterconfig-arn)" : String
}
```

### YAML<a name="aws-properties-scheduler-schedule-deadletterconfig-syntax.yaml"></a>

```
  [Arn](#cfn-scheduler-schedule-deadletterconfig-arn): String
```

## Properties<a name="aws-properties-scheduler-schedule-deadletterconfig-properties"></a>

`Arn`  <a name="cfn-scheduler-schedule-deadletterconfig-arn"></a>
The Amazon Resource Name \(ARN\) of the SQS queue specified as the destination for the dead\-letter queue\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
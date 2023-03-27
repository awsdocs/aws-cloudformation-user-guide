# AWS::Scheduler::Schedule SqsParameters<a name="aws-properties-scheduler-schedule-sqsparameters"></a>

The templated target type for the Amazon SQS [https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_SendMessage.html](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_SendMessage.html) API operation\. Contains the message group ID to use when the target is a FIFO queue\. If you specify an Amazon SQS FIFO queue as a target, the queue must have content\-based deduplication enabled\. For more information, see [Using the Amazon SQS message deduplication ID](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/using-messagededuplicationid-property.html) in the *Amazon SQS Developer Guide*\. 

## Syntax<a name="aws-properties-scheduler-schedule-sqsparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-sqsparameters-syntax.json"></a>

```
{
  "[MessageGroupId](#cfn-scheduler-schedule-sqsparameters-messagegroupid)" : String
}
```

### YAML<a name="aws-properties-scheduler-schedule-sqsparameters-syntax.yaml"></a>

```
  [MessageGroupId](#cfn-scheduler-schedule-sqsparameters-messagegroupid): String
```

## Properties<a name="aws-properties-scheduler-schedule-sqsparameters-properties"></a>

`MessageGroupId`  <a name="cfn-scheduler-schedule-sqsparameters-messagegroupid"></a>
The FIFO message group ID to use as the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
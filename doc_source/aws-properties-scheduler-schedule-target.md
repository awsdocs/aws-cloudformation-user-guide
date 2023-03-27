# AWS::Scheduler::Schedule Target<a name="aws-properties-scheduler-schedule-target"></a>

The schedule's target\. EventBridge Scheduler supports templated target that invoke common API operations, as well as universal targets that you can customize to invoke over 6,000 API operations across more than 270 services\. You can only specify one templated or universal target for a schedule\.

## Syntax<a name="aws-properties-scheduler-schedule-target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-target-syntax.json"></a>

```
{
  "[Arn](#cfn-scheduler-schedule-target-arn)" : String,
  "[DeadLetterConfig](#cfn-scheduler-schedule-target-deadletterconfig)" : DeadLetterConfig,
  "[EcsParameters](#cfn-scheduler-schedule-target-ecsparameters)" : EcsParameters,
  "[EventBridgeParameters](#cfn-scheduler-schedule-target-eventbridgeparameters)" : EventBridgeParameters,
  "[Input](#cfn-scheduler-schedule-target-input)" : String,
  "[KinesisParameters](#cfn-scheduler-schedule-target-kinesisparameters)" : KinesisParameters,
  "[RetryPolicy](#cfn-scheduler-schedule-target-retrypolicy)" : RetryPolicy,
  "[RoleArn](#cfn-scheduler-schedule-target-rolearn)" : String,
  "[SageMakerPipelineParameters](#cfn-scheduler-schedule-target-sagemakerpipelineparameters)" : SageMakerPipelineParameters,
  "[SqsParameters](#cfn-scheduler-schedule-target-sqsparameters)" : SqsParameters
}
```

### YAML<a name="aws-properties-scheduler-schedule-target-syntax.yaml"></a>

```
  [Arn](#cfn-scheduler-schedule-target-arn): String
  [DeadLetterConfig](#cfn-scheduler-schedule-target-deadletterconfig): 
    DeadLetterConfig
  [EcsParameters](#cfn-scheduler-schedule-target-ecsparameters): 
    EcsParameters
  [EventBridgeParameters](#cfn-scheduler-schedule-target-eventbridgeparameters): 
    EventBridgeParameters
  [Input](#cfn-scheduler-schedule-target-input): String
  [KinesisParameters](#cfn-scheduler-schedule-target-kinesisparameters): 
    KinesisParameters
  [RetryPolicy](#cfn-scheduler-schedule-target-retrypolicy): 
    RetryPolicy
  [RoleArn](#cfn-scheduler-schedule-target-rolearn): String
  [SageMakerPipelineParameters](#cfn-scheduler-schedule-target-sagemakerpipelineparameters): 
    SageMakerPipelineParameters
  [SqsParameters](#cfn-scheduler-schedule-target-sqsparameters): 
    SqsParameters
```

## Properties<a name="aws-properties-scheduler-schedule-target-properties"></a>

`Arn`  <a name="cfn-scheduler-schedule-target-arn"></a>
The Amazon Resource Name \(ARN\) of the target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeadLetterConfig`  <a name="cfn-scheduler-schedule-target-deadletterconfig"></a>
An object that contains information about an Amazon SQS queue that EventBridge Scheduler uses as a dead\-letter queue for your schedule\. If specified, EventBridge Scheduler delivers failed events that could not be successfully delivered to a target to the queue\.  
*Required*: No  
*Type*: [DeadLetterConfig](aws-properties-scheduler-schedule-deadletterconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcsParameters`  <a name="cfn-scheduler-schedule-target-ecsparameters"></a>
The templated target type for the Amazon ECS [https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_RunTask.html](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_RunTask.html) API operation\.  
*Required*: No  
*Type*: [EcsParameters](aws-properties-scheduler-schedule-ecsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBridgeParameters`  <a name="cfn-scheduler-schedule-target-eventbridgeparameters"></a>
The templated target type for the EventBridge [https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_PutEvents.html](https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_PutEvents.html) API operation\.  
*Required*: No  
*Type*: [EventBridgeParameters](aws-properties-scheduler-schedule-eventbridgeparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Input`  <a name="cfn-scheduler-schedule-target-input"></a>
The text, or well\-formed JSON, passed to the target\. If you are configuring a templated Lambda, AWS Step Functions, or Amazon EventBridge target, the input must be a well\-formed JSON\. For all other target types, a JSON is not required\. If you do not specify anything for this field, Amazon EventBridge Scheduler delivers a default notification to the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisParameters`  <a name="cfn-scheduler-schedule-target-kinesisparameters"></a>
The templated target type for the Amazon Kinesis [kinesis/latest/APIReference/API_PutRecord.html](kinesis/latest/APIReference/API_PutRecord.html) API operation\.  
*Required*: No  
*Type*: [KinesisParameters](aws-properties-scheduler-schedule-kinesisparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryPolicy`  <a name="cfn-scheduler-schedule-target-retrypolicy"></a>
A `RetryPolicy` object that includes information about the retry policy settings, including the maximum age of an event, and the maximum number of times EventBridge Scheduler will try to deliver the event to a target\.  
*Required*: No  
*Type*: [RetryPolicy](aws-properties-scheduler-schedule-retrypolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-scheduler-schedule-target-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that EventBridge Scheduler will use for this target when the schedule is invoked\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SageMakerPipelineParameters`  <a name="cfn-scheduler-schedule-target-sagemakerpipelineparameters"></a>
The templated target type for the Amazon SageMaker [https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_StartPipelineExecution.html](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_StartPipelineExecution.html) API operation\.  
*Required*: No  
*Type*: [SageMakerPipelineParameters](aws-properties-scheduler-schedule-sagemakerpipelineparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqsParameters`  <a name="cfn-scheduler-schedule-target-sqsparameters"></a>
The templated target type for the Amazon SQS [https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_SendMessage.html](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_SendMessage.html) API operation\. Contains the message group ID to use when the target is a FIFO queue\. If you specify an Amazon SQS FIFO queue as a target, the queue must have content\-based deduplication enabled\. For more information, see [Using the Amazon SQS message deduplication ID](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/using-messagededuplicationid-property.html) in the *Amazon SQS Developer Guide*\.  
*Required*: No  
*Type*: [SqsParameters](aws-properties-scheduler-schedule-sqsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
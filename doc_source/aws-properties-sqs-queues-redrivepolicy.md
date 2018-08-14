# Amazon SQS RedrivePolicy<a name="aws-properties-sqs-queues-redrivepolicy"></a>

The `RedrivePolicy` type is a property of the [AWS::SQS::Queue](aws-properties-sqs-queues.md) resource\. A redrive policy defines the parameters for the dead letter queue functionality of the source queue\. For more information about the redrive policy and dead letter queues, see [Using Amazon SQS Dead Letter Queues](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html) in the *Amazon Simple Queue Service Developer Guide*\.

## Syntax<a name="w3ab2c21c14e1987b5"></a>

### JSON<a name="aws-properties-sqs-queues-redrivepolicy-syntax.json"></a>

```
{
  "[deadLetterTargetArn](#aws-sqs-queue-redrivepolicy-targetarn)" : String,
  "[maxReceiveCount](#aws-sqs-queue-redrivepolicy-maxcount)" : Integer
}
```

### YAML<a name="aws-properties-sqs-queues-redrivepolicy-syntax.yaml"></a>

```
[deadLetterTargetArn](#aws-sqs-queue-redrivepolicy-targetarn): String
[maxReceiveCount](#aws-sqs-queue-redrivepolicy-maxcount): Integer
```

## Properties<a name="w3ab2c21c14e1987b7"></a>

`deadLetterTargetArn`  <a name="aws-sqs-queue-redrivepolicy-targetarn"></a>
The Amazon Resource Name \(ARN\) of the dead\-letter queue to which Amazon SQS moves messages after the value of `maxReceiveCount` is exceeded\.  
*Required*: Yes  
*Type*: String

`maxReceiveCount`  <a name="aws-sqs-queue-redrivepolicy-maxcount"></a>
The number of times a message is delivered to the source queue before being moved to the dead\-letter queue\.  
*Required*: Yes  
*Type*: Integer
# AWS::SQS::Queue<a name="aws-properties-sqs-queues"></a>

The `AWS::SQS::Queue` resource creates an Amazon Simple Queue Service \(Amazon SQS\) queue\.

For more information about creating FIFO \(first\-in\-first\-out\) queues, see the tutorial [Create a queue using AWS CloudFormation](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-create-queue.html#create-queue-cloudformation) in the *Amazon Simple Queue Service Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-sqs-queues-syntax)
+ [Properties](#aws-properties-sqs-queues-prop)
+ [Return Values](#aws-properties-sqs-queues-ref)
+ [Examples](#w3ab2c21c10e1138c15)
+ [See Also](#w3ab2c21c10e1138c17)

## Syntax<a name="aws-resource-sqs-queues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sqs-queues-syntax.json"></a>

```
{
   "Type" : "AWS::SQS::Queue",
   "Properties" : {
      "[ContentBasedDeduplication](#cfn-sqs-queue-contentbaseddeduplication)" : Boolean,
      "[DelaySeconds](#aws-sqs-queue-delayseconds)": Integer,
      "[FifoQueue](#cfn-sqs-queue-fifoqueue)" : Boolean,
      "[KmsMasterKeyId](#aws-sqs-queue-kmsmasterkeyid)": String,
      "[KmsDataKeyReusePeriodSeconds](#aws-sqs-queue-kmsdatakeyreuseperiodseconds)": Integer,
      "[MaximumMessageSize](#aws-sqs-queue-maxmsgsize)": Integer,
      "[MessageRetentionPeriod](#aws-sqs-queue-msgretentionperiod)": Integer,
      "[QueueName](#aws-sqs-queue-name)": String,
      "[ReceiveMessageWaitTimeSeconds](#aws-sqs-queue-receivemsgwaittime)": Integer,
      "[RedrivePolicy](#aws-sqs-queue-redrive)": RedrivePolicy,
      "[VisibilityTimeout](#aws-sqs-queue-visibilitytimeout)": Integer
   }
}
```

### YAML<a name="aws-resource-sqs-queues-syntax.yaml"></a>

```
Type: "AWS::SQS::Queue"
Properties:
  [ContentBasedDeduplication](#cfn-sqs-queue-contentbaseddeduplication): Boolean
  [DelaySeconds](#aws-sqs-queue-delayseconds): Integer
  [FifoQueue](#cfn-sqs-queue-fifoqueue): Boolean
  [KmsMasterKeyId](#aws-sqs-queue-kmsmasterkeyid): String
  [KmsDataKeyReusePeriodSeconds](#aws-sqs-queue-kmsdatakeyreuseperiodseconds): Integer
  [MaximumMessageSize](#aws-sqs-queue-maxmsgsize): Integer
  [MessageRetentionPeriod](#aws-sqs-queue-msgretentionperiod): Integer
  [QueueName](#aws-sqs-queue-name): String
  [ReceiveMessageWaitTimeSeconds](#aws-sqs-queue-receivemsgwaittime): Integer
  [RedrivePolicy](#aws-sqs-queue-redrive):
    RedrivePolicy
  [VisibilityTimeout](#aws-sqs-queue-visibilitytimeout): Integer
```

## Properties<a name="aws-properties-sqs-queues-prop"></a>

`ContentBasedDeduplication`  <a name="cfn-sqs-queue-contentbaseddeduplication"></a>
For first\-in\-first\-out \(FIFO\) queues, specifies whether to enable content\-based deduplication\. During the deduplication interval, Amazon SQS treats messages that are sent with identical content as duplicates and delivers only one copy of the message\. For more information, see the `ContentBasedDeduplication` attribute for the [CreateQueue](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_CreateQueue.html) action in the *Amazon Simple Queue Service API Reference*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DelaySeconds`  <a name="aws-sqs-queue-delayseconds"></a>
The time in seconds that the delivery of all messages in the queue is delayed\. You can specify an integer value of `0` to `900` \(15 minutes\)\. The default value is `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`FifoQueue`  <a name="cfn-sqs-queue-fifoqueue"></a>
Indicates whether this queue is a FIFO queue\. For more information, see [FIFO \(First\-In\-First\-Out\) Queues](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html) in the *Amazon Simple Queue Service Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KmsMasterKeyId`  <a name="aws-sqs-queue-kmsmasterkeyid"></a>
The ID of an AWS managed customer master key \(CMK\) for Amazon SQS or a custom CMK\. To use the AWS managed CMK for Amazon SQS, specify the alias `alias/aws/sqs`\. For more information, see [CreateQueue](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_CreateQueue.html) in the *Amazon Simple Queue Service API Reference*, [Protecting Data Using Server\-Side Encryption \(SSE\) and AWS KMS](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-server-side-encryption.html) in the *Amazon Simple Queue Service Developer Guide*, or **Customer Master Keys** in the [AWS Key Management Service Best Practices](https://d0.awsstatic.com/whitepapers/aws-kms-best-practices.pdf) whitepaper\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsDataKeyReusePeriodSeconds`  <a name="aws-sqs-queue-kmsdatakeyreuseperiodseconds"></a>
The length of time in seconds that Amazon SQS can reuse a data key to encrypt or decrypt messages before calling AWS KMS again\. The value must be an integer between 60 \(1 minute\) and 86,400 \(24 hours\)\. The default is 300 \(5 minutes\)\.  
A shorter time period provides better security, but results in more calls to AWS KMS, which might incur charges after Free Tier\. For more information, see [ How Does the Data Key Reuse Period Work?](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-server-side-encryption.html#sqs-how-does-the-data-key-reuse-period-work) in the *Amazon Simple Queue Service Developer Guide*\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MaximumMessageSize`  <a name="aws-sqs-queue-maxmsgsize"></a>
The limit of how many bytes that a message can contain before Amazon SQS rejects it\. You can specify an integer value from `1024` bytes \(1 KiB\) to `262144` bytes \(256 KiB\)\. The default value is `262144` \(256 KiB\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MessageRetentionPeriod`  <a name="aws-sqs-queue-msgretentionperiod"></a>
The number of seconds that Amazon SQS retains a message\. You can specify an integer value from `60` seconds \(1 minute\) to `1209600` seconds \(14 days\)\. The default value is `345600` seconds \(4 days\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`QueueName`  <a name="aws-sqs-queue-name"></a>
A name for the queue\. To create a FIFO queue, the name of your FIFO queue must end with the `.fifo` suffix\. For more information, see [FIFO \(First\-In\-First\-Out\) Queues](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html) in the *Amazon Simple Queue Service Developer Guide*\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the queue name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ReceiveMessageWaitTimeSeconds`  <a name="aws-sqs-queue-receivemsgwaittime"></a>
Specifies the duration, in seconds, that the `ReceiveMessage` action call waits until a message is in the queue in order to include it in the response, as opposed to returning an empty response if a message isn't yet available\. You can specify an integer from `1` to `20`\. The short polling is used as the default or when you specify `0` for this property\. For more information, see [Amazon SQS Long Poll](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-long-polling.html)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RedrivePolicy`  <a name="aws-sqs-queue-redrive"></a>
Specifies an existing dead letter queue to receive messages after the source queue \(this queue\) fails to process a message a specified number of times\.  
*Required*: No  
*Type*: [Amazon SQS RedrivePolicy](aws-properties-sqs-queues-redrivepolicy.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VisibilityTimeout`  <a name="aws-sqs-queue-visibilitytimeout"></a>
The length of time during which a message will be unavailable after a message is delivered from the queue\. This blocks other components from receiving the same message and gives the initial component time to process and delete the message from the queue\.  
Values must be from 0 to 43200 seconds \(12 hours\)\. If you don't specify a value, AWS CloudFormation uses the default value of 30 seconds\.  
For more information about Amazon SQS queue visibility timeouts, see [Visibility Timeout](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/AboutVT.html) in the *Amazon Simple Queue Service Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-properties-sqs-queues-ref"></a>

### Ref<a name="w3ab2c21c10e1138c13b2"></a>

The `AWS::SQS::Queue` type returns the queue URL\. For example: `https://sqs.``us-east-2``.amazonaws.com/123456789012/aa4-MyQueue-Z5NOSZO2PZE9`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10e1138c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
Returns the Amazon Resource Name \(ARN\) of the queue\. For example: `arn:aws:sqs:``us-east-2``:123456789012:mystack-myqueue-15PG5C2FC1CW8`\.

`QueueName`  
Returns the queue name\. For example:  
`mystack-myqueue-1VF9BKQH5BJVI`

## Examples<a name="w3ab2c21c10e1138c15"></a>

### SQS Queue with Cloudwatch Alarms<a name="w3ab2c21c10e1138c15b2"></a>

#### JSON<a name="aws-resource-sqs-queues-example1.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
 
  "Description" : "AWS CloudFormation Sample Template SQS_With_CloudWatch_Alarms: Sample template showing how to create an SQS queue with Amazon CloudWatch alarms on queue depth. **WARNING** This template creates an Amazon SQS queue and one or more Amazon CloudWatch alarms. You will be billed for the AWS resources used if you create a stack from this template.",
 
  "Parameters" : {
    "AlarmEmail": {
      "Default": "nobody@amazon.com",
      "Description": "Email address to notify if operational problems arise",
      "Type": "String"
    }
  },
 
  "Resources" : {
    "MyQueue" : {
      "Type" : "AWS::SQS::Queue",
      "Properties" : {
         "QueueName" : "SampleQueue"
      }
    },
    "AlarmTopic": {
      "Type": "AWS::SNS::Topic",
      "Properties": {
        "Subscription": [{
          "Endpoint": { "Ref": "AlarmEmail" },
          "Protocol": "email"
        }]
      }
    },
    "QueueDepthAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "AlarmDescription": "Alarm if queue depth grows beyond 10 messages",
        "Namespace": "AWS/SQS",
        "MetricName": "ApproximateNumberOfMessagesVisible",
        "Dimensions": [{
          "Name": "QueueName",
          "Value" : { "Fn::GetAtt" : ["MyQueue", "QueueName"] }
        }],
        "Statistic": "Sum",
        "Period": "300",
        "EvaluationPeriods": "1",
        "Threshold": "10",
        "ComparisonOperator": "GreaterThanThreshold",
        "AlarmActions": [{
          "Ref": "AlarmTopic"
        }],
        "InsufficientDataActions": [{
          "Ref": "AlarmTopic"
        }]
      }
    }
  },
  "Outputs" : {
    "QueueURL" : {
      "Description" : "URL of newly created SQS Queue",
      "Value" : { "Ref" : "MyQueue" }
    },
    "QueueARN" : {
      "Description" : "ARN of newly created SQS Queue",
      "Value" : { "Fn::GetAtt" : ["MyQueue", "Arn"]}
    },
    "QueueName" : {
      "Description" : "Name newly created SQS Queue",
      "Value" : { "Fn::GetAtt" : ["MyQueue", "QueueName"]}
    }
  }
}
```

#### YAML<a name="aws-resource-sqs-queues-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: "AWS CloudFormation Sample Template SQS_With_CloudWatch_Alarms: Sample template showing how to create an SQS queue with Amazon CloudWatch alarms on queue depth. **WARNING** This template creates an Amazon SQS queue and one or more Amazon CloudWatch alarms. You will be billed for the AWS resources used if you create a stack from this template."
Parameters: 
  AlarmEmail: 
    Default: "nobody@amazon.com"
    Description: "Email address to notify if operational problems arise"
    Type: "String"
Resources: 
  MyQueue: 
    Type: "AWS::SQS::Queue"
    Properties: 
      QueueName: "SampleQueue"
  AlarmTopic: 
    Type: "AWS::SNS::Topic"
    Properties: 
      Subscription: 
        - 
          Endpoint: 
            Ref: "AlarmEmail"
          Protocol: "email"
  QueueDepthAlarm: 
    Type: "AWS::CloudWatch::Alarm"
    Properties: 
      AlarmDescription: "Alarm if queue depth grows beyond 10 messages"
      Namespace: "AWS/SQS"
      MetricName: "ApproximateNumberOfMessagesVisible"
      Dimensions: 
        - 
          Name: "QueueName"
          Value: 
            Fn::GetAtt: 
              - "MyQueue"
              - "QueueName"
      Statistic: "Sum"
      Period: "300"
      EvaluationPeriods: "1"
      Threshold: "10"
      ComparisonOperator: "GreaterThanThreshold"
      AlarmActions: 
        - 
          Ref: "AlarmTopic"
      InsufficientDataActions: 
        - 
          Ref: "AlarmTopic"
Outputs: 
  QueueURL: 
    Description: "URL of newly created SQS Queue"
    Value: 
      Ref: "MyQueue"
  QueueARN: 
    Description: "ARN of newly created SQS Queue"
    Value: 
      Fn::GetAtt: 
        - "MyQueue"
        - "Arn"
  QueueName: 
    Description: "Name newly created SQS Queue"
    Value: 
      Fn::GetAtt: 
        - "MyQueue"
        - "QueueName"
```

### SQS Queue with a Dead Letter Queue<a name="w3ab2c21c10e1138c15b4"></a>

The following sample creates a source queue and a dead letter queue\. Because the source queue specifies the dead letter queue in its redrive policy, the source queue is dependent on the creation of the dead letter queue\.

#### JSON<a name="aws-resource-sqs-queues-example2.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
   
  "Resources" : {
    "MySourceQueue" : {
      "Type" : "AWS::SQS::Queue",
      "Properties" : {
        "RedrivePolicy": {
          "deadLetterTargetArn" : {"Fn::GetAtt" : [ "MyDeadLetterQueue" , "Arn" ]},
          "maxReceiveCount" : 5
        }
      }
    },    
    "MyDeadLetterQueue" : {
      "Type" : "AWS::SQS::Queue"
    }
  },

  "Outputs" : {
    "SourceQueueURL" : {
      "Description" : "URL of the source queue",
      "Value" : { "Ref" : "MySourceQueue" }
    },
    "SourceQueueARN" : {
      "Description" : "ARN of the source queue",
      "Value" : { "Fn::GetAtt" : ["MySourceQueue", "Arn"]}
    },
    "DeadLetterQueueURL" : {
      "Description" : "URL of the dead letter queue",
      "Value" : { "Ref" : "MyDeadLetterQueue" }
    },
    "DeadLetterQueueARN" : {
      "Description" : "ARN of the dead letter queue",
      "Value" : { "Fn::GetAtt" : ["MyDeadLetterQueue", "Arn"]}
    }    
  }
}
```

#### YAML<a name="aws-resource-sqs-queues-example2.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MySourceQueue: 
    Type: "AWS::SQS::Queue"
    Properties: 
      RedrivePolicy: 
        deadLetterTargetArn: 
          Fn::GetAtt: 
            - "MyDeadLetterQueue"
            - "Arn"
        maxReceiveCount: 5
  MyDeadLetterQueue: 
    Type: "AWS::SQS::Queue"
Outputs: 
  SourceQueueURL: 
    Description: "URL of the source queue"
    Value: 
      Ref: "MySourceQueue"
  SourceQueueARN: 
    Description: "ARN of the source queue"
    Value: 
      Fn::GetAtt: 
        - "MySourceQueue"
        - "Arn"
  DeadLetterQueueURL: 
    Description: "URL of the dead letter queue"
    Value: 
      Ref: "MyDeadLetterQueue"
  DeadLetterQueueARN: 
    Description: "ARN of the dead letter queue"
    Value: 
      Fn::GetAtt: 
        - "MyDeadLetterQueue"
        - "Arn"
```

## See Also<a name="w3ab2c21c10e1138c17"></a>
+ [CreateQueue](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/Query_QueryCreateQueue.html) in the *Amazon Simple Queue Service API Reference*
+ [What is Amazon Simple Queue Service?](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/Welcome.html) in the *Amazon Simple Queue Service Developer Guide*
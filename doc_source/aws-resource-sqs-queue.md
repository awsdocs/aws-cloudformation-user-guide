# AWS::SQS::Queue<a name="aws-resource-sqs-queue"></a>

The `AWS::SQS::Queue` resource creates an Amazon SQS standard or FIFO queue\.

Keep the following caveats in mind:
+ If you don't specify the `FifoQueue` property, Amazon SQS creates a standard queue\.
**Note**  
You can't change the queue type after you create it and you can't convert an existing standard queue into a FIFO queue\. You must either create a new FIFO queue for your application or delete your existing standard queue and recreate it as a FIFO queue\. For more information, see [Moving from a standard queue to a FIFO queue](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues-moving.html) in the *Amazon SQS Developer Guide*\. 
+ If you don't provide a value for a property, the queue is created with the default value for the property\.
+ If you delete a queue, you must wait at least 60 seconds before creating a queue with the same name\.
+ To successfully create a new queue, you must provide a queue name that adheres to the [limits related to queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/limits-queues.html) and is unique within the scope of your queues\.

For more information about creating FIFO \(first\-in\-first\-out\) queues, see [Creating an Amazon SQS queue \(AWS CloudFormation\)](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/screate-queue-cloudformation.html) in the *Amazon SQS Developer Guide*\.

## Syntax<a name="aws-resource-sqs-queue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sqs-queue-syntax.json"></a>

```
{
  "Type" : "AWS::SQS::Queue",
  "Properties" : {
      "[ContentBasedDeduplication](#cfn-sqs-queue-contentbaseddeduplication)" : Boolean,
      "[DeduplicationScope](#cfn-sqs-queue-deduplicationscope)" : String,
      "[DelaySeconds](#cfn-sqs-queue-delayseconds)" : Integer,
      "[FifoQueue](#cfn-sqs-queue-fifoqueue)" : Boolean,
      "[FifoThroughputLimit](#cfn-sqs-queue-fifothroughputlimit)" : String,
      "[KmsDataKeyReusePeriodSeconds](#cfn-sqs-queue-kmsdatakeyreuseperiodseconds)" : Integer,
      "[KmsMasterKeyId](#cfn-sqs-queue-kmsmasterkeyid)" : String,
      "[MaximumMessageSize](#cfn-sqs-queue-maximummessagesize)" : Integer,
      "[MessageRetentionPeriod](#cfn-sqs-queue-messageretentionperiod)" : Integer,
      "[QueueName](#cfn-sqs-queue-queuename)" : String,
      "[ReceiveMessageWaitTimeSeconds](#cfn-sqs-queue-receivemessagewaittimeseconds)" : Integer,
      "[RedriveAllowPolicy](#cfn-sqs-queue-redriveallowpolicy)" : Json,
      "[RedrivePolicy](#cfn-sqs-queue-redrivepolicy)" : Json,
      "[SqsManagedSseEnabled](#cfn-sqs-queue-sqsmanagedsseenabled)" : Boolean,
      "[Tags](#cfn-sqs-queue-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VisibilityTimeout](#cfn-sqs-queue-visibilitytimeout)" : Integer
    }
}
```

### YAML<a name="aws-resource-sqs-queue-syntax.yaml"></a>

```
Type: AWS::SQS::Queue
Properties: 
  [ContentBasedDeduplication](#cfn-sqs-queue-contentbaseddeduplication): Boolean
  [DeduplicationScope](#cfn-sqs-queue-deduplicationscope): String
  [DelaySeconds](#cfn-sqs-queue-delayseconds): Integer
  [FifoQueue](#cfn-sqs-queue-fifoqueue): Boolean
  [FifoThroughputLimit](#cfn-sqs-queue-fifothroughputlimit): String
  [KmsDataKeyReusePeriodSeconds](#cfn-sqs-queue-kmsdatakeyreuseperiodseconds): Integer
  [KmsMasterKeyId](#cfn-sqs-queue-kmsmasterkeyid): String
  [MaximumMessageSize](#cfn-sqs-queue-maximummessagesize): Integer
  [MessageRetentionPeriod](#cfn-sqs-queue-messageretentionperiod): Integer
  [QueueName](#cfn-sqs-queue-queuename): String
  [ReceiveMessageWaitTimeSeconds](#cfn-sqs-queue-receivemessagewaittimeseconds): Integer
  [RedriveAllowPolicy](#cfn-sqs-queue-redriveallowpolicy): Json
  [RedrivePolicy](#cfn-sqs-queue-redrivepolicy): Json
  [SqsManagedSseEnabled](#cfn-sqs-queue-sqsmanagedsseenabled): Boolean
  [Tags](#cfn-sqs-queue-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VisibilityTimeout](#cfn-sqs-queue-visibilitytimeout): Integer
```

## Properties<a name="aws-resource-sqs-queue-properties"></a>

`ContentBasedDeduplication`  <a name="cfn-sqs-queue-contentbaseddeduplication"></a>
For first\-in\-first\-out \(FIFO\) queues, specifies whether to enable content\-based deduplication\. During the deduplication interval, Amazon SQS treats messages that are sent with identical content as duplicates and delivers only one copy of the message\. For more information, see the `ContentBasedDeduplication` attribute for the ` [CreateQueue](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_CreateQueue.html) ` action in the *Amazon SQS API Reference*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeduplicationScope`  <a name="cfn-sqs-queue-deduplicationscope"></a>
For high throughput for FIFO queues, specifies whether message deduplication occurs at the message group or queue level\. Valid values are `messageGroup` and `queue`\.  
To enable high throughput for a FIFO queue, set this attribute to `messageGroup` *and* set the `FifoThroughputLimit` attribute to `perMessageGroupId`\. If you set these attributes to anything other than these values, normal throughput is in effect and deduplication occurs as specified\. For more information, see [High throughput for FIFO queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/high-throughput-fifo.html) and [Quotas related to messages](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/quotas-messages.html) in the *Amazon SQS Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DelaySeconds`  <a name="cfn-sqs-queue-delayseconds"></a>
The time in seconds for which the delivery of all messages in the queue is delayed\. You can specify an integer value of `0` to `900` \(15 minutes\)\. The default value is `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FifoQueue`  <a name="cfn-sqs-queue-fifoqueue"></a>
If set to true, creates a FIFO queue\. If you don't specify this property, Amazon SQS creates a standard queue\. For more information, see [FIFO queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html) in the *Amazon SQS Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FifoThroughputLimit`  <a name="cfn-sqs-queue-fifothroughputlimit"></a>
For high throughput for FIFO queues, specifies whether the FIFO queue throughput quota applies to the entire queue or per message group\. Valid values are `perQueue` and `perMessageGroupId`\.  
To enable high throughput for a FIFO queue, set this attribute to `perMessageGroupId` *and* set the `DeduplicationScope` attribute to `messageGroup`\. If you set these attributes to anything other than these values, normal throughput is in effect and deduplication occurs as specified\. For more information, see [High throughput for FIFO queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/high-throughput-fifo.html) and [Quotas related to messages](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/quotas-messages.html) in the *Amazon SQS Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsDataKeyReusePeriodSeconds`  <a name="cfn-sqs-queue-kmsdatakeyreuseperiodseconds"></a>
The length of time in seconds for which Amazon SQS can reuse a data key to encrypt or decrypt messages before calling AWS KMS again\. The value must be an integer between 60 \(1 minute\) and 86,400 \(24 hours\)\. The default is 300 \(5 minutes\)\.  
A shorter time period provides better security, but results in more calls to AWS KMS, which might incur charges after Free Tier\. For more information, see [Encryption at rest](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-server-side-encryption.html#sqs-how-does-the-data-key-reuse-period-work) in the *Amazon SQS Developer Guide*\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsMasterKeyId`  <a name="cfn-sqs-queue-kmsmasterkeyid"></a>
The ID of an AWS Key Management Service \(KMS\) for Amazon SQS, or a custom KMS\. To use the AWS managed KMS for Amazon SQS, specify a \(default\) alias ARN, alias name \(e\.g\. `alias/aws/sqs`\), key ARN, or key ID\. For more information, see the following:  
+  [Encryption at rest](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-server-side-encryption.html) in the *Amazon SQS Developer Guide* 
+  [CreateQueue](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_CreateQueue.html) in the *Amazon SQS API Reference* 
+  [Request Parameters](https://docs.aws.amazon.com/kms/latest/APIReference/API_DescribeKey.html#API_DescribeKey_RequestParameters) in the *AWS Key Management Service API Reference* 
+  The Key Management Service \(KMS\) section of the [AWS Key Management Service Best Practices](https://d0.awsstatic.com/whitepapers/aws-kms-best-practices.pdf) whitepaper 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumMessageSize`  <a name="cfn-sqs-queue-maximummessagesize"></a>
The limit of how many bytes that a message can contain before Amazon SQS rejects it\. You can specify an integer value from `1,024` bytes \(1 KiB\) to `262,144` bytes \(256 KiB\)\. The default value is `262,144` \(256 KiB\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageRetentionPeriod`  <a name="cfn-sqs-queue-messageretentionperiod"></a>
The number of seconds that Amazon SQS retains a message\. You can specify an integer value from `60` seconds \(1 minute\) to `1,209,600` seconds \(14 days\)\. The default value is `345,600` seconds \(4 days\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueName`  <a name="cfn-sqs-queue-queuename"></a>
A name for the queue\. To create a FIFO queue, the name of your FIFO queue must end with the `.fifo` suffix\. For more information, see [FIFO queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html) in the *Amazon SQS Developer Guide*\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the queue name\. For more information, see [Name type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html) in the *AWS CloudFormation User Guide*\.   
If you specify a name, you can't perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReceiveMessageWaitTimeSeconds`  <a name="cfn-sqs-queue-receivemessagewaittimeseconds"></a>
Specifies the duration, in seconds, that the ReceiveMessage action call waits until a message is in the queue in order to include it in the response, rather than returning an empty response if a message isn't yet available\. You can specify an integer from 1 to 20\. Short polling is used as the default or when you specify 0 for this property\. For more information, see [Consuming messages using long polling](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html#sqs-long-polling) in the *Amazon SQS Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedriveAllowPolicy`  <a name="cfn-sqs-queue-redriveallowpolicy"></a>
The string that includes the parameters for the permissions for the dead\-letter queue redrive permission and which source queues can specify dead\-letter queues as a JSON object\. The parameters are as follows:  
+ `redrivePermission`: The permission type that defines which source queues can specify the current queue as the dead\-letter queue\. Valid values are:
  + `allowAll`: \(Default\) Any source queues in this AWS account in the same Region can specify this queue as the dead\-letter queue\.
  + `denyAll`: No source queues can specify this queue as the dead\-letter queue\.
  + `byQueue`: Only queues specified by the `sourceQueueArns` parameter can specify this queue as the dead\-letter queue\.
+ `sourceQueueArns`: The Amazon Resource Names \(ARN\)s of the source queues that can specify this queue as the dead\-letter queue and redrive messages\. You can specify this parameter only when the `redrivePermission` parameter is set to `byQueue`\. You can specify up to 10 source queue ARNs\. To allow more than 10 source queues to specify dead\-letter queues, set the `redrivePermission` parameter to `allowAll`\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedrivePolicy`  <a name="cfn-sqs-queue-redrivepolicy"></a>
The string that includes the parameters for the dead\-letter queue functionality of the source queue as a JSON object\. The parameters are as follows:  
+ `deadLetterTargetArn`: The Amazon Resource Name \(ARN\) of the dead\-letter queue to which Amazon SQS moves messages after the value of `maxReceiveCount` is exceeded\.
+ `maxReceiveCount`: The number of times a message is delivered to the source queue before being moved to the dead\-letter queue\. When the `ReceiveCount` for a message exceeds the `maxReceiveCount` for a queue, Amazon SQS moves the message to the dead\-letter\-queue\.
The dead\-letter queue of a FIFO queue must also be a FIFO queue\. Similarly, the dead\-letter queue of a standard queue must also be a standard queue\.
 *JSON*   
 `{ "deadLetterTargetArn" : String, "maxReceiveCount" : Integer }`   
 *YAML*   
 `deadLetterTargetArn : String `   
 `maxReceiveCount : Integer `   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqsManagedSseEnabled`  <a name="cfn-sqs-queue-sqsmanagedsseenabled"></a>
 Enables server\-side queue encryption using SQS owned encryption keys\. Only one server\-side encryption option is supported per queue \(for example, [SSE\-KMS](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-configure-sse-existing-queue.html) or [SSE\-SQS](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-configure-sqs-sse-queue.html)\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sqs-queue-tags"></a>
The tags that you attach to this queue\. For more information, see [Resource tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisibilityTimeout`  <a name="cfn-sqs-queue-visibilitytimeout"></a>
The length of time during which a message will be unavailable after a message is delivered from the queue\. This blocks other components from receiving the same message and gives the initial component time to process and delete the message from the queue\.  
Values must be from 0 to 43,200 seconds \(12 hours\)\. If you don't specify a value, AWS CloudFormation uses the default value of 30 seconds\.  
For more information about Amazon SQS queue visibility timeouts, see [Visibility timeout](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-visibility-timeout.html) in the *Amazon SQS Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sqs-queue-return-values"></a>

### Ref<a name="aws-resource-sqs-queue-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the queue URL\. For example: 

 `{ "Ref": "https://sqs.us-east-2.amazonaws.com/123456789012/ab1-MyQueue-A2BCDEF3GHI4" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sqs-queue-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-sqs-queue-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the queue\. For example: `arn:aws:sqs:us-east-2:123456789012:mystack-myqueue-15PG5C2FC1CW8`\.

`QueueName`  <a name="QueueName-fn::getatt"></a>
Returns the queue name\. For example: `mystack-myqueue-1VF9BKQH5BJVI`\.

`QueueUrl`  <a name="QueueUrl-fn::getatt"></a>
Returns the URLs of the queues from the policy\.

## Examples<a name="aws-resource-sqs-queue--examples"></a>



### Amazon SQS Queue with CloudWatch Alarms<a name="aws-resource-sqs-queue--examples--Amazon_SQS_Queue_with_CloudWatch_Alarms"></a>

#### JSON<a name="aws-resource-sqs-queue--examples--Amazon_SQS_Queue_with_CloudWatch_Alarms--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
 
  "Description" : "This example template shows how to create an Amazon SQS queue with CloudWatch alarms on queue depth. This template creates an Amazon SQS queue and one or more CloudWatch alarms. You will be billed for the AWS resources used if you create a stack using this template.",
 
  "Parameters" : {
    "AlarmEmail": {
      "Default": "jane.doe@example.com",
      "Description": "Email address to notify of operational issues",
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
        "AlarmDescription": "Alarm if queue depth increases to more than 10 messages",
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
      "Description" : "URL of new Amazon SQS Queue",
      "Value" : { "Ref" : "MyQueue" }
    },
    "QueueARN" : {
      "Description" : "ARN of new Amazon SQS Queue",
      "Value" : { "Fn::GetAtt" : ["MyQueue", "Arn"]}
    },
    "QueueName" : {
      "Description" : "Name new Amazon SQS Queue",
      "Value" : { "Fn::GetAtt" : ["MyQueue", "QueueName"]}
    }
  }
}
```

#### YAML<a name="aws-resource-sqs-queue--examples--Amazon_SQS_Queue_with_CloudWatch_Alarms--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: "This example template shows how to create an Amazon SQS queue with CloudWatch alarms on queue depth. This template creates an Amazon SQS queue and one or more CloudWatch alarms. You will be billed for the AWS resources used if you create a stack using this template."
Parameters: 
  AlarmEmail: 
    Default: "jane.doe@example.com"
    Description: "Email address to notify of operational issues"
    Type: "String"
Resources: 
  MyQueue: 
    Type: AWS::SQS::Queue
    Properties: 
      QueueName: "SampleQueue"
  AlarmTopic: 
    Type: AWS::SNS::Topic
    Properties: 
      Subscription: 
        - 
          Endpoint: 
            Ref: "AlarmEmail"
          Protocol: "email"
  QueueDepthAlarm: 
    Type: AWS::CloudWatch::Alarm
    Properties: 
      AlarmDescription: "Alarm if queue depth increases to more than 10 messages"
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
    Description: "URL of new Amazon SQS Queue"
    Value: 
      Ref: "MyQueue"
  QueueARN: 
    Description: "ARN of new AmazonSQS Queue"
    Value: 
      Fn::GetAtt: 
        - "MyQueue"
        - "Arn"
  QueueName: 
    Description: "Name of new Amazon SQS Queue"
    Value: 
      Fn::GetAtt: 
        - "MyQueue"
        - "QueueName"
```

### Amazon SQS Queue with a Dead\-Letter Queue<a name="aws-resource-sqs-queue--examples--Amazon_SQS_Queue_with_a_Dead-Letter_Queue"></a>

The following example template creates a source queue and a dead\-letter queue\.

**Note**  
Because the source queue specifies the dead\-letter queue in its redrive policy, the source queue is dependent on the creation of the dead\-letter queue\.

#### JSON<a name="aws-resource-sqs-queue--examples--Amazon_SQS_Queue_with_a_Dead-Letter_Queue--json"></a>

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
      "Description" : "ARN of source queue",
      "Value" : { "Fn::GetAtt" : ["MySourceQueue", "Arn"]}
    },
    "DeadLetterQueueURL" : {
      "Description" : "URL of dead-letter queue",
      "Value" : { "Ref" : "MyDeadLetterQueue" }
    },
    "DeadLetterQueueARN" : {
      "Description" : "ARN of dead-letter queue",
      "Value" : { "Fn::GetAtt" : ["MyDeadLetterQueue", "Arn"]}
    }    
  }
}
```

#### YAML<a name="aws-resource-sqs-queue--examples--Amazon_SQS_Queue_with_a_Dead-Letter_Queue--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MySourceQueue: 
    Type: AWS::SQS::Queue
    Properties: 
      RedrivePolicy: 
        deadLetterTargetArn: 
          Fn::GetAtt: 
            - "MyDeadLetterQueue"
            - "Arn"
        maxReceiveCount: 5
  MyDeadLetterQueue: 
    Type: AWS::SQS::Queue
Outputs: 
  SourceQueueURL: 
    Description: "URL of source queue"
    Value: 
      Ref: "MySourceQueue"
  SourceQueueARN: 
    Description: "ARN of source queue"
    Value: 
      Fn::GetAtt: 
        - "MySourceQueue"
        - "Arn"
  DeadLetterQueueURL: 
    Description: "URL of dead-letter queue"
    Value: 
      Ref: "MyDeadLetterQueue"
  DeadLetterQueueARN: 
    Description: "ARN of dead-letter queue"
    Value: 
      Fn::GetAtt: 
        - "MyDeadLetterQueue"
        - "Arn"
```

## See also<a name="aws-resource-sqs-queue--seealso"></a>
+  [What is Amazon Simple Queue Service?](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html) in the *Amazon SQS Developer Guide* 
+  ` [CreateQueue](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_CreateQueue.html) ` in the *Amazon SQS API Reference* 
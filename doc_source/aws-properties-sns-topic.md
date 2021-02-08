# AWS::SNS::Topic<a name="aws-properties-sns-topic"></a>

The `AWS::SNS::Topic` resource creates a topic to which notifications can be published\.

**Note**  
One account can create a maximum of 100,000 standard topics and 1,000 FIFO topics\. For more information, see [Amazon Simple Notification Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/sns.html) in the *AWS General Reference*\.

## Syntax<a name="aws-properties-sns-topic-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sns-topic-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::Topic",
  "Properties" : {
      "[ContentBasedDeduplication](#cfn-sns-topic-contentbaseddeduplication)" : Boolean,
      "[DisplayName](#cfn-sns-topic-displayname)" : String,
      "[FifoTopic](#cfn-sns-topic-fifotopic)" : Boolean,
      "[KmsMasterKeyId](#cfn-sns-topic-kmsmasterkeyid)" : String,
      "[Subscription](#cfn-sns-topic-subscription)" : [ Subscription, ... ],
      "[Tags](#cfn-sns-topic-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TopicName](#cfn-sns-topic-topicname)" : String
    }
}
```

### YAML<a name="aws-properties-sns-topic-syntax.yaml"></a>

```
Type: AWS::SNS::Topic
Properties: 
  [ContentBasedDeduplication](#cfn-sns-topic-contentbaseddeduplication): Boolean
  [DisplayName](#cfn-sns-topic-displayname): String
  [FifoTopic](#cfn-sns-topic-fifotopic): Boolean
  [KmsMasterKeyId](#cfn-sns-topic-kmsmasterkeyid): String
  [Subscription](#cfn-sns-topic-subscription): 
    - Subscription
  [Tags](#cfn-sns-topic-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TopicName](#cfn-sns-topic-topicname): String
```

## Properties<a name="aws-properties-sns-topic-properties"></a>

`ContentBasedDeduplication`  <a name="cfn-sns-topic-contentbaseddeduplication"></a>
Enables content\-based deduplication for FIFO topics\.  
+ By default, `ContentBasedDeduplication` is set to `false`\. If you create a FIFO topic and this attribute is `false`, you must specify a value for the `MessageDeduplicationId` parameter for the [Publish](https://docs.aws.amazon.com/sns/latest/api/API_Publish.html) action\. 
+ When you set `ContentBasedDeduplication` to `true`, Amazon SNS uses a SHA\-256 hash to generate the `MessageDeduplicationId` using the body of the message \(but not the attributes of the message\)\.

  \(Optional\) To override the generated value, you can specify a value for the the `MessageDeduplicationId` parameter for the `Publish` action\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-sns-topic-displayname"></a>
The display name to use for an Amazon SNS topic with SMS subscriptions\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FifoTopic`  <a name="cfn-sns-topic-fifotopic"></a>
Set to true to create a FIFO topic\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsMasterKeyId`  <a name="cfn-sns-topic-kmsmasterkeyid"></a>
The ID of an AWS\-managed customer master key \(CMK\) for Amazon SNS or a custom CMK\. For more information, see [Key Terms](https://docs.aws.amazon.com/sns/latest/dg/sns-server-side-encryption.html#sse-key-terms)\. For more examples, see ` [KeyId](https://docs.aws.amazon.com/kms/latest/APIReference/API_DescribeKey.html#API_DescribeKey_RequestParameters) ` in the *AWS Key Management Service API Reference*\.  
This property applies only to [server\-side\-encryption](https://docs.aws.amazon.com/sns/latest/dg/sns-server-side-encryption.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subscription`  <a name="cfn-sns-topic-subscription"></a>
The SNS subscriptions \(endpoints\) for this topic\.  
*Required*: No  
*Type*: [List](aws-properties-sns-subscription.md) of [Subscription](aws-properties-sns-subscription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sns-topic-tags"></a>
The list of tags to add to a new topic\.  
To be able to tag a topic on creation, you must have the `sns:CreateTopic` and `sns:TagResource` permissions\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicName`  <a name="cfn-sns-topic-topicname"></a>
The name of the topic you want to create\. Topic names must include only uppercase and lowercase ASCII letters, numbers, underscores, and hyphens, and must be between 1 and 256 characters long\. FIFO topic names must end with `.fifo`\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the topic name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you can't perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-properties-sns-topic-return-values"></a>

### Ref<a name="aws-properties-sns-topic-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the topic ARN, for example: `arn:aws:sns:us-east-1:123456789012:mystack-mytopic-NZJ5JSMVGFIE`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-sns-topic-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-sns-topic-return-values-fn--getatt-fn--getatt"></a>

`TopicName`  <a name="TopicName-fn::getatt"></a>
Returns the name of an Amazon SNS topic\.

## Examples<a name="aws-properties-sns-topic--examples"></a>



### An Amazon SNS topic with two Amazon SQS queue subscriptions<a name="aws-properties-sns-topic--examples--An_Amazon_SNS_topic_with_two_Amazon_SQS_queue_subscriptions"></a>

#### JSON<a name="aws-properties-sns-topic--examples--An_Amazon_SNS_topic_with_two_Amazon_SQS_queue_subscriptions--json"></a>

```
"MySNSTopic" : {
  "Type" : "AWS::SNS::Topic",
  "Properties" : {
    "Subscription" : [{
      "Endpoint" : { "Fn::GetAtt" : [ "MyQueue1", "Arn" ] },
      "Protocol" : "sqs"
    }, {
      "Endpoint" : { "Fn::GetAtt" : [ "MyQueue2", "Arn" ] },
      "Protocol" : "sqs"
    }],
    "TopicName" : "SampleTopic"
  }
}
```

#### YAML<a name="aws-properties-sns-topic--examples--An_Amazon_SNS_topic_with_two_Amazon_SQS_queue_subscriptions--yaml"></a>

```
MySNSTopic:
  Type: AWS::SNS::Topic
  Properties:
    Subscription:
      - Endpoint:
          Fn::GetAtt:
            - "MyQueue1"
            - "Arn"
        Protocol: "sqs"
      - Endpoint:
          Fn::GetAtt:
            - "MyQueue2"
            - "Arn"
        Protocol: "sqs"
    TopicName: "SampleTopic"
```

## See also<a name="aws-properties-sns-topic--seealso"></a>
+  [Using an AWS CloudFormation Template to Create a Topic that Sends Messages to Amazon SQS Queues](https://docs.aws.amazon.com/sns/latest/dg/SendMessageToSQS.cloudformation.html) in the *Amazon Simple Notification Service Developer Guide* 
+ The [Using AWS CloudFormation](https://docs.aws.amazon.com/sns/latest/dg/fifo-topic-code-examples.html#fifo-topic-cfn) code example for FIFO topics in the *Amazon Simple Notification Service Developer Guide*
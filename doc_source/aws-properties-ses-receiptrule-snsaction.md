# AWS::SES::ReceiptRule SNSAction<a name="aws-properties-ses-receiptrule-snsaction"></a>

When included in a receipt rule, this action publishes a notification to Amazon Simple Notification Service \(Amazon SNS\)\. This action includes a complete copy of the email content in the Amazon SNS notifications\. Amazon SNS notifications for all other actions simply provide information about the email\. They don't include the email content itself\.

If you own the Amazon SNS topic, you don't need to do anything to give Amazon SES permission to publish emails to it\. However, if you don't own the Amazon SNS topic, you need to attach a policy to the topic to give Amazon SES permissions to access it\. For information about giving permissions, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-permissions.html)\.

**Important**  
You can only publish emails that are 150 KB or less \(including the header\) to Amazon SNS\. Emails that are larger than 150 KB aren't published\. If you anticipate emails larger than 150 KB, use the S3 action instead\.

For information about using a receipt rule to publish an Amazon SNS notification, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-action-sns.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-snsaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-snsaction-syntax.json"></a>

```
{
  "[Encoding](#cfn-ses-receiptrule-snsaction-encoding)" : String,
  "[TopicArn](#cfn-ses-receiptrule-snsaction-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-snsaction-syntax.yaml"></a>

```
  [Encoding](#cfn-ses-receiptrule-snsaction-encoding): String
  [TopicArn](#cfn-ses-receiptrule-snsaction-topicarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-snsaction-properties"></a>

`Encoding`  <a name="cfn-ses-receiptrule-snsaction-encoding"></a>
The encoding to use for the email within the Amazon SNS notification\. UTF\-8 is easier to use, but may not preserve all special characters when a message was encoded with a different encoding format\. Base64 preserves all special characters\. The default value is UTF\-8\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Base64 | UTF-8`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="cfn-ses-receiptrule-snsaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify\. You can find the ARN of a topic by using the [ListTopics](https://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html) operation in the Amazon SNS API\.  
For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
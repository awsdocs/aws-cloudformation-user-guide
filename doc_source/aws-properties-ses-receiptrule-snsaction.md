# Amazon Simple Email Service ReceiptRule SNSAction<a name="aws-properties-ses-receiptrule-snsaction"></a>

<a name="aws-properties-ses-receiptrule-snsaction-description"></a>The `SNSAction` property type includes an action in an Amazon SES receipt rule that publishes a notification to Amazon SNS\.

If you own the Amazon SNS topic, you don't need to do anything to give Amazon SES permission to publish emails to it\. However, if you don't own the Amazon SNS topic, you need to attach a policy to the topic to give Amazon SES permissions to access it\. For information about giving permissions, see [Giving Permissions to Amazon SES for Email Receiving](url-ses-dev;receiving-email-permissions.html) in the *Amazon Simple Email Service Developer Guide*\.

**Important**  
You can only publish emails that are 150 KB or less \(including the header\) to Amazon SNS\. Larger emails will bounce\. If you anticipate emails larger than 150 KB, use the S3 action instead\.

For more information, see [SNS Action](url-ses-dev;receiving-email-action-sns.html) in the *Amazon Simple Email Service Developer Guide*\.

<a name="aws-properties-ses-receiptrule-snsaction-inheritance"></a> `SNSAction` is a property of the [Amazon Simple Email Service ReceiptRule Action](aws-properties-ses-receiptrule-action.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-snsaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-snsaction-syntax.json"></a>

```
{
  "[TopicArn](#cfn-ses-receiptrule-snsaction-topicarn)" : String,
  "[Encoding](#cfn-ses-receiptrule-snsaction-encoding)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-snsaction-syntax.yaml"></a>

```
[TopicArn](#cfn-ses-receiptrule-snsaction-topicarn): String
[Encoding](#cfn-ses-receiptrule-snsaction-encoding): String
```

## Properties<a name="aws-properties-ses-receiptrule-snsaction-properties"></a>

`Encoding`  <a name="cfn-ses-receiptrule-snsaction-encoding"></a>
The encoding to use for the email within the Amazon SNS notification\. UTF\-8 is easier to use, but may not preserve all special characters when a message was encoded with a different encoding format\. Base64 preserves all special characters\. The default value is UTF\-8\.  
Valid values include `Base64` and `UTF-8`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TopicArn`  <a name="cfn-ses-receiptrule-snsaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify\. An example of an Amazon SNS topic ARN is `arn:aws:sns:us-west-2:123456789012:MyTopic`\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-snsaction-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [Giving Permissions to Amazon SES for Email Receiving](url-ses-dev;receiving-email-permissions.html) in the *Amazon Simple Email Service Developer Guide*
+ [SNS Action](url-ses-dev;receiving-email-action-sns.html) in the *Amazon Simple Email Service Developer Guide*
+ [SNSAction](url-ses-api;API_SNSAction.html) in the *Amazon Simple Email Service API Reference*
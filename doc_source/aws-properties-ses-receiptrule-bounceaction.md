# Amazon Simple Email Service ReceiptRule BounceAction<a name="aws-properties-ses-receiptrule-bounceaction"></a>

<a name="aws-properties-ses-receiptrule-bounceaction-description"></a>The `BounceAction` property type includes an action in an Amazon SES receipt rule that rejects the received email by returning a bounce response to the sender and, optionally, publishes a notification to Amazon SNS\.

<a name="aws-properties-ses-receiptrule-bounceaction-inheritance"></a> `BounceAction` is a property of the [Amazon Simple Email Service ReceiptRule Action](aws-properties-ses-receiptrule-action.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-bounceaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-bounceaction-syntax.json"></a>

```
{
  "[Sender](#cfn-ses-receiptrule-bounceaction-sender)" : String,
  "[SmtpReplyCode](#cfn-ses-receiptrule-bounceaction-smtpreplycode)" : String,
  "[Message](#cfn-ses-receiptrule-bounceaction-message)" : String,
  "[TopicArn](#cfn-ses-receiptrule-bounceaction-topicarn)" : String,
  "[StatusCode](#cfn-ses-receiptrule-bounceaction-statuscode)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-bounceaction-syntax.yaml"></a>

```
[Sender](#cfn-ses-receiptrule-bounceaction-sender): String
[SmtpReplyCode](#cfn-ses-receiptrule-bounceaction-smtpreplycode): String
[Message](#cfn-ses-receiptrule-bounceaction-message): String
[TopicArn](#cfn-ses-receiptrule-bounceaction-topicarn): String
[StatusCode](#cfn-ses-receiptrule-bounceaction-statuscode): String
```

## Properties<a name="aws-properties-ses-receiptrule-bounceaction-properties"></a>

`Message`  <a name="cfn-ses-receiptrule-bounceaction-message"></a>
Human\-readable text to include in the bounce message\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Sender`  <a name="cfn-ses-receiptrule-bounceaction-sender"></a>
The email address of the sender of the bounced email\. This is the address from which the bounce message will be sent\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SmtpReplyCode`  <a name="cfn-ses-receiptrule-bounceaction-smtpreplycode"></a>
The SMTP reply code, as defined by [RFC 5321](https://tools.ietf.org/html/rfc5321)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TopicArn`  <a name="cfn-ses-receiptrule-bounceaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the bounce action is taken\. An example of an Amazon SNS topic ARN is `arn:aws:sns:us-west-2:123456789012:MyTopic`\. For more information about Amazon SNS topics, see [Create a Topic](url-sns-dg;CreateTopic.html) in the *Amazon Simple Notification Service Developer Guide*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StatusCode`  <a name="cfn-ses-receiptrule-bounceaction-statuscode"></a>
The SMTP enhanced status code, as defined by [RFC 3463](https://tools.ietf.org/html/rfc3463)\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-bounceaction-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [CreateReceiptRule](url-ses-api;API_CreateReceiptRule.html) in the *Amazon Simple Email Service API Reference*
+ [BounceAction](url-ses-api;API_BounceAction.html) in the *Amazon Simple Email Service API Reference*
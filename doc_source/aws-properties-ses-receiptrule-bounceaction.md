# AWS::SES::ReceiptRule BounceAction<a name="aws-properties-ses-receiptrule-bounceaction"></a>

When included in a receipt rule, this action rejects the received email by returning a bounce response to the sender and, optionally, publishes a notification to Amazon Simple Notification Service \(Amazon SNS\)\.

For information about sending a bounce message in response to a received email, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-action-bounce.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-bounceaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-bounceaction-syntax.json"></a>

```
{
  "[Message](#cfn-ses-receiptrule-bounceaction-message)" : String,
  "[Sender](#cfn-ses-receiptrule-bounceaction-sender)" : String,
  "[SmtpReplyCode](#cfn-ses-receiptrule-bounceaction-smtpreplycode)" : String,
  "[StatusCode](#cfn-ses-receiptrule-bounceaction-statuscode)" : String,
  "[TopicArn](#cfn-ses-receiptrule-bounceaction-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-bounceaction-syntax.yaml"></a>

```
  [Message](#cfn-ses-receiptrule-bounceaction-message): String
  [Sender](#cfn-ses-receiptrule-bounceaction-sender): String
  [SmtpReplyCode](#cfn-ses-receiptrule-bounceaction-smtpreplycode): String
  [StatusCode](#cfn-ses-receiptrule-bounceaction-statuscode): String
  [TopicArn](#cfn-ses-receiptrule-bounceaction-topicarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-bounceaction-properties"></a>

`Message`  <a name="cfn-ses-receiptrule-bounceaction-message"></a>
Human\-readable text to include in the bounce message\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sender`  <a name="cfn-ses-receiptrule-bounceaction-sender"></a>
The email address of the sender of the bounced email\. This is the address that the bounce message is sent from\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmtpReplyCode`  <a name="cfn-ses-receiptrule-bounceaction-smtpreplycode"></a>
The SMTP reply code, as defined by [RFC 5321](https://tools.ietf.org/html/rfc5321)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusCode`  <a name="cfn-ses-receiptrule-bounceaction-statuscode"></a>
The SMTP enhanced status code, as defined by [RFC 3463](https://tools.ietf.org/html/rfc3463)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="cfn-ses-receiptrule-bounceaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the bounce action is taken\. You can find the ARN of a topic by using the [ListTopics](https://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html) operation in the Amazon SNS API\.  
For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
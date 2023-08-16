# AWS::SES::ConfigurationSetEventDestination EventDestination<a name="aws-properties-ses-configurationseteventdestination-eventdestination"></a>

Contains information about an event destination\.

**Note**  
When you create or update an event destination, you must provide one, and only one, destination\. The destination can be Amazon CloudWatch, Amazon Kinesis Firehose or Amazon Simple Notification Service \(Amazon SNS\)\.

Event destinations are associated with configuration sets, which enable you to publish email sending events to Amazon CloudWatch, Amazon Kinesis Firehose, or Amazon Simple Notification Service \(Amazon SNS\)\. For information about using configuration sets, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/dg/monitor-sending-activity.html)\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax.json"></a>

```
{
  "[CloudWatchDestination](#cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination)" : CloudWatchDestination,
  "[Enabled](#cfn-ses-configurationseteventdestination-eventdestination-enabled)" : Boolean,
  "[KinesisFirehoseDestination](#cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination)" : KinesisFirehoseDestination,
  "[MatchingEventTypes](#cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes)" : [ String, ... ],
  "[Name](#cfn-ses-configurationseteventdestination-eventdestination-name)" : String,
  "[SnsDestination](#cfn-ses-configurationseteventdestination-eventdestination-snsdestination)" : SnsDestination
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax.yaml"></a>

```
  [CloudWatchDestination](#cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination): 
    CloudWatchDestination
  [Enabled](#cfn-ses-configurationseteventdestination-eventdestination-enabled): Boolean
  [KinesisFirehoseDestination](#cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination): 
    KinesisFirehoseDestination
  [MatchingEventTypes](#cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes): 
    - String
  [Name](#cfn-ses-configurationseteventdestination-eventdestination-name): String
  [SnsDestination](#cfn-ses-configurationseteventdestination-eventdestination-snsdestination): 
    SnsDestination
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-eventdestination-properties"></a>

`CloudWatchDestination`  <a name="cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination"></a>
An object that contains the names, default values, and sources of the dimensions associated with an Amazon CloudWatch event destination\.  
*Required*: No  
*Type*: [CloudWatchDestination](aws-properties-ses-configurationseteventdestination-cloudwatchdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-ses-configurationseteventdestination-eventdestination-enabled"></a>
Sets whether Amazon SES publishes events to this destination when you send an email with the associated configuration set\. Set to `true` to enable publishing to this destination; set to `false` to prevent publishing to this destination\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisFirehoseDestination`  <a name="cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination"></a>
An object that contains the delivery stream ARN and the IAM role ARN associated with an Amazon Kinesis Firehose event destination\.  
*Required*: No  
*Type*: [KinesisFirehoseDestination](aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchingEventTypes`  <a name="cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes"></a>
The type of email sending events to publish to the event destination\.  
+ `send` \- The send request was successful and SES will attempt to deliver the message to the recipient’s mail server\. \(If account\-level or global suppression is being used, SES will still count it as a send, but delivery is suppressed\.\)
+ `reject` \- SES accepted the email, but determined that it contained a virus and didn’t attempt to deliver it to the recipient’s mail server\.
+ `bounce` \- \(*Hard bounce*\) The recipient's mail server permanently rejected the email\. \(*Soft bounces* are only included when SES fails to deliver the email after retrying for a period of time\.\)
+ `complaint` \- The email was successfully delivered to the recipient’s mail server, but the recipient marked it as spam\.
+ `delivery` \- SES successfully delivered the email to the recipient's mail server\.
+ `open` \- The recipient received the message and opened it in their email client\.
+ `click` \- The recipient clicked one or more links in the email\.
+ `renderingFailure` \- The email wasn't sent because of a template rendering issue\. This event type can occur when template data is missing, or when there is a mismatch between template parameters and data\. \(This event type only occurs when you send email using the [https://docs.aws.amazon.com/ses/latest/APIReference/API_SendTemplatedEmail.html](https://docs.aws.amazon.com/ses/latest/APIReference/API_SendTemplatedEmail.html) or [https://docs.aws.amazon.com/ses/latest/APIReference/API_SendBulkTemplatedEmail.html](https://docs.aws.amazon.com/ses/latest/APIReference/API_SendBulkTemplatedEmail.html) API operations\.\) 
+ `deliveryDelay` \- The email couldn't be delivered to the recipient’s mail server because a temporary issue occurred\. Delivery delays can occur, for example, when the recipient's inbox is full, or when the receiving email server experiences a transient issue\.
+ `subscription` \- The email was successfully delivered, but the recipient updated their subscription preferences by clicking on an *unsubscribe* link as part of your [subscription management](https://docs.aws.amazon.com/ses/latest/dg/sending-email-subscription-management.html)\.
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ses-configurationseteventdestination-eventdestination-name"></a>
The name of the event destination\. The name must meet the following requirements:  
+ Contain only ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain 64 characters or fewer\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsDestination`  <a name="cfn-ses-configurationseteventdestination-eventdestination-snsdestination"></a>
An object that contains the topic ARN associated with an Amazon Simple Notification Service \(Amazon SNS\) event destination\.  
*Required*: No  
*Type*: [SnsDestination](aws-properties-ses-configurationseteventdestination-snsdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
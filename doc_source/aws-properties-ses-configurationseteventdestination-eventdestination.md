# AWS::SES::ConfigurationSetEventDestination EventDestination<a name="aws-properties-ses-configurationseteventdestination-eventdestination"></a>

Contains information about the event destination that the specified email sending events are published to\.

**Note**  
When you specify an event destination, you must provide one, and only one, destination\. The destination can be Amazon CloudWatch, Amazon Kinesis Data Firehose or Amazon Simple Notification Service \(Amazon SNS\)\.

Event destinations are associated with configuration sets, which enable you to publish email sending events to Amazon CloudWatch, Amazon Kinesis Data Firehose, or Amazon Simple Notification Service \(Amazon SNS\)\. For information about using configuration sets, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/monitor-sending-activity.html)\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax.json"></a>

```
{
  "[CloudWatchDestination](#cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination)" : [CloudWatchDestination](aws-properties-ses-configurationseteventdestination-cloudwatchdestination.md),
  "[Enabled](#cfn-ses-configurationseteventdestination-eventdestination-enabled)" : Boolean,
  "[KinesisFirehoseDestination](#cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination)" : [KinesisFirehoseDestination](aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination.md),
  "[MatchingEventTypes](#cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes)" : [ String, ... ],
  "[Name](#cfn-ses-configurationseteventdestination-eventdestination-name)" : String
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax.yaml"></a>

```
  [CloudWatchDestination](#cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination): 
    [CloudWatchDestination](aws-properties-ses-configurationseteventdestination-cloudwatchdestination.md)
  [Enabled](#cfn-ses-configurationseteventdestination-eventdestination-enabled): Boolean
  [KinesisFirehoseDestination](#cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination): 
    [KinesisFirehoseDestination](aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination.md)
  [MatchingEventTypes](#cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes): 
    - String
  [Name](#cfn-ses-configurationseteventdestination-eventdestination-name): String
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
An object that contains the delivery stream ARN and the IAM role ARN associated with an Amazon Kinesis Data Firehose event destination\.  
*Required*: No  
*Type*: [KinesisFirehoseDestination](aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchingEventTypes`  <a name="cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes"></a>
The type of email sending events to publish to the event destination\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ses-configurationseteventdestination-eventdestination-name"></a>
The name of the event destination\. The name must:  
+ This value can only contain ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain less than 64 characters\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
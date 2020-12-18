# AWS::SES::ConfigurationSetEventDestination EventDestination<a name="aws-properties-ses-configurationseteventdestination-eventdestination"></a>

Contains information about the event destination that email sending events are published to\. Event destinations are associated with configuration sets\. When you specify an event destination, you provide one, and only one, destination\. You can send event data to Amazon CloudWatch or Amazon Kinesis Data Firehose\. For more information about using configuration sets, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/monitor-sending-activity.html)\.

**Note**  
You can't specify Amazon SNS event destinations in CloudFormation templates\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax.json"></a>

```
{
  "[CloudWatchDestination](#cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination)" : CloudWatchDestination,
  "[Enabled](#cfn-ses-configurationseteventdestination-eventdestination-enabled)" : Boolean,
  "[KinesisFirehoseDestination](#cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination)" : KinesisFirehoseDestination,
  "[MatchingEventTypes](#cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes)" : [ String, ... ],
  "[Name](#cfn-ses-configurationseteventdestination-eventdestination-name)" : String
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
+ This value can only contain ASCII letters \(a–z, A–Z\), numbers \(0–9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain fewer than 64 characters\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
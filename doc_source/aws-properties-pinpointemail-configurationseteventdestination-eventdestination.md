# AWS::PinpointEmail::ConfigurationSetEventDestination EventDestination<a name="aws-properties-pinpointemail-configurationseteventdestination-eventdestination"></a>

In Amazon Pinpoint, *events* include message sends, deliveries, opens, clicks, bounces, and complaints\. *Event destinations* are places that you can send information about these events to\. For example, you can send event data to Amazon SNS to receive notifications when you receive bounces or complaints, or you can use Amazon Kinesis Data Firehose to stream data to Amazon S3 for long\-term storage\.

## Syntax<a name="aws-properties-pinpointemail-configurationseteventdestination-eventdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationseteventdestination-eventdestination-syntax.json"></a>

```
{
  "[CloudWatchDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-cloudwatchdestination)" : CloudWatchDestination,
  "[Enabled](#cfn-pinpointemail-configurationseteventdestination-eventdestination-enabled)" : Boolean,
  "[KinesisFirehoseDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-kinesisfirehosedestination)" : KinesisFirehoseDestination,
  "[MatchingEventTypes](#cfn-pinpointemail-configurationseteventdestination-eventdestination-matchingeventtypes)" : [ String, ... ],
  "[PinpointDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-pinpointdestination)" : PinpointDestination,
  "[SnsDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-snsdestination)" : SnsDestination
}
```

### YAML<a name="aws-properties-pinpointemail-configurationseteventdestination-eventdestination-syntax.yaml"></a>

```
  [CloudWatchDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-cloudwatchdestination): 
    CloudWatchDestination
  [Enabled](#cfn-pinpointemail-configurationseteventdestination-eventdestination-enabled): Boolean
  [KinesisFirehoseDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-kinesisfirehosedestination): 
    KinesisFirehoseDestination
  [MatchingEventTypes](#cfn-pinpointemail-configurationseteventdestination-eventdestination-matchingeventtypes): 
    - String
  [PinpointDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-pinpointdestination): 
    PinpointDestination
  [SnsDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination-snsdestination): 
    SnsDestination
```

## Properties<a name="aws-properties-pinpointemail-configurationseteventdestination-eventdestination-properties"></a>

`CloudWatchDestination`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestination-cloudwatchdestination"></a>
An object that defines an Amazon CloudWatch destination for email events\. You can use Amazon CloudWatch to monitor and gain insights on your email sending metrics\.  
*Required*: No  
*Type*: [CloudWatchDestination](aws-properties-pinpointemail-configurationseteventdestination-cloudwatchdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestination-enabled"></a>
If `true`, the event destination is enabled\. When the event destination is enabled, the specified event types are sent to the destinations in this `EventDestinationDefinition`\.  
If `false`, the event destination is disabled\. When the event destination is disabled, events aren't sent to the specified destinations\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisFirehoseDestination`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestination-kinesisfirehosedestination"></a>
An object that defines an Amazon Kinesis Data Firehose destination for email events\. You can use Amazon Kinesis Data Firehose to stream data to other services, such as Amazon S3 and Amazon Redshift\.  
*Required*: No  
*Type*: [KinesisFirehoseDestination](aws-properties-pinpointemail-configurationseteventdestination-kinesisfirehosedestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchingEventTypes`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestination-matchingeventtypes"></a>
The types of events that Amazon Pinpoint sends to the specified event destinations\. Acceptable values: `SEND`, `REJECT`, `BOUNCE`, `COMPLAINT`, `DELIVERY`, `OPEN`, `CLICK`, and `RENDERING_FAILURE`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PinpointDestination`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestination-pinpointdestination"></a>
An object that defines a Amazon Pinpoint destination for email events\. You can use Amazon Pinpoint events to create attributes in Amazon Pinpoint projects\. You can use these attributes to create segments for your campaigns\.  
*Required*: No  
*Type*: [PinpointDestination](aws-properties-pinpointemail-configurationseteventdestination-pinpointdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsDestination`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestination-snsdestination"></a>
An object that defines an Amazon SNS destination for email events\. You can use Amazon SNS to send notification when certain email events occur\.  
*Required*: No  
*Type*: [SnsDestination](aws-properties-pinpointemail-configurationseteventdestination-snsdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
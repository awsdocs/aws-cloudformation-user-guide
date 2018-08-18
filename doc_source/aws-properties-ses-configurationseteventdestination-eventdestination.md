# Amazon Simple Email Service ConfigurationSetEventDestination EventDestination<a name="aws-properties-ses-configurationseteventdestination-eventdestination"></a>

<a name="aws-properties-ses-configurationseteventdestination-eventdestination-description"></a>For an Amazon SES configuration set event destination, the `EventDestination` property type specifies information about the event destination that the specified email sending events will be published to\.

**Note**  
When you create or update an event destination, you must provide one, and only one, destination\. The destination can be Amazon CloudWatch or Amazon Kinesis Firehose\.

Event destinations are associated with configuration sets, which enable you to publish email sending events to Amazon CloudWatch or Amazon Kinesis Firehose\. For information, see [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*\.

<a name="aws-properties-ses-configurationseteventdestination-eventdestination-inheritance"></a> `EventDestination` is a property of the [AWS::SES::ConfigurationSetEventDestination](aws-resource-ses-configurationseteventdestination.md) resource\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax.json"></a>

```
{
  "[CloudWatchDestination](#cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination)" : [*CloudWatchDestination*](aws-properties-ses-configurationseteventdestination-cloudwatchdestination.md),
  "[Enabled](#cfn-ses-configurationseteventdestination-eventdestination-enabled)" : Boolean,
  "[MatchingEventTypes](#cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes)" : [ String, ... ],
  "[Name](#cfn-ses-configurationseteventdestination-eventdestination-name)" : String,
  "[KinesisFirehoseDestination](#cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination)" : [*KinesisFirehoseDestination*](aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination.md)
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-eventdestination-syntax.yaml"></a>

```
[CloudWatchDestination](#cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination): [*CloudWatchDestination*](aws-properties-ses-configurationseteventdestination-cloudwatchdestination.md)
[Enabled](#cfn-ses-configurationseteventdestination-eventdestination-enabled): Boolean
[MatchingEventTypes](#cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes): 
  - String
[Name](#cfn-ses-configurationseteventdestination-eventdestination-name): String
[KinesisFirehoseDestination](#cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination): [*KinesisFirehoseDestination*](aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination.md)
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-eventdestination-properties"></a>

`CloudWatchDestination`  <a name="cfn-ses-configurationseteventdestination-eventdestination-cloudwatchdestination"></a>
The names, default values, and sources of the dimensions associated with an CloudWatch event destination\.  
 *Required*: No  
 *Type*: [Amazon SES ConfigurationSetEventDestination CloudWatchDestination](aws-properties-ses-configurationseteventdestination-cloudwatchdestination.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Enabled`  <a name="cfn-ses-configurationseteventdestination-eventdestination-enabled"></a>
Sets whether Amazon SES publishes events to this destination when you send an email with the associated configuration set\. Set to `true` to enable publishing to this destination; set to `false` to prevent publishing to this destination\. The default value is `false`\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KinesisFirehoseDestination`  <a name="cfn-ses-configurationseteventdestination-eventdestination-kinesisfirehosedestination"></a>
Contains the delivery stream ARN and the IAM role ARN associated with an Kinesis Firehose event destination\.  
 *Required*: No  
 *Type*: [Amazon SES ConfigurationSetEventDestination KinesisFirehoseDestination](aws-properties-ses-configurationseteventdestination-kinesisfirehosedestination.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MatchingEventTypes`  <a name="cfn-ses-configurationseteventdestination-eventdestination-matchingeventtypes"></a>
The type of email sending events to publish to the event destination\.  
For a list of valid values, see [EventDestination](http://docs.aws.amazon.com/ses/latest/APIReference/API_EventDestination.html) in the *Amazon Simple Email Service API Reference*\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ses-configurationseteventdestination-eventdestination-name"></a>
The name of the event destination\. The name can:  
+ Contain ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain up to 64 characters\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-configurationseteventdestination-eventdestination-seealso"></a>
+ [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*
+ [EventDestination](http://docs.aws.amazon.com/ses/latest/APIReference/API_EventDestination.html) in the *Amazon Simple Email Service API Reference*
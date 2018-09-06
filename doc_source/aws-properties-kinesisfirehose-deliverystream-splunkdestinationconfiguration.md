# Amazon Kinesis Data Firehose DeliveryStream SplunkDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration"></a>

<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-description"></a>The `SplunkDestinationConfiguration` property type specifies the configuration of a destination in Splunk for a Kinesis Data Firehose delivery stream\.

<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-inheritance"></a> `SplunkDestinationConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="zzz-syntax.json"></a>

```
{
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-cloudwatchloggingoptions)" : [*CloudWatchLoggingOptions*](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md),
  "[HECAcknowledgmentTimeoutInSeconds](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecacknowledgmenttimeoutinseconds)" : Integer,
  "[HECEndpoint](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpoint)" : String,
  "[HECEndpointType](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpointtype)" : String,
  "[HECToken](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hectoken)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-processingconfiguration)" : [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md),
  "[RetryOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-retryoptions)" : [*RetryOptions*](aws-properties-kinesisfirehose-deliverystream-splunkretryoptions.md),
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3backupmode)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3configuration)" : [*S3Configuration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-syntax.yaml"></a>

```
[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-cloudwatchloggingoptions):
  [*CloudWatchLoggingOptions*](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)
[HECAcknowledgmentTimeoutInSeconds](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecacknowledgmenttimeoutinseconds): Integer
[HECEndpoint](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpoint): String
[HECEndpointType](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpointtype): String
[HECToken](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hectoken): String
[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-processingconfiguration):
  [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)
[RetryOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-retryoptions):
  [*RetryOptions*](aws-properties-kinesisfirehose-deliverystream-splunkretryoptions.md)
[S3BackupMode](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3backupmode): String
[S3Configuration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3configuration):
  [*S3Configuration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-properties"></a>

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-cloudwatchloggingoptions"></a>
The CloudWatch logging options for your delivery stream\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`HECAcknowledgmentTimeoutInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecacknowledgmenttimeoutinseconds"></a>
The amount of time that Kinesis Data Firehose waits to receive an acknowledgment from Splunk after it sends it data\. At the end of the timeout period, Kinesis Data Firehose either tries to send the data again or considers it an error, based on your retry settings\.  
Valid Range: Minimum value of 180\. Maximum value of 600\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`HECEndpoint`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpoint"></a>
The HTTP Event Collector \(HEC\) endpoint to which Kinesis Data Firehose sends your data\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`HECEndpointType`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpointtype"></a>
This type can be either `Raw` or `Event`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`HECToken`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hectoken"></a>
A GUID that you obtain from your Splunk cluster when you create a new HEC endpoint\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-processingconfiguration"></a>
The data processing configuration\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RetryOptions`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-retryoptions"></a>
The retry behavior in case Kinesis Data Firehose is unable to deliver data to Splunk, or if it doesn't receive an acknowledgment of receipt from Splunk\.  
 *Required*: No  
 *Type*: [Kinesis Data Firehose DeliveryStream SplunkRetryOptions](aws-properties-kinesisfirehose-deliverystream-splunkretryoptions.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3backupmode"></a>
Defines how documents should be delivered to Amazon S3\. When set to `FailedEventsOnly`, Kinesis Data Firehose writes any data that could not be indexed to the configured Amazon S3 destination\. When set to `AllEvents`, Kinesis Data Firehose delivers all incoming records to Amazon S3, and also writes failed documents to Amazon S3\. Default value is `FailedEventsOnly`\.  
Valid values include `FailedEventsOnly` and `AllEvents`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3configuration"></a>
The configuration for the backup Amazon S3 location\.  
 *Required*: Yes  
 *Type*: [Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-seealso"></a>
+ [SplunkDestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_SplunkDestinationConfiguration.html) in the *Amazon Kinesis Data Firehose API Reference*
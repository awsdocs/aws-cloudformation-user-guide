# AWS::KinesisFirehose::DeliveryStream SplunkDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration"></a>

The `SplunkDestinationConfiguration` property type specifies the configuration of a destination in Splunk for a Kinesis Data Firehose delivery stream\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-syntax.json"></a>

```
{
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-cloudwatchloggingoptions)" : CloudWatchLoggingOptions,
  "[HECAcknowledgmentTimeoutInSeconds](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecacknowledgmenttimeoutinseconds)" : Integer,
  "[HECEndpoint](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpoint)" : String,
  "[HECEndpointType](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpointtype)" : String,
  "[HECToken](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hectoken)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-processingconfiguration)" : ProcessingConfiguration,
  "[RetryOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-retryoptions)" : SplunkRetryOptions,
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3backupmode)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3configuration)" : S3DestinationConfiguration
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-syntax.yaml"></a>

```
  [CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-cloudwatchloggingoptions): 
    CloudWatchLoggingOptions
  [HECAcknowledgmentTimeoutInSeconds](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecacknowledgmenttimeoutinseconds): Integer
  [HECEndpoint](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpoint): String
  [HECEndpointType](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpointtype): String
  [HECToken](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hectoken): String
  [ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-processingconfiguration): 
    ProcessingConfiguration
  [RetryOptions](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-retryoptions): 
    SplunkRetryOptions
  [S3BackupMode](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3backupmode): String
  [S3Configuration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3configuration): 
    S3DestinationConfiguration
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration-properties"></a>

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-cloudwatchloggingoptions"></a>
The Amazon CloudWatch logging options for your delivery stream\.  
*Required*: No  
*Type*: [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HECAcknowledgmentTimeoutInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecacknowledgmenttimeoutinseconds"></a>
The amount of time that Kinesis Data Firehose waits to receive an acknowledgment from Splunk after it sends it data\. At the end of the timeout period, Kinesis Data Firehose either tries to send the data again or considers it an error, based on your retry settings\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `180`  
*Maximum*: `600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HECEndpoint`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpoint"></a>
The HTTP Event Collector \(HEC\) endpoint to which Kinesis Data Firehose sends your data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HECEndpointType`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hecendpointtype"></a>
This type can be either `Raw` or `Event`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Event | Raw`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HECToken`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-hectoken"></a>
This is a GUID that you obtain from your Splunk cluster when you create a new HEC endpoint\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-processingconfiguration"></a>
The data processing configuration\.  
*Required*: No  
*Type*: [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryOptions`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-retryoptions"></a>
The retry behavior in case Kinesis Data Firehose is unable to deliver data to Splunk, or if it doesn't receive an acknowledgment of receipt from Splunk\.  
*Required*: No  
*Type*: [SplunkRetryOptions](aws-properties-kinesisfirehose-deliverystream-splunkretryoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3backupmode"></a>
Defines how documents should be delivered to Amazon S3\. When set to `FailedEventsOnly`, Kinesis Data Firehose writes any data that could not be indexed to the configured Amazon S3 destination\. When set to `AllEvents`, Kinesis Data Firehose delivers all incoming records to Amazon S3, and also writes failed documents to Amazon S3\. The default value is `FailedEventsOnly`\.  
You can update this backup mode from `FailedEventsOnly` to `AllEvents`\. You can't update it from `AllEvents` to `FailedEventsOnly`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AllEvents | FailedEventsOnly`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration-s3configuration"></a>
The configuration for the backup Amazon S3 location\.  
*Required*: Yes  
*Type*: [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration--seealso"></a>
+  [SplunkDestinationConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_SplunkDestinationConfiguration.html) in the *Amazon Kinesis Data Firehose API Reference *\. 


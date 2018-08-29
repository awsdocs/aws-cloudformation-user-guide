# Amazon Kinesis Firehose DeliveryStream CloudWatchLoggingOptions<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions"></a>

The `CloudWatchLoggingOptions` property type specifies Amazon CloudWatch Logs \(CloudWatch Logs\) logging options that Amazon Kinesis Firehose \(Kinesis Firehose\) uses for the delivery stream\.

`CloudWatchLoggingOptions` is a property of the [Amazon Kinesis Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md), [Amazon Kinesis Firehose DeliveryStream ExtendedS3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.md), [Amazon Kinesis Firehose DeliveryStream RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md), [Amazon Kinesis Data Firehose DeliveryStream SplunkDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration.md), and [Amazon Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md) property types\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-enabled)" : Boolean,
  "[LogGroupName](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-loggroupname)" : String,
  "[LogStreamName](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-logstreamname)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-syntax.yaml"></a>

```
[Enabled](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-enabled): Boolean
[LogGroupName](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-loggroupname): String
[LogStreamName](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-logstreamname): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-properties"></a>

`Enabled`  <a name="cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-enabled"></a>
Indicates whether CloudWatch Logs logging is enabled\.  
*Required*: No  
*Type*: Boolean

`LogGroupName`  <a name="cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-loggroupname"></a>
The name of the CloudWatch Logs log group that contains the log stream that Kinesis Firehose will use\.  
*Required*: Conditional\. If you enable logging, you must specify this property\.  
*Type*: String

`LogStreamName`  <a name="cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-logstreamname"></a>
The name of the CloudWatch Logs log stream that Kinesis Firehose uses to send logs about data delivery\.  
*Required*: Conditional\. If you enable logging, you must specify this property\.  
*Type*: String
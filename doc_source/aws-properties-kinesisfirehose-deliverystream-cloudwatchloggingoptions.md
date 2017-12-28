# Amazon Kinesis Firehose DeliveryStream CloudWatchLoggingOptions<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions"></a>

The `CloudWatchLoggingOptions` property type specifies Amazon CloudWatch Logs \(CloudWatch Logs\) logging options that Amazon Kinesis Firehose \(Kinesis Firehose\) uses for the delivery stream\.

`CloudWatchLoggingOptions` is a property of the [Amazon Kinesis Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md), [Amazon Kinesis Firehose DeliveryStream ExtendedS3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.md), [Amazon Kinesis Firehose DeliveryStream RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md), and [Amazon Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md) property types\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-enabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-loggroupname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-logstreamname)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-enabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-loggroupname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-cloudwatchloggingoptions-logstreamname): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions-properties"></a>

`Enabled`  
Indicates whether CloudWatch Logs logging is enabled\.  
*Required: *No  
*Type*: Boolean

`LogGroupName`  
The name of the CloudWatch Logs log group that contains the log stream that Kinesis Firehose will use\.  
*Required: *Conditional\. If you enable logging, you must specify this property\.  
*Type*: String

`LogStreamName`  
The name of the CloudWatch Logs log stream that Kinesis Firehose uses to send logs about data delivery\.  
*Required: *Conditional\. If you enable logging, you must specify this property\.  
*Type*: String
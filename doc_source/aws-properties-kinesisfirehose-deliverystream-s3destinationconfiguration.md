# Amazon Kinesis Data Firehose DeliveryStream S3DestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration"></a>

The `S3DestinationConfiguration` property type specifies an Amazon Simple Storage Service \(Amazon S3\) destination to which Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) delivers data\.

`S3DestinationConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource and the [Amazon Kinesis Data Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md), [Amazon Kinesis Data Firehose DeliveryStream RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md), and [Amazon Kinesis Data Firehose DeliveryStream SplunkDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration.md) property types\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-syntax.json"></a>

```
{
  "[BucketARN](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bucketarn)" : String,
  "[BufferingHints](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bufferinghints)" : [`BufferingHints`](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md),
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-cloudwatchloggingoptions)" : [`CloudWatchLoggingOptions`](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md),
  "[CompressionFormat](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-compressionformat)" : String,
  "[EncryptionConfiguration](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-encryptionconfiguration)" : [`EncryptionConfiguration`](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md),
  "[Prefix](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-prefix)" : String,
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-syntax.yaml"></a>

```
[BucketARN](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bucketarn): String
[BufferingHints](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bufferinghints):
  [`BufferingHints`](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)
[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-cloudwatchloggingoptions):
  [`CloudWatchLoggingOptions`](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)
[CompressionFormat](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-compressionformat): String
[EncryptionConfiguration](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-encryptionconfiguration):
  [`EncryptionConfiguration`](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md)
[Prefix](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-prefix): String
[RoleARN](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-rolearn): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-properties"></a>

`BucketARN`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bucketarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket to send data to\.  
*Required*: Yes  
*Type*: String

`BufferingHints`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bufferinghints"></a>
Configures how Kinesis Data Firehose buffers incoming data while delivering it to the Amazon S3 bucket\.  
*Required*: Yes  
*Type*: [BufferingHints](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-cloudwatchloggingoptions"></a>
The Amazon CloudWatch Logs logging options for the delivery stream\.  
*Required*: No  
*Type*: [Amazon Kinesis Data Firehose DeliveryStream CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)

`CompressionFormat`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-compressionformat"></a>
The type of compression that Kinesis Data Firehose uses to compress the data that it delivers to the Amazon S3 bucket\. For valid values, see the `CompressionFormat` content for the [S3DestinationConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_S3DestinationConfiguration.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.  
*Required*: Yes  
*Type*: String

`EncryptionConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-encryptionconfiguration"></a>
Configures Amazon Simple Storage Service \(Amazon S3\) server\-side encryption\. Kinesis Data Firehose uses AWS Key Management Service \(AWS KMS\) to encrypt the data that it delivers to your Amazon S3 bucket\.  
*Required*: No  
*Type*: [Amazon Kinesis Data Firehose DeliveryStream EncryptionConfiguration](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md)

`Prefix`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-prefix"></a>
A prefix that Kinesis Data Firehose adds to the files that it delivers to the Amazon S3 bucket\. The prefix helps you identify the files that Kinesis Data Firehose delivered\.  
*Required: *No  
*Type*: String

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-rolearn"></a>
The ARN of an AWS Identity and Access Management \(IAM\) role that grants Kinesis Data Firehose access to your Amazon S3 bucket and AWS KMS \(if you enable data encryption\)\.  
For more information, see [Grant Kinesis Data Firehose Access to an Amazon S3 Destination](https://docs.aws.amazon.com/firehose/latest/dev/controlling-access.html#using-iam-s3) in the *Amazon Kinesis Data Firehose Developer Guide*\.  
*Required*: Yes  
*Type*: String
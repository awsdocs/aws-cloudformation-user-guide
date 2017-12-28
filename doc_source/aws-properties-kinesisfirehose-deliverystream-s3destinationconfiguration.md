# Amazon Kinesis Firehose DeliveryStream S3DestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration"></a>

The `S3DestinationConfiguration` property type specifies an Amazon Simple Storage Service \(Amazon S3\) destination to which Amazon Kinesis Firehose \(Kinesis Firehose\) delivers data\.

`S3DestinationConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource and the [Amazon Kinesis Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md) and [Amazon Kinesis Firehose DeliveryStream RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md) property types\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bucketarn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bufferinghints)" : BufferingHints,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-cloudwatchloggingoptions)" : CloudWatchLoggingOptions,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-compressionformat)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-encryptionconfiguration)" : EncryptionConfiguration,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-prefix)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bucketarn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-bufferinghints):
  BufferingHints
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-cloudwatchloggingoptions):
  CloudWatchLoggingOptions
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-compressionformat): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-encryptionconfiguration):
  EncryptionConfiguration
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-prefix): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration-rolearn): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration-properties"></a>

`BucketARN`  
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket to send data to\.  
*Required: *Yes  
*Type*: String

`BufferingHints`  
Configures how Kinesis Firehose buffers incoming data while delivering it to the Amazon S3 bucket\.  
*Required: *Yes  
*Type*: [Kinesis Firehose DeliveryStream BufferingHints](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)

`CloudWatchLoggingOptions`  
The Amazon CloudWatch Logs logging options for the delivery stream\.  
*Required: *No  
*Type*: [Amazon Kinesis Firehose DeliveryStream CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)

`CompressionFormat`  
The type of compression that Kinesis Firehose uses to compress the data that it delivers to the Amazon S3 bucket\. For valid values, see the `CompressionFormat` content for the [S3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_S3DestinationConfiguration.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required: *Yes  
*Type*: String

`EncryptionConfiguration`  
Configures Amazon Simple Storage Service \(Amazon S3\) server\-side encryption\. Kinesis Firehose uses AWS Key Management Service \(AWS KMS\) to encrypt the data that it delivers to your Amazon S3 bucket\.  
*Required: *No  
*Type*: [Amazon Kinesis Firehose DeliveryStream EncryptionConfiguration](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md)

`Prefix`  
A prefix that Kinesis Firehose adds to the files that it delivers to the Amazon S3 bucket\. The prefix helps you identify the files that Kinesis Firehose delivered\.  
*Required: *No  
*Type*: String

`RoleARN`  
The ARN of an AWS Identity and Access Management \(IAM\) role that grants Kinesis Firehose access to your Amazon S3 bucket and AWS KMS \(if you enable data encryption\)\.  
For more information, see [Grant Kinesis Firehose Access to an Amazon S3 Destination](http://docs.aws.amazon.com/firehose/latest/dev/controlling-access.html#using-iam-s3) in the *Amazon Kinesis Firehose Developer Guide*\.  
*Required: *Yes  
*Type*: String
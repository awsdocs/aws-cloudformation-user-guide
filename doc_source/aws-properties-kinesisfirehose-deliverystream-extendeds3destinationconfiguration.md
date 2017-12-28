# Amazon Kinesis Firehose DeliveryStream ExtendedS3DestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration"></a>

The `ExtendedS3DestinationConfiguration` property type configures an Amazon S3 destination for an Amazon Kinesis Firehose delivery stream\. `ExtendedS3DestinationConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints)" : BufferingHints,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions)" : CloudWatchLoggingOptions,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration)" : EncryptionConfiguration,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration)" : ProcessingConfiguration,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration)" : S3DestinationConfiguration,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints):
    BufferingHints
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions): 
    CloudWatchLoggingOptions
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration): 
    EncryptionConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration): 
    ProcessingConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration): 
    S3DestinationConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-properties"></a>

`BucketARN`  
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket\. For constraints, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: No interruption 

`BufferingHints`  
The buffering option\.  
 *Required*: Yes  
 *Type*: [Kinesis Firehose DeliveryStream BufferingHints](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)  
 *Update requires*: No interruption 

`CloudWatchLoggingOptions`  
The CloudWatch logging options for the Kinesis Firehose delivery stream\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
 *Update requires*: No interruption 

`CompressionFormat`  
The compression format for the Kinesis Firehose delivery stream\. The default value is `UNCOMPRESSED`\. For valid values, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: No interruption 

`EncryptionConfiguration`  
The encryption configuration for the Kinesis Firehose delivery stream\. The default value is `NoEncryption`\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream EncryptionConfiguration](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md)  
 *Update requires*: No interruption 

`Prefix`  
The `YYYY/MM/DD/HH` time format prefix is automatically used for delivered Amazon S3 files\. For more information, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: No interruption 

`ProcessingConfiguration`  
The data processing configuration for the Kinesis Firehose delivery stream\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
 *Update requires*: No interruption 

`RoleARN`  
The ARN of the AWS credentials\. For constraints, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: No interruption 

`S3BackupConfiguration`  
The configuration for backup in Amazon S3\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
 *Update requires*: No interruption 

`S3BackupMode`  
The Amazon S3 backup mode\. For valid values, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: No  
*Type*: String  
 *Update requires*: No interruption 
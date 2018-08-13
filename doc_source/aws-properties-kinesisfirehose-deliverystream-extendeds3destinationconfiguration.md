# Amazon Kinesis Firehose DeliveryStream ExtendedS3DestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration"></a>

The `ExtendedS3DestinationConfiguration` property type configures an Amazon S3 destination for an Amazon Kinesis Firehose delivery stream\. `ExtendedS3DestinationConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax.json"></a>

```
{
  "[BucketARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn)" : String,
  "[BufferingHints](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints)" : [*BufferingHints*](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md),
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions)" : [*CloudWatchLoggingOptions*](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md),
  "[CompressionFormat](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat)" : String,
  "[EncryptionConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration)" : [*EncryptionConfiguration*](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md),
  "[Prefix](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration)" : [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md),
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn)" : String,
  "[S3BackupConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration)" : [*S3DestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md),
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax.yaml"></a>

```
  [BucketARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn): String
  [BufferingHints](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints):
    [*BufferingHints*](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)
  [CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions): 
    [*CloudWatchLoggingOptions*](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)
  [CompressionFormat](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat): String
  [EncryptionConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration): 
    [*EncryptionConfiguration*](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md)
  [Prefix](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix): String
  [ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration): 
    [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)
  [RoleARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn): String
  [S3BackupConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration): 
    [*S3DestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)
  [S3BackupMode](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-properties"></a>

`BucketARN`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket\. For constraints, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`BufferingHints`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints"></a>
The buffering option\.  
 *Required*: Yes  
 *Type*: [Kinesis Firehose DeliveryStream BufferingHints](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions"></a>
The CloudWatch logging options for the Kinesis Firehose delivery stream\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CompressionFormat`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat"></a>
The compression format for the Kinesis Firehose delivery stream\. The default value is `UNCOMPRESSED`\. For valid values, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`EncryptionConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration"></a>
The encryption configuration for the Kinesis Firehose delivery stream\. The default value is `NoEncryption`\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream EncryptionConfiguration](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Prefix`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix"></a>
The `YYYY/MM/DD/HH` time format prefix is automatically used for delivered Amazon S3 files\. For more information, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration"></a>
The data processing configuration for the Kinesis Firehose delivery stream\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn"></a>
The ARN of the AWS credentials\. For constraints, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3BackupConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration"></a>
The configuration for backup in Amazon S3\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode"></a>
The Amazon S3 backup mode\. For valid values, see [ExtendedS3DestinationConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Firehose API Reference*\.  
 *Required*: No  
*Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
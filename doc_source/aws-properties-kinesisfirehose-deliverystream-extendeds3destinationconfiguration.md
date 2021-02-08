# AWS::KinesisFirehose::DeliveryStream ExtendedS3DestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration"></a>

The `ExtendedS3DestinationConfiguration` property type configures an Amazon S3 destination for an Amazon Kinesis Data Firehose delivery stream\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax.json"></a>

```
{
  "[BucketARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn)" : String,
  "[BufferingHints](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints)" : BufferingHints,
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions)" : CloudWatchLoggingOptions,
  "[CompressionFormat](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat)" : String,
  "[DataFormatConversionConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-dataformatconversionconfiguration)" : DataFormatConversionConfiguration,
  "[EncryptionConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration)" : EncryptionConfiguration,
  "[ErrorOutputPrefix](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-erroroutputprefix)" : String,
  "[Prefix](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration)" : ProcessingConfiguration,
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn)" : String,
  "[S3BackupConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration)" : S3DestinationConfiguration,
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-syntax.yaml"></a>

```
  [BucketARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn): String
  [BufferingHints](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints): 
    BufferingHints
  [CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions): 
    CloudWatchLoggingOptions
  [CompressionFormat](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat): String
  [DataFormatConversionConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-dataformatconversionconfiguration): 
    DataFormatConversionConfiguration
  [EncryptionConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration): 
    EncryptionConfiguration
  [ErrorOutputPrefix](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-erroroutputprefix): String
  [Prefix](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix): String
  [ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration): 
    ProcessingConfiguration
  [RoleARN](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn): String
  [S3BackupConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration): 
    S3DestinationConfiguration
  [S3BackupMode](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-properties"></a>

`BucketARN`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bucketarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket\. For constraints, see [ExtendedS3DestinationConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BufferingHints`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-bufferinghints"></a>
The buffering option\.  
*Required*: No  
*Type*: [BufferingHints](aws-properties-kinesisfirehose-deliverystream-bufferinghints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-cloudwatchloggingoptions"></a>
The Amazon CloudWatch logging options for your delivery stream\.  
*Required*: No  
*Type*: [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CompressionFormat`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-compressionformat"></a>
The compression format\. If no value is specified, the default is `UNCOMPRESSED`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GZIP | HADOOP_SNAPPY | Snappy | UNCOMPRESSED | ZIP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataFormatConversionConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-dataformatconversionconfiguration"></a>
The serializer, deserializer, and schema for converting data from the JSON format to the Parquet or ORC format before writing it to Amazon S3\.  
*Required*: No  
*Type*: [DataFormatConversionConfiguration](aws-properties-kinesisfirehose-deliverystream-dataformatconversionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-encryptionconfiguration"></a>
The encryption configuration for the Kinesis Data Firehose delivery stream\. The default value is `NoEncryption`\.   
*Required*: No  
*Type*: [EncryptionConfiguration](aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorOutputPrefix`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-erroroutputprefix"></a>
A prefix that Kinesis Data Firehose evaluates and adds to failed records before writing them to S3\. This prefix appears immediately following the bucket name\. For information about how to specify this prefix, see [Custom Prefixes for Amazon S3 Objects](https://docs.aws.amazon.com/firehose/latest/dev/s3-prefixes.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-prefix"></a>
The `YYYY/MM/DD/HH` time format prefix is automatically used for delivered Amazon S3 files\. For more information, see [ExtendedS3DestinationConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-processingconfiguration"></a>
The data processing configuration for the Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-rolearn"></a>
The Amazon Resource Name \(ARN\) of the AWS credentials\. For constraints, see [ExtendedS3DestinationConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_ExtendedS3DestinationConfiguration.html) in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BackupConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupconfiguration"></a>
The configuration for backup in Amazon S3\.  
*Required*: No  
*Type*: [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration-s3backupmode"></a>
The Amazon S3 backup mode\. After you create a delivery stream, you can update it to enable Amazon S3 backup if it is disabled\. If backup is enabled, you can't update the delivery stream to disable it\.   
*Required*: No  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
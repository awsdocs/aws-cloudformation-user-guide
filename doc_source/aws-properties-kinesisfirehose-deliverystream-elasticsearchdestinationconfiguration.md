# Amazon Kinesis Data Firehose DeliveryStream ElasticsearchDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration"></a>

The `ElasticsearchDestinationConfiguration` property type specifies an Amazon Elasticsearch Service \(Amazon ES\) domain that Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) delivers data to\.

`ElasticsearchDestinationConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-syntax.json"></a>

```
{
  "[BufferingHints](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-bufferinghints)" : [*BufferingHints*](aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints.md),
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-cloudwatchloggingoptions)" : [*CloudWatchLoggingOptions*](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md),
  "[DomainARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-domainarn)" : String,
  "[IndexName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexname)" : String,
  "[IndexRotationPeriod](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexrotationperiod)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-processingconfiguration)" : [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md),
  "[RetryOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-retryoptions)" : [*RetryOptions*](aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions.md),
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-rolearn)" : String,
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3backupmodee)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3configuration)" : [*S3Configuration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md),
  "[TypeName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-typename)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-syntax.yaml"></a>

```
[BufferingHints](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-bufferinghints):
  [*BufferingHints*](aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints.md)
[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-cloudwatchloggingoptions):
  [*CloudWatchLoggingOptions*](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)
[DomainARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-domainarn): String
[IndexName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexname): String
[IndexRotationPeriod](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexrotationperiod): String
[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-processingconfiguration):
  [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)
[RetryOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-retryoptions):
  [*RetryOptions*](aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions.md)
[RoleARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-rolearn): String
[S3BackupMode](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3backupmodee): String
[S3Configuration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3configuration):
  [*S3Configuration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)
[TypeName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-typename): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-properties"></a>

`BufferingHints`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-bufferinghints"></a>
Configures how Kinesis Data Firehose buffers incoming data while delivering it to the Amazon ES domain\.  
*Required*: Yes  
*Type*: [ElasticsearchBufferingHints](aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints.md)

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-cloudwatchloggingoptions"></a>
The Amazon CloudWatch Logs logging options for the delivery stream\.  
*Required*: No  
*Type*: [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)

`DomainARN`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-domainarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon ES domain that Kinesis Data Firehose delivers data to\.  
*Required*: Yes  
*Type*: String

`IndexName`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexname"></a>
The name of the Elasticsearch index to which Kinesis Data Firehose adds data for indexing\.  
*Required*: Yes  
*Type*: String

`IndexRotationPeriod`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexrotationperiod"></a>
The frequency of Elasticsearch index rotation\. If you enable index rotation, Kinesis Data Firehose appends a portion of the UTC arrival timestamp to the specified index name, and rotates the appended timestamp accordingly\. For more information, see [Index Rotation for the Amazon ES Destination](https://docs.aws.amazon.com/firehose/latest/dev/basic-deliver.html#es-index-rotation) in the *Amazon Kinesis Data Firehose Developer Guide*\.  
*Required*: Yes  
*Type*: String

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-processingconfiguration"></a>
The data processing configuration for the Kinesis Data Firehose delivery stream\.  
 *Required*: No  
 *Type*: [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)

`RetryOptions`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-retryoptions"></a>
The retry behavior when Kinesis Data Firehose is unable to deliver data to Amazon ES\.  
 *Required*: Yes  
*Type*: [ElasticsearchRetryOptions](aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions.md)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to be assumed by Kinesis Data Firehose for calling the Amazon ES Configuration API and for indexing documents\.  
For more information, see [Grant Kinesis Data Firehose Access to an Amazon S3 Destination](https://docs.aws.amazon.com/firehose/latest/dev/controlling-access.html#using-iam-s3) in the Amazon Kinesis Data Firehose Developer Guide and [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the Amazon Web Services General Reference\.  
*Required*: Yes  
*Type*: String

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3backupmodee"></a>
The condition under which Kinesis Data Firehose delivers data to Amazon Simple Storage Service \(Amazon S3\)\. You can send Amazon S3 all documents \(all data\) or only the documents that Kinesis Data Firehose could not deliver to the Amazon ES destination\. For more information and valid values, see the `S3BackupMode` content for the [ElasticsearchDestinationConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_ElasticsearchDestinationConfiguration.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: Yes  
*Type*: String

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3configuration"></a>
The S3 bucket where Kinesis Data Firehose backs up incoming data\.  
 *Required*: Yes  
*Type*: [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)

`TypeName`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-typename"></a>
The Elasticsearch type name that Amazon ES adds to documents when indexing data\.  
*Required*: Yes  
*Type*: String
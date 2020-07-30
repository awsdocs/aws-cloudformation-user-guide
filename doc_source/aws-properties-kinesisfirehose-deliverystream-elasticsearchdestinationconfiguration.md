# AWS::KinesisFirehose::DeliveryStream ElasticsearchDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration"></a>

The `ElasticsearchDestinationConfiguration` property type specifies an Amazon Elasticsearch Service \(Amazon ES\) domain that Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) delivers data to\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-syntax.json"></a>

```
{
  "[BufferingHints](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-bufferinghints)" : ElasticsearchBufferingHints,
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-cloudwatchloggingoptions)" : CloudWatchLoggingOptions,
  "[ClusterEndpoint](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-clusterendpoint)" : String,
  "[DomainARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-domainarn)" : String,
  "[IndexName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexname)" : String,
  "[IndexRotationPeriod](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexrotationperiod)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-processingconfiguration)" : ProcessingConfiguration,
  "[RetryOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-retryoptions)" : ElasticsearchRetryOptions,
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-rolearn)" : String,
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3backupmode)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3configuration)" : S3DestinationConfiguration,
  "[TypeName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-typename)" : String,
  "[VpcConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-vpcconfiguration)" : VpcConfiguration
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-syntax.yaml"></a>

```
  [BufferingHints](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-bufferinghints): 
    ElasticsearchBufferingHints
  [CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-cloudwatchloggingoptions): 
    CloudWatchLoggingOptions
  [ClusterEndpoint](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-clusterendpoint): String
  [DomainARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-domainarn): String
  [IndexName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexname): String
  [IndexRotationPeriod](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexrotationperiod): String
  [ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-processingconfiguration): 
    ProcessingConfiguration
  [RetryOptions](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-retryoptions): 
    ElasticsearchRetryOptions
  [RoleARN](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-rolearn): String
  [S3BackupMode](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3backupmode): String
  [S3Configuration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3configuration): 
    S3DestinationConfiguration
  [TypeName](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-typename): String
  [VpcConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-vpcconfiguration): 
    VpcConfiguration
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-properties"></a>

`BufferingHints`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-bufferinghints"></a>
Configures how Kinesis Data Firehose buffers incoming data while delivering it to the Amazon ES domain\.  
*Required*: No  
*Type*: [ElasticsearchBufferingHints](aws-properties-kinesisfirehose-deliverystream-elasticsearchbufferinghints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-cloudwatchloggingoptions"></a>
The Amazon CloudWatch Logs logging options for the delivery stream\.  
*Required*: No  
*Type*: [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterEndpoint`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-clusterendpoint"></a>
The endpoint to use when communicating with the cluster\. Specify either this `ClusterEndpoint` or the `DomainARN` field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainARN`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-domainarn"></a>
The ARN of the Amazon ES domain\. The IAM role must have permissions for `DescribeElasticsearchDomain`, `DescribeElasticsearchDomains`, and `DescribeElasticsearchDomainConfig` after assuming the role specified in **RoleARN**\.   
Specify either `ClusterEndpoint` or `DomainARN`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexName`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexname"></a>
The name of the Elasticsearch index to which Kinesis Data Firehose adds data for indexing\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `80`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexRotationPeriod`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-indexrotationperiod"></a>
The frequency of Elasticsearch index rotation\. If you enable index rotation, Kinesis Data Firehose appends a portion of the UTC arrival timestamp to the specified index name, and rotates the appended timestamp accordingly\. For more information, see [Index Rotation for the Amazon ES Destination](https://docs.aws.amazon.com/firehose/latest/dev/basic-deliver.html#es-index-rotation) in the *Amazon Kinesis Data Firehose Developer Guide*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `NoRotation | OneDay | OneHour | OneMonth | OneWeek`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-processingconfiguration"></a>
The data processing configuration for the Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryOptions`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-retryoptions"></a>
The retry behavior when Kinesis Data Firehose is unable to deliver data to Amazon ES\.  
*Required*: No  
*Type*: [ElasticsearchRetryOptions](aws-properties-kinesisfirehose-deliverystream-elasticsearchretryoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to be assumed by Kinesis Data Firehose for calling the Amazon ES Configuration API and for indexing documents\. For more information, see [Controlling Access with Amazon Kinesis Data Firehose](https://docs.aws.amazon.com/firehose/latest/dev/controlling-access.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3backupmode"></a>
The condition under which Kinesis Data Firehose delivers data to Amazon Simple Storage Service \(Amazon S3\)\. You can send Amazon S3 all documents \(all data\) or only the documents that Kinesis Data Firehose could not deliver to the Amazon ES destination\. For more information and valid values, see the `S3BackupMode` content for the [ElasticsearchDestinationConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_ElasticsearchDestinationConfiguration.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `AllDocuments | FailedDocumentsOnly`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-s3configuration"></a>
The S3 bucket where Kinesis Data Firehose backs up incoming data\.  
*Required*: Yes  
*Type*: [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeName`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-typename"></a>
The Elasticsearch type name that Amazon ES adds to documents when indexing data\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `100`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration-vpcconfiguration"></a>
The details of the VPC of the Amazon ES destination\.  
*Required*: No  
*Type*: [VpcConfiguration](aws-properties-kinesisfirehose-deliverystream-vpcconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
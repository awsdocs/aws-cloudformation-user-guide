# AWS::KinesisFirehose::DeliveryStream AmazonopensearchserviceDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration"></a>

Describes the configuration of a destination in Amazon OpenSearch Service\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-syntax.json"></a>

```
{
  "[BufferingHints](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-bufferinghints)" : AmazonopensearchserviceBufferingHints,
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-cloudwatchloggingoptions)" : CloudWatchLoggingOptions,
  "[ClusterEndpoint](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-clusterendpoint)" : String,
  "[DomainARN](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-domainarn)" : String,
  "[IndexName](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-indexname)" : String,
  "[IndexRotationPeriod](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-indexrotationperiod)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-processingconfiguration)" : ProcessingConfiguration,
  "[RetryOptions](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-retryoptions)" : AmazonopensearchserviceRetryOptions,
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-rolearn)" : String,
  "[S3BackupMode](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-s3backupmode)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-s3configuration)" : S3DestinationConfiguration,
  "[TypeName](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-typename)" : String,
  "[VpcConfiguration](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-vpcconfiguration)" : VpcConfiguration
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-syntax.yaml"></a>

```
  [BufferingHints](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-bufferinghints): 
    AmazonopensearchserviceBufferingHints
  [CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-cloudwatchloggingoptions): 
    CloudWatchLoggingOptions
  [ClusterEndpoint](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-clusterendpoint): String
  [DomainARN](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-domainarn): String
  [IndexName](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-indexname): String
  [IndexRotationPeriod](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-indexrotationperiod): String
  [ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-processingconfiguration): 
    ProcessingConfiguration
  [RetryOptions](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-retryoptions): 
    AmazonopensearchserviceRetryOptions
  [RoleARN](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-rolearn): String
  [S3BackupMode](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-s3backupmode): String
  [S3Configuration](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-s3configuration): 
    S3DestinationConfiguration
  [TypeName](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-typename): String
  [VpcConfiguration](#cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-vpcconfiguration): 
    VpcConfiguration
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-properties"></a>

`BufferingHints`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-bufferinghints"></a>
The buffering options\. If no value is specified, the default values for AmazonopensearchserviceBufferingHints are used\.  
*Required*: No  
*Type*: [AmazonopensearchserviceBufferingHints](aws-properties-kinesisfirehose-deliverystream-amazonopensearchservicebufferinghints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-cloudwatchloggingoptions"></a>
Describes the Amazon CloudWatch logging options for your delivery stream\.  
*Required*: No  
*Type*: [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterEndpoint`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-clusterendpoint"></a>
The endpoint to use when communicating with the cluster\. Specify either this ClusterEndpoint or the DomainARN field\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `https:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainARN`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-domainarn"></a>
The ARN of the Amazon OpenSearch Service domain\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexName`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-indexname"></a>
The Amazon OpenSearch Service index name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `80`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexRotationPeriod`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-indexrotationperiod"></a>
The Amazon OpenSearch Service index rotation period\. Index rotation appends a timestamp to the IndexName to facilitate the expiration of old data\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NoRotation | OneDay | OneHour | OneMonth | OneWeek`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-processingconfiguration"></a>
Describes a data processing configuration\.  
*Required*: No  
*Type*: [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryOptions`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-retryoptions"></a>
The retry behavior in case Kinesis Data Firehose is unable to deliver documents to Amazon OpenSearch Service\. The default value is 300 \(5 minutes\)\.  
*Required*: No  
*Type*: [AmazonopensearchserviceRetryOptions](aws-properties-kinesisfirehose-deliverystream-amazonopensearchserviceretryoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to be assumed by Kinesis Data Firehose for calling the Amazon OpenSearch Service Configuration API and for indexing documents\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BackupMode`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-s3backupmode"></a>
Defines how documents should be delivered to Amazon S3\.   
*Required*: No  
*Type*: String  
*Allowed values*: `AllDocuments | FailedDocumentsOnly`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-s3configuration"></a>
Describes the configuration of a destination in Amazon S3\.  
*Required*: Yes  
*Type*: [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeName`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-typename"></a>
The Amazon OpenSearch Service type name\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `100`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchservicedestinationconfiguration-vpcconfiguration"></a>
The details of the VPC of the Amazon OpenSearch Service destination\.  
*Required*: No  
*Type*: [VpcConfiguration](aws-properties-kinesisfirehose-deliverystream-vpcconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
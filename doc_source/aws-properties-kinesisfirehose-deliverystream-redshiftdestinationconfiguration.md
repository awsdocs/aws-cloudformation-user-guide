# Amazon Kinesis Firehose DeliveryStream RedshiftDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration"></a>

The `RedshiftDestinationConfiguration` property type specifies an Amazon Redshift cluster to which Amazon Kinesis Firehose \(Kinesis Firehose\) delivers data\.

`RedshiftDestinationConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-syntax.json"></a>

```
{
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-cloudwatchloggingoptions)" : [`CloudWatchLoggingOptions`](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md),
  "[ClusterJDBCURL](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-clusterjdbcurl)" : String,
  "[CopyCommand](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-copycommand)" : [*CopyCommand*](aws-properties-kinesisfirehose-deliverystream-copycommand.md),
  "[Password](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-password)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-processingconfiguration)" : [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md),
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-rolearn)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-s3configuration)" : [*S3Configuration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md),
  "[Username](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-username)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-syntax.yaml"></a>

```
[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-cloudwatchloggingoptions):
  [*CloudWatchLoggingOptions*](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)
[ClusterJDBCURL](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-clusterjdbcurl): String
[CopyCommand](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-copycommand):
  [*CopyCommand*](aws-properties-kinesisfirehose-deliverystream-copycommand.md)
[Password](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-password): String
[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-processingconfiguration): 
  [*ProcessingConfiguration*](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)
[RoleARN](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-rolearn): String
[S3Configuration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-s3configuration):
  [*S3Configuration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)
[Username](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-username): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-properties"></a>

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-cloudwatchloggingoptions"></a>
The Amazon CloudWatch Logs logging options for the delivery stream\.  
*Required*: No  
*Type*: [Kinesis Firehose DeliveryStream CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)

`ClusterJDBCURL`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-clusterjdbcurl"></a>
The connection string that Kinesis Firehose uses to connect to the Amazon Redshift cluster\.  
*Required*: Yes  
*Type*: String

`CopyCommand`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-copycommand"></a>
Configures the Amazon Redshift `COPY` command that Kinesis Firehose uses to load data into the cluster from the Amazon S3 bucket\.  
*Required*: Yes  
*Type*: [Kinesis Firehose DeliveryStream CopyCommand](aws-properties-kinesisfirehose-deliverystream-copycommand.md)

`Password`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-password"></a>
The password for the Amazon Redshift user that you specified in the `Username` property\.  
*Required*: Yes  
*Type*: String

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-processingconfiguration"></a>
The data processing configuration for the Kinesis Firehose delivery stream\.  
 *Required*: No  
 *Type*: [Kinesis Firehose DeliveryStream ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-rolearn"></a>
The ARN of the AWS Identity and Access Management \(IAM\) role that grants Kinesis Firehose access to your Amazon S3 bucket and AWS KMS \(if you enable data encryption\)\.  
For more information, see [Grant Kinesis Firehose Access to an Amazon Redshift Destination ](http://docs.aws.amazon.com/firehose/latest/dev/controlling-access.html#using-iam-rs) in the *Amazon Kinesis Firehose Developer Guide*\.  
*Required*: Yes  
*Type*: String

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-s3configuration"></a>
The S3 bucket where Kinesis Firehose first delivers data\. After the data is in the bucket, Kinesis Firehose uses the `COPY` command to load the data into the Amazon Redshift cluster\. For the Amazon S3 bucket's compression format, don't specify `SNAPPY` or `ZIP` because the Amazon Redshift `COPY` command doesn't support them\.  
*Required*: Yes  
*Type*: [Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)

`Username`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-username"></a>
The Amazon Redshift user that has permission to access the Amazon Redshift cluster\. This user must have `INSERT` privileges for copying data from the Amazon S3 bucket to the cluster\.  
*Required*: Yes  
*Type*: String
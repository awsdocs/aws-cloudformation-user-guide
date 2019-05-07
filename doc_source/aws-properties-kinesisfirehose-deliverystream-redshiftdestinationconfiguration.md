# AWS::KinesisFirehose::DeliveryStream RedshiftDestinationConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration"></a>

The `RedshiftDestinationConfiguration` property type specifies an Amazon Redshift cluster to which Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) delivers data\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-syntax.json"></a>

```
{
  "[CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-cloudwatchloggingoptions)" : [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md),
  "[ClusterJDBCURL](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-clusterjdbcurl)" : String,
  "[CopyCommand](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-copycommand)" : [CopyCommand](aws-properties-kinesisfirehose-deliverystream-copycommand.md),
  "[Password](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-password)" : String,
  "[ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-processingconfiguration)" : [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md),
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-rolearn)" : String,
  "[S3Configuration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-s3configuration)" : [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md),
  "[Username](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-username)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-syntax.yaml"></a>

```
﻿  [CloudWatchLoggingOptions](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-cloudwatchloggingoptions) : 
    [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)
﻿  [ClusterJDBCURL](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-clusterjdbcurl) : String
﻿  [CopyCommand](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-copycommand) : 
    [CopyCommand](aws-properties-kinesisfirehose-deliverystream-copycommand.md)
﻿  [Password](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-password) : String
﻿  [ProcessingConfiguration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-processingconfiguration) : 
    [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)
﻿  [RoleARN](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-rolearn) : String
﻿  [S3Configuration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-s3configuration) : 
    [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)
﻿  [Username](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-username) : String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-properties"></a>

`CloudWatchLoggingOptions`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-cloudwatchloggingoptions"></a>
The CloudWatch logging options for your delivery stream\.  
*Required*: No  
*Type*: [CloudWatchLoggingOptions](aws-properties-kinesisfirehose-deliverystream-cloudwatchloggingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterJDBCURL`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-clusterjdbcurl"></a>
The connection string that Kinesis Data Firehose uses to connect to the Amazon Redshift cluster\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Pattern*: `jdbc:(redshift|postgresql)://((?!-)[A-Za-z0-9-]{1,63}(?<!-)\.)+redshift\.amazonaws\.com:\d{1,5}/[a-zA-Z0-9_$]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyCommand`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-copycommand"></a>
Configures the Amazon Redshift `COPY` command that Kinesis Data Firehose uses to load data into the cluster from the Amazon S3 bucket\.   
*Required*: Yes  
*Type*: [CopyCommand](aws-properties-kinesisfirehose-deliverystream-copycommand.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-password"></a>
The password for the Amazon Redshift user that you specified in the `Username` property\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `6`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProcessingConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-processingconfiguration"></a>
The data processing configuration for the Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: [ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-rolearn"></a>
The ARN of the AWS Identity and Access Management \(IAM\) role that grants Kinesis Data Firehose access to your Amazon S3 bucket and AWS KMS \(if you enable data encryption\)\. For more information, see [Grant Kinesis Data Firehose Access to an Amazon Redshift Destination](https://docs.aws.amazon.com/firehose/latest/dev/controlling-access.html#using-iam-rs) in the *Amazon Kinesis Data Firehose Developer Guide*\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-s3configuration"></a>
The S3 bucket where Kinesis Data Firehose first delivers data\. After the data is in the bucket, Kinesis Data Firehose uses the `COPY` command to load the data into the Amazon Redshift cluster\. For the Amazon S3 bucket's compression format, don't specify `SNAPPY` or `ZIP` because the Amazon Redshift `COPY` command doesn't support them\.   
*Required*: Yes  
*Type*: [S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration-username"></a>
The Amazon Redshift user that has permission to access the Amazon Redshift cluster\. This user must have `INSERT` privileges for copying data from the Amazon S3 bucket to the cluster\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
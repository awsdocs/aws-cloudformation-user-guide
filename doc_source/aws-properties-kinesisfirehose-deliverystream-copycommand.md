# Amazon Kinesis Firehose DeliveryStream CopyCommand<a name="aws-properties-kinesisfirehose-deliverystream-copycommand"></a>

The `CopyCommand` property type configures the Amazon Redshift `COPY` command that Amazon Kinesis Firehose \(Kinesis Firehose\) uses to load data into an Amazon Redshift cluster from an Amazon S3 bucket\.

`CopyCommand` is a property of the [Amazon Kinesis Firehose DeliveryStream RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md) property type\.

## Syntax<a name="w3ab2c21c14e1478b7"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-copycommand-syntax.json"></a>

```
{
  "[CopyOptions](#cfn-kinesisfirehose-deliverystream-copycommand-copyoptions)" : String,
  "[DataTableColumns](#cfn-kinesisfirehose-deliverystream-copycommand-datatablecolumns)" : String,
  "[DataTableName](#cfn-kinesisfirehose-deliverystream-copycommand-datatablename)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-copycommand-syntax.yaml"></a>

```
[CopyOptions](#cfn-kinesisfirehose-deliverystream-copycommand-copyoptions): String
[DataTableColumns](#cfn-kinesisfirehose-deliverystream-copycommand-datatablecolumns): String
[DataTableName](#cfn-kinesisfirehose-deliverystream-copycommand-datatablename): String
```

## Properties<a name="w3ab2c21c14e1478b9"></a>

`CopyOptions`  <a name="cfn-kinesisfirehose-deliverystream-copycommand-copyoptions"></a>
Parameters to use with the Amazon Redshift `COPY` command\. For examples, see the `CopyOptions` content for the [CopyCommand](http://docs.aws.amazon.com/firehose/latest/APIReference/API_CopyCommand.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required*: No  
*Type*: String

`DataTableColumns`  <a name="cfn-kinesisfirehose-deliverystream-copycommand-datatablecolumns"></a>
A comma\-separated list of the column names in the table that Kinesis Firehose copies data to\.  
*Required*: No  
*Type*: String

`DataTableName`  <a name="cfn-kinesisfirehose-deliverystream-copycommand-datatablename"></a>
The name of the table where Kinesis Firehose adds the copied data\.  
*Required*: Yes  
*Type*: String
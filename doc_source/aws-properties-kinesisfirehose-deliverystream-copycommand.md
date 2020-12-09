# AWS::KinesisFirehose::DeliveryStream CopyCommand<a name="aws-properties-kinesisfirehose-deliverystream-copycommand"></a>

The `CopyCommand` property type configures the Amazon Redshift `COPY` command that Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) uses to load data into an Amazon Redshift cluster from an Amazon S3 bucket\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-copycommand-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-copycommand-properties"></a>

`CopyOptions`  <a name="cfn-kinesisfirehose-deliverystream-copycommand-copyoptions"></a>
Parameters to use with the Amazon Redshift `COPY` command\. For examples, see the `CopyOptions` content for the [CopyCommand](https://docs.aws.amazon.com/firehose/latest/APIReference/API_CopyCommand.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `204800`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataTableColumns`  <a name="cfn-kinesisfirehose-deliverystream-copycommand-datatablecolumns"></a>
A comma\-separated list of column names\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `204800`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataTableName`  <a name="cfn-kinesisfirehose-deliverystream-copycommand-datatablename"></a>
The name of the target table\. The table must already exist in the database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::KinesisFirehose::DeliveryStream SchemaConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-schemaconfiguration"></a>

Specifies the schema to which you want Kinesis Data Firehose to configure your data before it writes it to Amazon S3\. This parameter is required if `Enabled` is set to true\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-schemaconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-schemaconfiguration-syntax.json"></a>

```
{
  "[CatalogId](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-catalogid)" : String,
  "[DatabaseName](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-databasename)" : String,
  "[Region](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-region)" : String,
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-rolearn)" : String,
  "[TableName](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-tablename)" : String,
  "[VersionId](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-versionid)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-schemaconfiguration-syntax.yaml"></a>

```
  [CatalogId](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-catalogid): String
  [DatabaseName](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-databasename): String
  [Region](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-region): String
  [RoleARN](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-rolearn): String
  [TableName](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-tablename): String
  [VersionId](#cfn-kinesisfirehose-deliverystream-schemaconfiguration-versionid): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-schemaconfiguration-properties"></a>

`CatalogId`  <a name="cfn-kinesisfirehose-deliverystream-schemaconfiguration-catalogid"></a>
The ID of the AWS Glue Data Catalog\. If you don't supply this, the AWS account ID is used by default\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^\S+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-kinesisfirehose-deliverystream-schemaconfiguration-databasename"></a>
Specifies the name of the AWS Glue database that contains the schema for the output data\.  
If the `SchemaConfiguration` request parameter is used as part of invoking the `CreateDeliveryStream` API, then the `DatabaseName` property is required and its value must be specified\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^\S+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-kinesisfirehose-deliverystream-schemaconfiguration-region"></a>
If you don't specify an AWS Region, the default is the current Region\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^\S+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-schemaconfiguration-rolearn"></a>
The role that Kinesis Data Firehose can use to access AWS Glue\. This role must be in the same account you use for Kinesis Data Firehose\. Cross\-account roles aren't allowed\.  
If the `SchemaConfiguration` request parameter is used as part of invoking the `CreateDeliveryStream` API, then the `RoleARN` property is required and its value must be specified\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^\S+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-kinesisfirehose-deliverystream-schemaconfiguration-tablename"></a>
Specifies the AWS Glue table that contains the column information that constitutes your data schema\.  
If the `SchemaConfiguration` request parameter is used as part of invoking the `CreateDeliveryStream` API, then the `TableName` property is required and its value must be specified\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^\S+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionId`  <a name="cfn-kinesisfirehose-deliverystream-schemaconfiguration-versionid"></a>
Specifies the table version for the output data schema\. If you don't specify this version ID, or if you set it to `LATEST`, Kinesis Data Firehose uses the most recent version\. This means that any updates to the table are automatically picked up\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^\S+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
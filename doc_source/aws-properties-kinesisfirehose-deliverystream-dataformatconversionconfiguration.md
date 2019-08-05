# AWS::KinesisFirehose::DeliveryStream DataFormatConversionConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-dataformatconversionconfiguration"></a>

Specifies that you want Kinesis Data Firehose to convert data from the JSON format to the Parquet or ORC format before writing it to Amazon S3\. Kinesis Data Firehose uses the serializer and deserializer that you specify, in addition to the column information from the AWS Glue table, to deserialize your input data from JSON and then serialize it to the Parquet or ORC format\. For more information, see [Kinesis Data Firehose Record Format Conversion](https://docs.aws.amazon.com/firehose/latest/dev/record-format-conversion.html)\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-dataformatconversionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-dataformatconversionconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-enabled)" : Boolean,
  "[InputFormatConfiguration](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-inputformatconfiguration)" : [InputFormatConfiguration](aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration.md),
  "[OutputFormatConfiguration](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-outputformatconfiguration)" : [OutputFormatConfiguration](aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration.md),
  "[SchemaConfiguration](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-schemaconfiguration)" : [SchemaConfiguration](aws-properties-kinesisfirehose-deliverystream-schemaconfiguration.md)
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-dataformatconversionconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-enabled): Boolean
  [InputFormatConfiguration](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-inputformatconfiguration):
    [InputFormatConfiguration](aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration.md)
  [OutputFormatConfiguration](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-outputformatconfiguration):
    [OutputFormatConfiguration](aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration.md)
  [SchemaConfiguration](#cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-schemaconfiguration):
    [SchemaConfiguration](aws-properties-kinesisfirehose-deliverystream-schemaconfiguration.md)
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-dataformatconversionconfiguration-properties"></a>

`Enabled`  <a name="cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-enabled"></a>
Defaults to `true`\. Set it to `false` if you want to disable format conversion while preserving the configuration details\.
*Required*: Yes
*Type*: Boolean
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputFormatConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-inputformatconfiguration"></a>
Specifies the deserializer that you want Kinesis Data Firehose to use to convert the format of your data from JSON\.
*Required*: Yes
*Type*: [InputFormatConfiguration](aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputFormatConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-outputformatconfiguration"></a>
Specifies the serializer that you want Kinesis Data Firehose to use to convert the format of your data to the Parquet or ORC format\.
*Required*: Yes
*Type*: [OutputFormatConfiguration](aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-dataformatconversionconfiguration-schemaconfiguration"></a>
Specifies the AWS Glue Data Catalog table that contains the column information\.
*Required*: Yes
*Type*: [SchemaConfiguration](aws-properties-kinesisfirehose-deliverystream-schemaconfiguration.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

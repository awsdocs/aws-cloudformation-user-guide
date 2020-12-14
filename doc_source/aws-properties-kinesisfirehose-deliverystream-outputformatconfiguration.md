# AWS::KinesisFirehose::DeliveryStream OutputFormatConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration"></a>

Specifies the serializer that you want Kinesis Data Firehose to use to convert the format of your data before it writes it to Amazon S3\. This parameter is required if `Enabled` is set to true\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration-syntax.json"></a>

```
{
  "[Serializer](#cfn-kinesisfirehose-deliverystream-outputformatconfiguration-serializer)" : Serializer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration-syntax.yaml"></a>

```
  [Serializer](#cfn-kinesisfirehose-deliverystream-outputformatconfiguration-serializer): 
    Serializer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-outputformatconfiguration-properties"></a>

`Serializer`  <a name="cfn-kinesisfirehose-deliverystream-outputformatconfiguration-serializer"></a>
Specifies which serializer to use\. You can choose either the ORC SerDe or the Parquet SerDe\. If both are non\-null, the server rejects the request\.  
*Required*: No  
*Type*: [Serializer](aws-properties-kinesisfirehose-deliverystream-serializer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
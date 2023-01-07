# AWS::KinesisFirehose::DeliveryStream Serializer<a name="aws-properties-kinesisfirehose-deliverystream-serializer"></a>

The serializer that you want Kinesis Data Firehose to use to convert data to the target format before writing it to Amazon S3\. Kinesis Data Firehose supports two types of serializers: the [ORC SerDe](https://hive.apache.org/javadocs/r1.2.2/api/org/apache/hadoop/hive/ql/io/orc/OrcSerde.html) and the [Parquet SerDe](https://hive.apache.org/javadocs/r1.2.2/api/org/apache/hadoop/hive/ql/io/parquet/serde/ParquetHiveSerDe.html)\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-serializer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-serializer-syntax.json"></a>

```
{
  "[OrcSerDe](#cfn-kinesisfirehose-deliverystream-serializer-orcserde)" : OrcSerDe,
  "[ParquetSerDe](#cfn-kinesisfirehose-deliverystream-serializer-parquetserde)" : ParquetSerDe
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-serializer-syntax.yaml"></a>

```
  [OrcSerDe](#cfn-kinesisfirehose-deliverystream-serializer-orcserde): 
    OrcSerDe
  [ParquetSerDe](#cfn-kinesisfirehose-deliverystream-serializer-parquetserde): 
    ParquetSerDe
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-serializer-properties"></a>

`OrcSerDe`  <a name="cfn-kinesisfirehose-deliverystream-serializer-orcserde"></a>
A serializer to use for converting data to the ORC format before storing it in Amazon S3\. For more information, see [Apache ORC](https://orc.apache.org/docs/)\.  
*Required*: No  
*Type*: [OrcSerDe](aws-properties-kinesisfirehose-deliverystream-orcserde.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParquetSerDe`  <a name="cfn-kinesisfirehose-deliverystream-serializer-parquetserde"></a>
A serializer to use for converting data to the Parquet format before storing it in Amazon S3\. For more information, see [Apache Parquet](https://parquet.apache.org/documentation/latest/)\.  
*Required*: No  
*Type*: [ParquetSerDe](aws-properties-kinesisfirehose-deliverystream-parquetserde.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
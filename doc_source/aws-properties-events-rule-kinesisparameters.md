# Amazon CloudWatch Events Rule KinesisParameters<a name="aws-properties-events-rule-kinesisparameters"></a>

<a name="aws-properties-events-rule-kinesisparameters-description"></a>The `KinesisParameters` property type specifies settings that control shard assignment for a Kinesis stream target\.

<a name="aws-properties-events-rule-kinesisparameters-inheritance"></a> `KinesisParameters` is a property of the [CloudWatch Events Rule Target](aws-properties-events-rule-target.md) property type\. 

## Syntax<a name="aws-properties-events-rule-kinesisparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-kinesisparameters-syntax.json"></a>

```
{
  "[PartitionKeyPath](#cfn-events-rule-kinesisparameters-partitionkeypath)" : String
}
```

### YAML<a name="aws-properties-events-rule-kinesisparameters-syntax.yaml"></a>

```
[PartitionKeyPath](#cfn-events-rule-kinesisparameters-partitionkeypath): String
```

## Properties<a name="aws-properties-events-rule-kinesisparameters-properties"></a>

For more information, including constraints, see [KinesisParameters](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_KinesisParameters.html) in the *Amazon CloudWatch Events API Reference*\.

`PartitionKeyPath`  <a name="cfn-events-rule-kinesisparameters-partitionkeypath"></a>
The JSON path to extract from the event and use as the partition key\. The default is to use the `eventId` as the partition key\. For more information, see [Amazon Kinesis Streams Key Concepts](http://docs.aws.amazon.com/streams/latest/dev/key-concepts.html#partition-key) in the *Kinesis Streams Developer Guide*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
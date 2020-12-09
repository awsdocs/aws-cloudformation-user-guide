# AWS::Events::Rule KinesisParameters<a name="aws-properties-events-rule-kinesisparameters"></a>

The `KinesisParameters` property type specifies settings that control shard assignment for a Kinesis data stream target\.

 `KinesisParameters` is a property of the [Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html) property type\.

This object enables you to specify a JSON path to extract from the event and use as the partition key for the Amazon Kinesis data stream, so that you can control the shard that the event goes to\. If you don't include this parameter, the default is to use the `eventId` as the partition key\.

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

`PartitionKeyPath`  <a name="cfn-events-rule-kinesisparameters-partitionkeypath"></a>
The JSON path to be extracted from the event and used as the partition key\. For more information, see [Partition Key](https://docs.aws.amazon.com/streams/latest/dev/key-concepts.html#partition-key) in the *Amazon Kinesis Data Streams Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
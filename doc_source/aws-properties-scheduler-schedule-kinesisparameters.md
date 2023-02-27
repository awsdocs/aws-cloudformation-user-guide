# AWS::Scheduler::Schedule KinesisParameters<a name="aws-properties-scheduler-schedule-kinesisparameters"></a>

The templated target type for the Amazon Kinesis [kinesis/latest/APIReference/API_PutRecord.html](kinesis/latest/APIReference/API_PutRecord.html) API operation\.

## Syntax<a name="aws-properties-scheduler-schedule-kinesisparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-kinesisparameters-syntax.json"></a>

```
{
  "[PartitionKey](#cfn-scheduler-schedule-kinesisparameters-partitionkey)" : String
}
```

### YAML<a name="aws-properties-scheduler-schedule-kinesisparameters-syntax.yaml"></a>

```
  [PartitionKey](#cfn-scheduler-schedule-kinesisparameters-partitionkey): String
```

## Properties<a name="aws-properties-scheduler-schedule-kinesisparameters-properties"></a>

`PartitionKey`  <a name="cfn-scheduler-schedule-kinesisparameters-partitionkey"></a>
Specifies the shard to which EventBridge Scheduler sends the event\. For more information, see [Amazon Kinesis Data Streams terminology and concepts](https://docs.aws.amazon.com/streams/latest/dev/key-concepts.html) in the *Amazon Kinesis Streams Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
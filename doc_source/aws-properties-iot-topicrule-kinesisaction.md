# AWS IoT TopicRule KinesisAction<a name="aws-properties-iot-topicrule-kinesisaction"></a>

`Kinesis` is a property of the `Actions` property that describes an action that writes data to an Kinesis stream\.

## Syntax<a name="w3ab2c21c14e1351b5"></a>

### JSON<a name="aws-properties-iot-topicrule-kinesisaction-syntax.json"></a>

```
{
  "[PartitionKey](#cfn-iot-topicrule-kinesisaction-partitionkey)": String,
  "[RoleArn](#cfn-iot-topicrule-kinesisaction-rolearn)": String,
  "[StreamName](#cfn-iot-topicrule-kinesisaction-streamname)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-kinesisaction-syntax.yaml"></a>

```
[PartitionKey](#cfn-iot-topicrule-kinesisaction-partitionkey): String
[RoleArn](#cfn-iot-topicrule-kinesisaction-rolearn): String
[StreamName](#cfn-iot-topicrule-kinesisaction-streamname): String
```

## Properties<a name="w3ab2c21c14e1351b7"></a>

`PartitionKey`  <a name="cfn-iot-topicrule-kinesisaction-partitionkey"></a>
The partition key \(the grouping of data by shard within an Kinesis stream\)\.  
*Required*: No  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-kinesisaction-rolearn"></a>
The ARN of the IAM role that grants access to an Kinesis stream\.  
*Required*: Yes  
*Type*: String

`StreamName`  <a name="cfn-iot-topicrule-kinesisaction-streamname"></a>
The name of the Kinesis stream\.  
*Required*: Yes  
*Type*: String
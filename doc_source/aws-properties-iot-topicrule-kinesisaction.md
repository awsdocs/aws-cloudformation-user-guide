# AWS IoT TopicRule KinesisAction<a name="aws-properties-iot-topicrule-kinesisaction"></a>

`Kinesis` is a property of the `Actions` property that describes an action that writes data to an Kinesis stream\.

## Syntax<a name="w3ab2c21c14e1154b5"></a>

### JSON<a name="aws-properties-iot-topicrule-kinesisaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-kinesisaction-partitionkey)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-kinesisaction-rolearn)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-kinesisaction-streamname)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-kinesisaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-kinesisaction-partitionkey): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-kinesisaction-rolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-kinesisaction-streamname): String
```

## Properties<a name="w3ab2c21c14e1154b7"></a>

`PartitionKey`  
The partition key \(the grouping of data by shard within an Kinesis stream\)\.  
*Required: *No  
*Type*: String

`RoleArn`  
The ARN of the IAM role that grants access to an Kinesis stream\.  
*Required: *Yes  
*Type*: String

`StreamName`  
The name of the Kinesis stream\.  
*Required: *Yes  
*Type*: String
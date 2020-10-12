# AWS::QLDB::Stream KinesisConfiguration<a name="aws-properties-qldb-stream-kinesisconfiguration"></a>

The configuration settings of the Amazon Kinesis Data Streams destination for an Amazon QLDB journal stream\.

## Syntax<a name="aws-properties-qldb-stream-kinesisconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-qldb-stream-kinesisconfiguration-syntax.json"></a>

```
{
  "[AggregationEnabled](#cfn-qldb-stream-kinesisconfiguration-aggregationenabled)" : Boolean,
  "[StreamArn](#cfn-qldb-stream-kinesisconfiguration-streamarn)" : String
}
```

### YAML<a name="aws-properties-qldb-stream-kinesisconfiguration-syntax.yaml"></a>

```
  [AggregationEnabled](#cfn-qldb-stream-kinesisconfiguration-aggregationenabled): Boolean
  [StreamArn](#cfn-qldb-stream-kinesisconfiguration-streamarn): String
```

## Properties<a name="aws-properties-qldb-stream-kinesisconfiguration-properties"></a>

`AggregationEnabled`  <a name="cfn-qldb-stream-kinesisconfiguration-aggregationenabled"></a>
Enables QLDB to publish multiple data records in a single Kinesis Data Streams record\. To learn more, see [KPL Key Concepts](https://docs.aws.amazon.com/streams/latest/dev/kinesis-kpl-concepts.html) in the *Amazon Kinesis Data Streams Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StreamArn`  <a name="cfn-qldb-stream-kinesisconfiguration-streamarn"></a>
The Amazon Resource Name \(ARN\) of the Kinesis Data Streams resource\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `1600`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
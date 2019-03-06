# Amazon Kinesis Data Analytics ApplicationOutput KinesisStreamsOutput<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-description"></a>The `KinesisStreamsOutput` property type specifies a Kinesis data stream as the destination for a SQL\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-inheritance"></a> `KinesisStreamsOutput` is a property of the [Output](aws-properties-kinesisanalyticsv2-applicationoutput-output.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-syntax.yaml"></a>

```
[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-resourcearn"></a>
The ARN of the destination Kinesis data stream to write to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
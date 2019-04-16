# Amazon Kinesis Data Analytics ApplicationOutput KinesisFirehoseOutput<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-description"></a>The `KinesisFirehoseOutput` property type specifies a Kinesis Data Firehose delivery stream as the destination for a SQL\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-inheritance"></a> `KinesisFirehoseOutput` is a property of the [Output](aws-properties-kinesisanalyticsv2-applicationoutput-output.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-syntax.yaml"></a>

```
[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-resourcearn"></a>
The ARN of the destination delivery stream to write to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
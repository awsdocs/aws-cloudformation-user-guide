# Amazon Kinesis Data Analytics Application KinesisFirehoseInput<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput"></a>

<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-description"></a>The `KinesisFirehoseInput` property type for an SQL\-based Amazon Kinesis Data Analytics application to identify a Kinesis Data Firehose delivery stream as the streaming source\.

<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-inheritance"></a> `KinesisFirehoseInput` is a property of the [Input](aws-properties-kinesisanalyticsv2-application-input.md) resource\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisfirehoseinput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-syntax.yaml"></a>

```
[ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisfirehoseinput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-application-kinesisfirehoseinput-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the delivery stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
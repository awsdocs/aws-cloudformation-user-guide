# Amazon Kinesis Data Analytics Application KinesisStreamsInput<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput"></a>

<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-description"></a>The `KinesisStreamsInput` property type specifies an Kinesis data stream as the streaming source\.

<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-inheritance"></a> `KinesisStreamsInput` is a property of the [Input](aws-properties-kinesisanalyticsv2-application-input.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisstreamsinput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-syntax.yaml"></a>

```
[ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisstreamsinput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-application-kinesisstreamsinput-resourcearn"></a>
The ARN of the input Kinesis data stream to read\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
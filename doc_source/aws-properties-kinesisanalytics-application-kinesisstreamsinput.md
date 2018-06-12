# Amazon Kinesis Data Analytics Application KinesisStreamsInput<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput"></a>

The `KinesisStreamsInput` property type specifies an Amazon Kinesis stream as the streaming source for an Amazon Kinesis Data Analytics application\. 

 `KinesisStreamsInput` is a property of the [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalytics-application-kinesisstreamsinput-resourcearn)" : String,
  "[RoleARN](#cfn-kinesisanalytics-application-kinesisstreamsinput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalytics-application-kinesisstreamsinput-resourcearn): String
  [RoleARN](#cfn-kinesisanalytics-application-kinesisstreamsinput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalytics-application-kinesisstreamsinput-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the input Amazon Kinesis stream to read\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleARN`  <a name="cfn-kinesisanalytics-application-kinesisstreamsinput-rolearn"></a>
The ARN of the IAM role that Kinesis Data Analytics can assume to access the stream on your behalf\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
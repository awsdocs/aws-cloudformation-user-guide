# Amazon Kinesis Data Analytics Application KinesisStreamsInput<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput"></a>

The `KinesisStreamsInput` property type specifies an Amazon Kinesis stream as the streaming source for an Amazon Kinesis Data Analytics application\. 

 `KinesisStreamsInput` is a property of the [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-kinesisstreamsinput-resourcearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-kinesisstreamsinput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-kinesisstreamsinput-resourcearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-kinesisstreamsinput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-kinesisstreamsinput-properties"></a>

`ResourceARN`  
The Amazon Resource Name \(ARN\) of the input Amazon Kinesis stream to read\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`RoleARN`  
The ARN of the IAM role that Kinesis Data Analytics can assume to access the stream on your behalf\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 
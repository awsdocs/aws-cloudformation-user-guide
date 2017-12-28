# Amazon Kinesis Data Analytics ApplicationOutput KinesisFirehoseOutput<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput"></a>

The `KinesisFirehoseOutput` property type specifies an Amazon Kinesis Data Firehose delivery stream as the destination when you are configuring application output\.

 `KinesisFirehoseOutput` is a property of the [Kinesis Data Analytics ApplicationOutput Output](aws-properties-kinesisanalytics-applicationoutput-output.md) property type\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-resourcearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-resourcearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-properties"></a>

`ResourceARN`  
The Amazon Resource Name \(ARN\) of the destination Amazon Kinesis Data Firehose delivery stream to write to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`RoleARN`  
The ARN of the IAM role that Amazon Kinesis Data Analytics can assume to write to the destination stream on your behalf\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 
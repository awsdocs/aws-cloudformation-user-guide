# Amazon Kinesis Data Analytics ApplicationOutput KinesisFirehoseOutput<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput"></a>

The `KinesisFirehoseOutput` property type specifies an Amazon Kinesis Data Firehose delivery stream as the destination when you are configuring application output\.

 `KinesisFirehoseOutput` is a property of the [Kinesis Data Analytics ApplicationOutput Output](aws-properties-kinesisanalytics-applicationoutput-output.md) property type\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-resourcearn)" : String,
  "[RoleARN](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-resourcearn): String
  [RoleARN](#cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the destination Amazon Kinesis Data Firehose delivery stream to write to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleARN`  <a name="cfn-kinesisanalytics-applicationoutput-kinesisfirehoseoutput-rolearn"></a>
The ARN of the IAM role that Amazon Kinesis Data Analytics can assume to write to the destination stream on your behalf\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
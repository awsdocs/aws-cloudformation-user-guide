# Amazon Kinesis Data Analytics ApplicationOutput KinesisStreamsOutput<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput"></a>

The `KinesisStreamsOutput` property type specifies an Amazon Kinesis stream as the destination when you are configuring application output\.

 `KinesisStreamsOutput` is a property of the [Kinesis Data Analytics ApplicationOutput Output](aws-properties-kinesisanalytics-applicationoutput-output.md) property type\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalytics-applicationoutput-kinesisstreamsoutput-resourcearn)" : String,
  "[RoleARN](#cfn-kinesisanalytics-applicationoutput-kinesisstreamsoutput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalytics-applicationoutput-kinesisstreamsoutput-resourcearn): String
  [RoleARN](#cfn-kinesisanalytics-applicationoutput-kinesisstreamsoutput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalytics-applicationoutput-kinesisstreamsoutput-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the destination Amazon Kinesis stream to write to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleARN`  <a name="cfn-kinesisanalytics-applicationoutput-kinesisstreamsoutput-rolearn"></a>
The ARN of the IAM role that Amazon Kinesis Data Analytics can assume to write to the destination stream on your behalf\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
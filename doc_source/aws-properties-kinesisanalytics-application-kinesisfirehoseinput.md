# Amazon Kinesis Data Analytics Application KinesisFirehoseInput<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput"></a>

The `KinesisFirehoseInput` property type identifies an Amazon Kinesis Data Firehose delivery stream as the streaming source for an Amazon Kinesis Data Analytics application\.

 `KinesisFirehoseInput` is a property of the [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-syntax.json"></a>

```
{
  "[ResourceArn](#cfn-kinesisanalytics-application-kinesisfirehoseinput-resourcearn)" : String,
  "[RoleArn](#cfn-kinesisanalytics-application-kinesisfirehoseinput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-syntax.yaml"></a>

```
  [ResourceArn](#cfn-kinesisanalytics-application-kinesisfirehoseinput-resourcearn): String
  [RoleArn](#cfn-kinesisanalytics-application-kinesisfirehoseinput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-kinesisfirehoseinput-properties"></a>

`ResourceArn`  <a name="cfn-kinesisanalytics-application-kinesisfirehoseinput-resourcearn"></a>
The Amazon Resource Name \(Arn\) of the input Kinesis Firehose delivery stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-kinesisanalytics-application-kinesisfirehoseinput-rolearn"></a>
The Arn of the IAM role that Kinesis Data Analytics can assume to access the stream on your behalf\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
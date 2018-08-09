# Amazon Kinesis Data Analytics ApplicationOutput LambdaOutput<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput"></a>

The `LambdaOutput` property type specifies a Lambda function as the destination when you are configuring application output\.

 `LambdaOutput` is a property of the [Kinesis Data Analytics ApplicationOutput Output](aws-properties-kinesisanalytics-applicationoutput-output.md) property type\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-syntax.json"></a>

```
{
  "[ResourceArn](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-resourcearn)" : String,
  "[RoleArn](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-syntax.yaml"></a>

```
  [ResourceArn](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-resourcearn): String
  [RoleArn](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-properties"></a>

`ResourceArn`  <a name="cfn-kinesisanalytics-applicationoutput-lambdaoutput-resourcearn"></a>
The Amazon Resource Name \(Arn\) of the destination Amazon Lambda function to write to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-kinesisanalytics-applicationoutput-lambdaoutput-rolearn"></a>
The Arn of the IAM role that Amazon Kinesis Data Analytics can assume to write to the destination function on your behalf\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
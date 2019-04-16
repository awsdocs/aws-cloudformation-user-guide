# Amazon Kinesis Data Analytics ApplicationOutput LambdaOutput<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-description"></a>The `LambdaOutput` property type specifies an AWS Lambda function as the destination for a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-inheritance"></a> `LambdaOutput` is a property of the [Output](aws-properties-kinesisanalyticsv2-applicationoutput-output.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-lambdaoutput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-syntax.yaml"></a>

```
[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-lambdaoutput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-applicationoutput-lambdaoutput-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the destination Lambda function to write to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
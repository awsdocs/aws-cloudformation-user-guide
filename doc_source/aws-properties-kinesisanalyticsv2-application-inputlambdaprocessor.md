# Amazon Kinesis Data Analytics Application InputLambdaProcessor<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor"></a>

<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-description"></a>The `InputLambdaProcessor` property type specifies the Amazon Resource Name \(ARN\) of the AWS Lambda function that is used to preprocess records in the stream in an SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-inheritance"></a> `InputLambdaProcessor` is a property of the [InputProcessingConfiguration](aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-application-inputlambdaprocessor-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-syntax.yaml"></a>

```
[ResourceARN](#cfn-kinesisanalyticsv2-application-inputlambdaprocessor-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-application-inputlambdaprocessor-resourcearn"></a>
The ARN of the AWS Lambda function that operates on records in the stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
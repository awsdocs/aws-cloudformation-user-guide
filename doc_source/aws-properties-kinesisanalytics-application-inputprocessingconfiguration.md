# AWS::KinesisAnalytics::Application InputProcessingConfiguration<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration"></a>

Provides a description of a processor that is used to preprocess the records in the stream before being processed by your application code\. Currently, the only input processor available is [AWS Lambda](https://docs.aws.amazon.com/lambda/)\.

## Syntax<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-syntax.json"></a>

```
{
  "[InputLambdaProcessor](#cfn-kinesisanalytics-application-inputprocessingconfiguration-inputlambdaprocessor)" : InputLambdaProcessor
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-syntax.yaml"></a>

```
  [InputLambdaProcessor](#cfn-kinesisanalytics-application-inputprocessingconfiguration-inputlambdaprocessor): 
    InputLambdaProcessor
```

## Properties<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-properties"></a>

`InputLambdaProcessor`  <a name="cfn-kinesisanalytics-application-inputprocessingconfiguration-inputlambdaprocessor"></a>
The [InputLambdaProcessor](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisanalytics-application-inputlambdaprocessor.html) that is used to preprocess the records in the stream before being processed by your application code\.  
*Required*: No  
*Type*: [InputLambdaProcessor](aws-properties-kinesisanalytics-application-inputlambdaprocessor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
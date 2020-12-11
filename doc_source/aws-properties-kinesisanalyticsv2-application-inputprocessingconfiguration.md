# AWS::KinesisAnalyticsV2::Application InputProcessingConfiguration<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration"></a>

For an SQL\-based Amazon Kinesis Data Analytics application, describes a processor that is used to preprocess the records in the stream before being processed by your application code\. Currently, the only input processor available is [AWS Lambda](https://docs.aws.amazon.com/lambda/)\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-syntax.json"></a>

```
{
  "[InputLambdaProcessor](#cfn-kinesisanalyticsv2-application-inputprocessingconfiguration-inputlambdaprocessor)" : InputLambdaProcessor
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-syntax.yaml"></a>

```
  [InputLambdaProcessor](#cfn-kinesisanalyticsv2-application-inputprocessingconfiguration-inputlambdaprocessor): 
    InputLambdaProcessor
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-properties"></a>

`InputLambdaProcessor`  <a name="cfn-kinesisanalyticsv2-application-inputprocessingconfiguration-inputlambdaprocessor"></a>
The [InputLambdaProcessor](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_InputLambdaProcessor.html) that is used to preprocess the records in the stream before being processed by your application code\.  
*Required*: No  
*Type*: [InputLambdaProcessor](aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration--seealso"></a>
+  [InputProcessingConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_InputProcessingConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 


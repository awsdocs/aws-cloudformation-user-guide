# Amazon Kinesis Data Analytics Application InputProcessingConfiguration<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-description"></a>The `InputProcessingConfiguration` property type specifies a processor that is used to preprocess the records in the stream before being processed by your application code, for a SQL\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-inheritance"></a> `InputProcessingConfiguration` is a property of the [Input](aws-properties-kinesisanalyticsv2-application-input.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-syntax.json"></a>

```
{
  "[InputLambdaProcessor](#cfn-kinesisanalyticsv2-application-inputprocessingconfiguration-inputlambdaprocessor)" : [*InputLambdaProcessor*](aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-syntax.yaml"></a>

```
[InputLambdaProcessor](#cfn-kinesisanalyticsv2-application-inputprocessingconfiguration-inputlambdaprocessor): [*InputLambdaProcessor*](aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration-properties"></a>

`InputLambdaProcessor`  <a name="cfn-kinesisanalyticsv2-application-inputprocessingconfiguration-inputlambdaprocessor"></a>
The `InputLambdaProcessor` that is used to preprocess the records in the stream before being processed by your application code\.   
 *Required*: No  
 *Type*: [InputLambdaProcessor](aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
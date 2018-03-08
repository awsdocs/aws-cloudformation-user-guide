# Amazon Kinesis Data Analytics Application InputProcessingConfiguration<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration"></a>

The `InputProcessingConfiguration` property type specifies a processing configuration for a [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) for an Amazon Kinesis Data Analytics application\. 

 `InputProcessingConfiguration` is a property of the [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-syntax.json"></a>

```
{
  "[InputLambdaProcessor](#cfn-kinesisanalytics-application-inputprocessingconfiguration-inputlambdaprocessor)" : [*InputLambdaProcessor*](aws-properties-kinesisanalytics-application-inputlambdaprocessor.md)
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-syntax.yaml"></a>

```
  [InputLambdaProcessor](#cfn-kinesisanalytics-application-inputprocessingconfiguration-inputlambdaprocessor): [*InputLambdaProcessor*](aws-properties-kinesisanalytics-application-inputlambdaprocessor.md)
```

## Properties<a name="aws-properties-kinesisanalytics-application-inputprocessingconfiguration-properties"></a>

`InputLambdaProcessor`  <a name="cfn-kinesisanalytics-application-inputprocessingconfiguration-inputlambdaprocessor"></a>
The InputLambdaProcessor that is used to preprocess the records in the stream before they are processed by your application code\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics Application InputLambdaProcessor](aws-properties-kinesisanalytics-application-inputlambdaprocessor.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
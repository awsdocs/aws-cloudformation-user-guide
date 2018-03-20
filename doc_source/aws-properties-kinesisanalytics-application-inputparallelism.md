# Amazon Kinesis Data Analytics Application InputParallelism<a name="aws-properties-kinesisanalytics-application-inputparallelism"></a>

The `InputParallelism` property type specifies the number of in\-application streams to create for a given streaming source in an Amazon Kinesis Data Analytics application\.

 `InputParallelism` is a property of the [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-inputparallelism-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-inputparallelism-syntax.json"></a>

```
{
  "[Count](#cfn-kinesisanalytics-application-inputparallelism-count)" : Integer
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-inputparallelism-syntax.yaml"></a>

```
  [Count](#cfn-kinesisanalytics-application-inputparallelism-count): Integer
```

## Properties<a name="aws-properties-kinesisanalytics-application-inputparallelism-properties"></a>

`Count`  <a name="cfn-kinesisanalytics-application-inputparallelism-count"></a>
The number of in\-application streams to create\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
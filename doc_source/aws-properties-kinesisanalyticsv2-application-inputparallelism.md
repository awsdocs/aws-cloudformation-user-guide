# Amazon Kinesis Data Analytics Application InputParallelism<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism"></a>

<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-description"></a>The `InputParallelism` property type specifies the number of in\-application streams to create for a given streaming source for an SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-inheritance"></a> `InputParallelism` is a property of the [Input](aws-properties-kinesisanalyticsv2-application-input.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-syntax.json"></a>

```
{
  "[Count](#cfn-kinesisanalyticsv2-application-inputparallelism-count)" : Integer
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-syntax.yaml"></a>

```
[Count](#cfn-kinesisanalyticsv2-application-inputparallelism-count): Integer
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-properties"></a>

`Count`  <a name="cfn-kinesisanalyticsv2-application-inputparallelism-count"></a>
The number of in\-application streams to create\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
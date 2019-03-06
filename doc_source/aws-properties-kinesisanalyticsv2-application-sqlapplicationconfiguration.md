# Amazon Kinesis Data Analytics Application SqlApplicationConfiguration<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-description"></a>The `SqlApplicationConfiguration` property type specifies the inputs, outputs, and reference data sources for an SQL\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-inheritance"></a> `SqlApplicationConfiguration` is a property of the [ApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-syntax.json"></a>

```
{
  "[Inputs](#cfn-kinesisanalyticsv2-application-sqlapplicationconfiguration-inputs)" : [ [*Input*](aws-properties-kinesisanalyticsv2-application-input.md), ... ]
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-syntax.yaml"></a>

```
[Inputs](#cfn-kinesisanalyticsv2-application-sqlapplicationconfiguration-inputs): 
  - [*Input*](aws-properties-kinesisanalyticsv2-application-input.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-properties"></a>

`Inputs`  <a name="cfn-kinesisanalyticsv2-application-sqlapplicationconfiguration-inputs"></a>
The array of `input` objects describing the input streams used by the application\.   
 *Required*: No  
 *Type*: List of [Input](aws-properties-kinesisanalyticsv2-application-input.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
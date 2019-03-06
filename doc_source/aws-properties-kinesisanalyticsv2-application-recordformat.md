# Amazon Kinesis Data Analytics Application RecordFormat<a name="aws-properties-kinesisanalyticsv2-application-recordformat"></a>

<a name="aws-properties-kinesisanalyticsv2-application-recordformat-description"></a>The `RecordFormat` property type specifies the record format and relevant mapping information for records for a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-recordformat-inheritance"></a> `RecordFormat` is a property of the [InputSchema](aws-properties-kinesisanalyticsv2-application-inputschema.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-recordformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-recordformat-syntax.json"></a>

```
{
  "[MappingParameters](#cfn-kinesisanalyticsv2-application-recordformat-mappingparameters)" : [*MappingParameters*](aws-properties-kinesisanalyticsv2-application-mappingparameters.md),
  "[RecordFormatType](#cfn-kinesisanalyticsv2-application-recordformat-recordformattype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-recordformat-syntax.yaml"></a>

```
[MappingParameters](#cfn-kinesisanalyticsv2-application-recordformat-mappingparameters): [*MappingParameters*](aws-properties-kinesisanalyticsv2-application-mappingparameters.md)
[RecordFormatType](#cfn-kinesisanalyticsv2-application-recordformat-recordformattype): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-recordformat-properties"></a>

`MappingParameters`  <a name="cfn-kinesisanalyticsv2-application-recordformat-mappingparameters"></a>
Provides additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the streaming source\.  
 *Required*: No  
 *Type*: [MappingParameters](aws-properties-kinesisanalyticsv2-application-mappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordFormatType`  <a name="cfn-kinesisanalyticsv2-application-recordformat-recordformattype"></a>
The type of record format\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
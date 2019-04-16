# Amazon Kinesis Data Analytics ApplicationReferenceDataSource RecordFormat<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-description"></a>The `RecordFormat` property type specifies the record format and relevant mapping information in a reference source for a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-inheritance"></a> `RecordFormat` is a property of the [ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-syntax.json"></a>

```
{
  "[MappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-mappingparameters)" : [*MappingParameters*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters.md),
  "[RecordFormatType](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-recordformattype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-syntax.yaml"></a>

```
[MappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-mappingparameters): [*MappingParameters*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters.md)
[RecordFormatType](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-recordformattype): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-properties"></a>

`MappingParameters`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-mappingparameters"></a>
Provides additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the reference source\.  
 *Required*: No  
 *Type*: [MappingParameters](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordFormatType`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-recordformattype"></a>
The type of record format\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
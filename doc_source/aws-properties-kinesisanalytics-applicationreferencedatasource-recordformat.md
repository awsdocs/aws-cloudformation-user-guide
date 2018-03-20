# Amazon Kinesis Data Analytics ApplicationReferenceDataSource RecordFormat<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat"></a>

The `RecordFormat` property type specifies the record format and relevant mapping information that should be applied to schematize the records on the stream\. 

 `RecordFormat` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceSchema](aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema.md) parameter\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat-syntax.json"></a>

```
{
  "[MappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-recordformat-mappingparameters)" : [*MappingParameters*](aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters.md),
  "[RecordFormatType](#cfn-kinesisanalytics-applicationreferencedatasource-recordformat-recordformattype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat-syntax.yaml"></a>

```
  [MappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-recordformat-mappingparameters): 
    [*MappingParameters*](aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters.md)
  [RecordFormatType](#cfn-kinesisanalytics-applicationreferencedatasource-recordformat-recordformattype): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat-properties"></a>

`MappingParameters`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-recordformat-mappingparameters"></a>
When configuring application input at the time of creating or updating an application, provides additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the streaming source\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource MappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordFormatType`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-recordformat-recordformattype"></a>
The type of record format \(CSV or JSON\)\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
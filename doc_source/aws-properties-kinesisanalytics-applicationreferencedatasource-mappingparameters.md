# Amazon Kinesis Data Analytics ApplicationReferenceDataSource MappingParameters<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters"></a>

When configuring application input at the time of creating or updating an application, provides additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the streaming source\. 

 `MappingParameters` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource RecordFormat](aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat.md) parameter\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-syntax.json"></a>

```
{
  "[CSVMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-csvmappingparameters)" : [*CSVMappingParameters*](aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters.md),
  "[JSONMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-jsonmappingparameters)" : [*JSONMappingParameters*](aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters.md)
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-syntax.yaml"></a>

```
  [CSVMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-csvmappingparameters): 
    [*CSVMappingParameters*](aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters.md)
  [JSONMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-jsonmappingparameters): 
    [*JSONMappingParameters*](aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters.md)
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-properties"></a>

`CSVMappingParameters`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-csvmappingparameters"></a>
Provides additional mapping information when the record format uses delimiters \(for example, CSV\)\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource CSVMappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`JSONMappingParameters`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-jsonmappingparameters"></a>
Provides additional mapping information when JSON is the record format on the streaming source\.  
 *Required*: No  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource JSONMappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
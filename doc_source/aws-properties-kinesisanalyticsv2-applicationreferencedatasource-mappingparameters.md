# Amazon Kinesis Data Analytics ApplicationReferenceDataSource MappingParameters<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-description"></a>The `MappingParameters` property type specifies additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the reference source\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-inheritance"></a> `MappingParameters` is a property of the [ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-syntax.json"></a>

```
{
  "[JSONMappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-jsonmappingparameters)" : [*JSONMappingParameters*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters.md),
  "[CSVMappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-csvmappingparameters)" : [*CSVMappingParameters*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-syntax.yaml"></a>

```
[JSONMappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-jsonmappingparameters): [*JSONMappingParameters*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters.md)
[CSVMappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-csvmappingparameters): [*CSVMappingParameters*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-properties"></a>

`JSONMappingParameters`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-jsonmappingparameters"></a>
Provides additional mapping information when JSON is the record format on the reference source\.   
 *Required*: No  
 *Type*: [JSONMappingParameters](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CSVMappingParameters`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters-csvmappingparameters"></a>
Provides additional mapping information when the reference source record format uses delimiters \(for example, CSV\)\.   
 *Required*: No  
 *Type*: [CSVMappingParameters](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
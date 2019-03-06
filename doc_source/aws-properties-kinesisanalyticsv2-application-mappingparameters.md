# Amazon Kinesis Data Analytics Application MappingParameters<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters"></a>

<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-description"></a>The `MappingParameters` property type specifies additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the streaming source for a SQL\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-inheritance"></a> `MappingParameters` is a property of the [RecordFormat](aws-properties-kinesisanalyticsv2-application-recordformat.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-syntax.json"></a>

```
{
  "[JSONMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-jsonmappingparameters)" : [*JSONMappingParameters*](aws-properties-kinesisanalyticsv2-application-jsonmappingparameters.md),
  "[CSVMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-csvmappingparameters)" : [*CSVMappingParameters*](aws-properties-kinesisanalyticsv2-application-csvmappingparameters.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-syntax.yaml"></a>

```
[JSONMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-jsonmappingparameters): [*JSONMappingParameters*](aws-properties-kinesisanalyticsv2-application-jsonmappingparameters.md)
[CSVMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-csvmappingparameters): [*CSVMappingParameters*](aws-properties-kinesisanalyticsv2-application-csvmappingparameters.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-properties"></a>

`JSONMappingParameters`  <a name="cfn-kinesisanalyticsv2-application-mappingparameters-jsonmappingparameters"></a>
Provides additional mapping information when JSON is the record format on the streaming source\.   
 *Required*: No  
 *Type*: [JSONMappingParameters](aws-properties-kinesisanalyticsv2-application-jsonmappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CSVMappingParameters`  <a name="cfn-kinesisanalyticsv2-application-mappingparameters-csvmappingparameters"></a>
Provides additional mapping information when the record format uses delimiters \(for example, CSV\)\.  
 *Required*: No  
 *Type*: [CSVMappingParameters](aws-properties-kinesisanalyticsv2-application-csvmappingparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
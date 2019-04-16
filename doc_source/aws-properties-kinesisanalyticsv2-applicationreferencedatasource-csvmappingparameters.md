# Amazon Kinesis Data Analytics ApplicationReferenceDataSource CSVMappingParameters<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-description"></a>The `CSVMappingParameters` property type specifies additional mapping information for a SQL\-based Amazon Kinesis Data Analytics application when the record format uses delimiters, such as CSV\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-inheritance"></a> `CSVMappingParameters` is a property of the [MappingParameters](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters.md) resource\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-syntax.json"></a>

```
{
  "[RecordRowDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter)" : String,
  "[RecordColumnDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-syntax.yaml"></a>

```
[RecordRowDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter): String
[RecordColumnDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-properties"></a>

`RecordRowDelimiter`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter"></a>
The row delimiter\. For example, in a CSV format, '\\n' is the typical row delimiter\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordColumnDelimiter`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter"></a>
The column delimiter\. For example, in a CSV format, a comma \(","\) is the typical column delimiter\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
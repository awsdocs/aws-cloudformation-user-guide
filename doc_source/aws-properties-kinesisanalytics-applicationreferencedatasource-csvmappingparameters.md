# Amazon Kinesis Data Analytics ApplicationReferenceDataSource CSVMappingParameters<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters"></a>

In AWS CloudFormation, use the `CSVMappingParameters` property to specify additional mapping information when the record format uses delimiters, such as CSV\. 

 `CSVMappingParameters` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource MappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters.md) resource\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-syntax.json"></a>

```
{
  "[RecordColumnDelimiter](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter)" : String,
  "[RecordRowDelimiter](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-syntax.yaml"></a>

```
  [RecordColumnDelimiter](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter): String
  [RecordRowDelimiter](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-properties"></a>

`RecordColumnDelimiter`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter"></a>
The column delimiter\. For example, in a CSV format, a comma \(","\) is the typical column delimiter\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordRowDelimiter`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter"></a>
The row delimiter\. For example, in a CSV format, "\\n" is the typical row delimiter\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
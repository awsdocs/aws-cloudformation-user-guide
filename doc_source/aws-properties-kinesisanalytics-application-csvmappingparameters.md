# Amazon Kinesis Data Analytics Application CSVMappingParameters<a name="aws-properties-kinesisanalytics-application-csvmappingparameters"></a>

The `CSVMappingParameters` property type specifies additional mapping information when the record format uses delimiters, such as CSV\. 

 `CSVMappingParameters` is a property of the [Kinesis Data Analytics Application MappingParameters](aws-properties-kinesisanalytics-application-mappingparameters.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-csvmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-csvmappingparameters-syntax.json"></a>

```
{
  "[RecordColumnDelimiter](#cfn-kinesisanalytics-application-csvmappingparameters-recordcolumndelimiter)" : String,
  "[RecordRowDelimiter](#cfn-kinesisanalytics-application-csvmappingparameters-recordrowdelimiter)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-csvmappingparameters-syntax.yaml"></a>

```
  [RecordColumnDelimiter](#cfn-kinesisanalytics-application-csvmappingparameters-recordcolumndelimiter): String
  [RecordRowDelimiter](#cfn-kinesisanalytics-application-csvmappingparameters-recordrowdelimiter): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-csvmappingparameters-properties"></a>

`RecordColumnDelimiter`  <a name="cfn-kinesisanalytics-application-csvmappingparameters-recordcolumndelimiter"></a>
The column delimiter\. For example, in a CSV format, a comma \(","\) is the typical column delimiter\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordRowDelimiter`  <a name="cfn-kinesisanalytics-application-csvmappingparameters-recordrowdelimiter"></a>
The row delimiter\. For example, in a CSV format, "\\n" is the typical row delimiter\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
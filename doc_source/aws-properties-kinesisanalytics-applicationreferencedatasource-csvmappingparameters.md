# Amazon Kinesis Data Analytics ApplicationReferenceDataSource CSVMappingParameters<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters"></a>

In AWS CloudFormation, use the `CSVMappingParameters` property to specify additional mapping information when the record format uses delimiters, such as CSV\. 

 `CSVMappingParameters` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource MappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters.md) resource\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters-properties"></a>

`RecordColumnDelimiter`  
The column delimiter\. For example, in a CSV format, a comma \(","\) is the typical column delimiter\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`RecordRowDelimiter`  
The row delimiter\. For example, in a CSV format, "\\n" is the typical row delimiter\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 
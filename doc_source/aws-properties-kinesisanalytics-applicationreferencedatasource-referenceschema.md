# Amazon Kinesis Data Analytics ApplicationReferenceDataSource ReferenceSchema<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema"></a>

The `ReferenceSchema` property type specifies the format of the data in the streaming source, and how each data element maps to corresponding columns created in the in\-application stream\.

 `ReferenceSchema` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md) property\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordcolumns)" : [ RecordColumn, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordencoding)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordformat)" : RecordFormat
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordcolumns): 
    - RecordColumn 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordencoding): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordformat): 
    RecordFormat
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-properties"></a>

`RecordColumns`  
A list of [Amazon Kinesis Data Analytics ApplicationReferenceDataSource RecordColumn](aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn.md) objects\.  
 *Required*: Yes  
 *Type*: List of [Kinesis Data Analytics ApplicationReferenceDataSource RecordColumn](aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn.md)  
 *Update requires*: No interruption 

`RecordEncoding`  
Specifies the encoding of the records in the streaming source; For example, UTF\-8\.  
 *Required*: No  
 *Type*: String;  
 *Update requires*: No interruption 

`RecordFormat`  
Specifies the format of the records on the streaming source\.  
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource RecordFormat](aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat.md)  
 *Update requires*: No interruption 
# Amazon Kinesis Data Analytics ApplicationReferenceDataSource ReferenceSchema<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema"></a>

The `ReferenceSchema` property type specifies the format of the data in the streaming source, and how each data element maps to corresponding columns created in the in\-application stream\.

 `ReferenceSchema` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md) property\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-syntax.json"></a>

```
{
  "[RecordColumns](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordcolumns)" : [ [*RecordColumn*](aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn.md), ... ],
  "[RecordEncoding](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordencoding)" : String,
  "[RecordFormat](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordformat)" : [*RecordFormat*](aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat.md)
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-syntax.yaml"></a>

```
  [RecordColumns](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordcolumns): 
    - [*RecordColumn*](aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn.md) 
  [RecordEncoding](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordencoding): String
  [RecordFormat](#cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordformat): 
    [*RecordFormat*](aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat.md)
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema-properties"></a>

`RecordColumns`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordcolumns"></a>
A list of [Amazon Kinesis Data Analytics ApplicationReferenceDataSource RecordColumn](aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn.md) objects\.  
 *Required*: Yes  
 *Type*: List of [Kinesis Data Analytics ApplicationReferenceDataSource RecordColumn](aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordEncoding`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordencoding"></a>
Specifies the encoding of the records in the streaming source; For example, UTF\-8\.  
 *Required*: No  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordFormat`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referenceschema-recordformat"></a>
Specifies the format of the records on the streaming source\.  
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource RecordFormat](aws-properties-kinesisanalytics-applicationreferencedatasource-recordformat.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
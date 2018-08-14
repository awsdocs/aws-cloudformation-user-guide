# Amazon Kinesis Data Analytics Application InputSchema<a name="aws-properties-kinesisanalytics-application-inputschema"></a>

The `InputSchema` property type describes the format of the data in the streaming source, and how each data element maps to corresponding columns that are created in the in\-application stream in an Amazon Kinesis Data Analytics application\.

 `InputSchema` is a property of the [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-inputschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-inputschema-syntax.json"></a>

```
{
  "[RecordColumns](#cfn-kinesisanalytics-application-inputschema-recordcolumns)" : [ [*RecordColumn*](aws-properties-kinesisanalytics-application-recordcolumn.md), ... ],
  "[RecordEncoding](#cfn-kinesisanalytics-application-inputschema-recordencoding)" : String,
  "[RecordFormat](#cfn-kinesisanalytics-application-inputschema-recordformat)" : [*RecordFormat*](aws-properties-kinesisanalytics-application-recordformat.md)
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-inputschema-syntax.yaml"></a>

```
  [RecordColumns](#cfn-kinesisanalytics-application-inputschema-recordcolumns): 
    - [*RecordColumn*](aws-properties-kinesisanalytics-application-recordcolumn.md)
  [RecordEncoding](#cfn-kinesisanalytics-application-inputschema-recordencoding): String
  [RecordFormat](#cfn-kinesisanalytics-application-inputschema-recordformat): 
    [*RecordFormat*](aws-properties-kinesisanalytics-application-recordformat.md)
```

## Properties<a name="aws-properties-kinesisanalytics-application-inputschema-properties"></a>

`RecordColumns`  <a name="cfn-kinesisanalytics-application-inputschema-recordcolumns"></a>
A list of `RecordColumn` objects\.  
 *Required*: Yes  
 *Type*: List of [Kinesis Data Analytics Application RecordColumn](aws-properties-kinesisanalytics-application-recordcolumn.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordEncoding`  <a name="cfn-kinesisanalytics-application-inputschema-recordencoding"></a>
Specifies the encoding of the records in the streaming source; for example, `UTF-8`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordFormat`  <a name="cfn-kinesisanalytics-application-inputschema-recordformat"></a>
Specifies the format of the records on the streaming source\.  
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics Application RecordFormat](aws-properties-kinesisanalytics-application-recordformat.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
# Amazon Kinesis Data Analytics Application InputSchema<a name="aws-properties-kinesisanalyticsv2-application-inputschema"></a>

<a name="aws-properties-kinesisanalyticsv2-application-inputschema-description"></a>The `InputSchema` property type for a SQL\-based Kinesis Data Analytics application to describe the format of the data in the streaming source, and how each data element maps to corresponding columns created in the in\-application stream\.

<a name="aws-properties-kinesisanalyticsv2-application-inputschema-inheritance"></a> `InputSchema` is a property of the [Input](aws-properties-kinesisanalyticsv2-application-input.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-inputschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-inputschema-syntax.json"></a>

```
{
  "[RecordEncoding](#cfn-kinesisanalyticsv2-application-inputschema-recordencoding)" : String,
  "[RecordColumns](#cfn-kinesisanalyticsv2-application-inputschema-recordcolumns)" : [ [*RecordColumn*](aws-properties-kinesisanalyticsv2-application-recordcolumn.md), ... ],
  "[RecordFormat](#cfn-kinesisanalyticsv2-application-inputschema-recordformat)" : [*RecordFormat*](aws-properties-kinesisanalyticsv2-application-recordformat.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-inputschema-syntax.yaml"></a>

```
[RecordEncoding](#cfn-kinesisanalyticsv2-application-inputschema-recordencoding): String
[RecordColumns](#cfn-kinesisanalyticsv2-application-inputschema-recordcolumns): 
  - [*RecordColumn*](aws-properties-kinesisanalyticsv2-application-recordcolumn.md)
[RecordFormat](#cfn-kinesisanalyticsv2-application-inputschema-recordformat): [*RecordFormat*](aws-properties-kinesisanalyticsv2-application-recordformat.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-inputschema-properties"></a>

`RecordEncoding`  <a name="cfn-kinesisanalyticsv2-application-inputschema-recordencoding"></a>
Specifies the encoding of the records in the streaming source\. For example, UTF\-8\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordColumns`  <a name="cfn-kinesisanalyticsv2-application-inputschema-recordcolumns"></a>
A list of RecordColumn objects\.   
 *Required*: Yes  
 *Type*: List of [RecordColumn](aws-properties-kinesisanalyticsv2-application-recordcolumn.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordFormat`  <a name="cfn-kinesisanalyticsv2-application-inputschema-recordformat"></a>
Specifies the format of the records on the streaming source\.  
 *Required*: Yes  
 *Type*: [RecordFormat](aws-properties-kinesisanalyticsv2-application-recordformat.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
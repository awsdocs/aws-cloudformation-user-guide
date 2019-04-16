# Amazon Kinesis Data Analytics ApplicationReferenceDataSource ReferenceSchema<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-description"></a>The `ReferenceSchema` property type specifies the format of the data in the reference source for a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-inheritance"></a> `ReferenceSchema` is a property of the [ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-syntax.json"></a>

```
{
  "[RecordEncoding](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordencoding)" : String,
  "[RecordColumns](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordcolumns)" : [ [*RecordColumn*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn.md), ... ],
  "[RecordFormat](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordformat)" : [*RecordFormat*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-syntax.yaml"></a>

```
[RecordEncoding](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordencoding): String
[RecordColumns](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordcolumns): 
  - [*RecordColumn*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn.md)
[RecordFormat](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordformat): [*RecordFormat*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-properties"></a>

`RecordEncoding`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordencoding"></a>
Specifies the encoding of the records in the reference source\. For example, UTF\-8\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordColumns`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordcolumns"></a>
A list of `RecordColumn` objects\.   
 *Required*: Yes  
 *Type*: List of [RecordColumn](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RecordFormat`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referenceschema-recordformat"></a>
Specifies the format of the records on the reference source\.  
 *Required*: Yes  
 *Type*: [RecordFormat](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
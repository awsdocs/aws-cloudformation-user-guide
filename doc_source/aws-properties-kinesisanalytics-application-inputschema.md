# AWS::KinesisAnalytics::Application InputSchema<a name="aws-properties-kinesisanalytics-application-inputschema"></a>

Describes the format of the data in the streaming source, and how each data element maps to corresponding columns in the in\-application stream that is being created\.

Also used to describe the format of the reference data source\.

## Syntax<a name="aws-properties-kinesisanalytics-application-inputschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-inputschema-syntax.json"></a>

```
{
  "[RecordColumns](#cfn-kinesisanalytics-application-inputschema-recordcolumns)" : [ RecordColumn, ... ],
  "[RecordEncoding](#cfn-kinesisanalytics-application-inputschema-recordencoding)" : String,
  "[RecordFormat](#cfn-kinesisanalytics-application-inputschema-recordformat)" : RecordFormat
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-inputschema-syntax.yaml"></a>

```
  [RecordColumns](#cfn-kinesisanalytics-application-inputschema-recordcolumns): 
    - RecordColumn
  [RecordEncoding](#cfn-kinesisanalytics-application-inputschema-recordencoding): String
  [RecordFormat](#cfn-kinesisanalytics-application-inputschema-recordformat): 
    RecordFormat
```

## Properties<a name="aws-properties-kinesisanalytics-application-inputschema-properties"></a>

`RecordColumns`  <a name="cfn-kinesisanalytics-application-inputschema-recordcolumns"></a>
A list of `RecordColumn` objects\.  
*Required*: Yes  
*Type*: List of [RecordColumn](aws-properties-kinesisanalytics-application-recordcolumn.md)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordEncoding`  <a name="cfn-kinesisanalytics-application-inputschema-recordencoding"></a>
Specifies the encoding of the records in the streaming source\. For example, UTF\-8\.  
*Required*: No  
*Type*: String  
*Pattern*: `UTF-8`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordFormat`  <a name="cfn-kinesisanalytics-application-inputschema-recordformat"></a>
Specifies the format of the records on the streaming source\.  
*Required*: Yes  
*Type*: [RecordFormat](aws-properties-kinesisanalytics-application-recordformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
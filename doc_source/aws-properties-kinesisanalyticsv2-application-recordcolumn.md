# Amazon Kinesis Data Analytics Application RecordColumn<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn"></a>

<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-description"></a>The `RecordColumn` property type specifies the mapping of each data element in the streaming source to the corresponding column in the in\-application stream for a Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-inheritance"></a> `RecordColumn` is a property of the [InputSchema](aws-properties-kinesisanalyticsv2-application-inputschema.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-syntax.json"></a>

```
{
  "[Mapping](#cfn-kinesisanalyticsv2-application-recordcolumn-mapping)" : String,
  "[SqlType](#cfn-kinesisanalyticsv2-application-recordcolumn-sqltype)" : String,
  "[Name](#cfn-kinesisanalyticsv2-application-recordcolumn-name)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-syntax.yaml"></a>

```
[Mapping](#cfn-kinesisanalyticsv2-application-recordcolumn-mapping): String
[SqlType](#cfn-kinesisanalyticsv2-application-recordcolumn-sqltype): String
[Name](#cfn-kinesisanalyticsv2-application-recordcolumn-name): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-properties"></a>

`Mapping`  <a name="cfn-kinesisanalyticsv2-application-recordcolumn-mapping"></a>
A reference to the data element in the streaming input\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SqlType`  <a name="cfn-kinesisanalyticsv2-application-recordcolumn-sqltype"></a>
The type of column created in the in\-application input stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-kinesisanalyticsv2-application-recordcolumn-name"></a>
The name of the column that is created in the in\-application input stream\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
# Amazon Kinesis Data Analytics ApplicationReferenceDataSource RecordColumn<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn"></a>

The `RecordColumn` property type specifies the mapping of each data element in the streaming source to the corresponding column in the in\-application stream\. 

 `RecordColumn` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceSchema](aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema.md) resource\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn-syntax.json"></a>

```
{
  "[Mapping](#cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-mapping)" : String,
  "[Name](#cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-name)" : String,
  "[SqlType](#cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-sqltype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn-syntax.yaml"></a>

```
  [Mapping](#cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-mapping): String
  [Name](#cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-name): String
  [SqlType](#cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-sqltype): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-recordcolumn-properties"></a>

`Mapping`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-mapping"></a>
The reference to the data element in the streaming input of the reference data source\.  
 *Required*: No  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-name"></a>
The name of the column created in the in\-application input stream or reference table\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SqlType`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-recordcolumn-sqltype"></a>
The SQL data type of the column created in the in\-application input stream or reference table\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
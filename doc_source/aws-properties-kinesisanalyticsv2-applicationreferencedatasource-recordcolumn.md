# Amazon Kinesis Data Analytics ApplicationReferenceDataSource RecordColumn<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-description"></a>The `RecordColumn` property type specifies the mapping of each data element in the reference source in a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-inheritance"></a> `RecordColumn` is a property of the [ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-syntax.json"></a>

```
{
  "[Mapping](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-mapping)" : String,
  "[SqlType](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-sqltype)" : String,
  "[Name](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-name)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-syntax.yaml"></a>

```
[Mapping](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-mapping): String
[SqlType](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-sqltype): String
[Name](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-name): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-properties"></a>

`Mapping`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-mapping"></a>
A reference to the data element in the reference data source\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SqlType`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-sqltype"></a>
The type of column created in the in\-application reference table\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-recordcolumn-name"></a>
The name of the column that is created in the in\-application reference table\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
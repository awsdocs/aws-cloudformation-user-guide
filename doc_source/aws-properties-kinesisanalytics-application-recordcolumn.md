# Amazon Kinesis Data Analytics Application RecordColumn<a name="aws-properties-kinesisanalytics-application-recordcolumn"></a>

The `RecordColumn` property type specifies the mapping of each data element in the streaming source to the corresponding column in the in\-application stream in an Amazon Kinesis Data Analytics application\.

 `RecordColumn` is a property of the [Kinesis Data Analytics Application InputSchema](aws-properties-kinesisanalytics-application-inputschema.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-recordcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-recordcolumn-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-recordcolumn-mapping)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-recordcolumn-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-recordcolumn-sqltype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-recordcolumn-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-recordcolumn-mapping): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-recordcolumn-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-recordcolumn-sqltype): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-recordcolumn-properties"></a>

`Mapping`  
Reference to the data element in the streaming input of the reference data source\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Name`  
The name of the column created in the in\-application input stream or reference table\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`SqlType`  
The type of column created in the in\-application input stream or reference table\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 
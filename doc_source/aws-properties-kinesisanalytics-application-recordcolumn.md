# AWS::KinesisAnalytics::Application RecordColumn<a name="aws-properties-kinesisanalytics-application-recordcolumn"></a>

Describes the mapping of each data element in the streaming source to the corresponding column in the in\-application stream\.

Also used to describe the format of the reference data source\.

## Syntax<a name="aws-properties-kinesisanalytics-application-recordcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-recordcolumn-syntax.json"></a>

```
{
  "[Mapping](#cfn-kinesisanalytics-application-recordcolumn-mapping)" : String,
  "[Name](#cfn-kinesisanalytics-application-recordcolumn-name)" : String,
  "[SqlType](#cfn-kinesisanalytics-application-recordcolumn-sqltype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-recordcolumn-syntax.yaml"></a>

```
  [Mapping](#cfn-kinesisanalytics-application-recordcolumn-mapping): String
  [Name](#cfn-kinesisanalytics-application-recordcolumn-name): String
  [SqlType](#cfn-kinesisanalytics-application-recordcolumn-sqltype): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-recordcolumn-properties"></a>

`Mapping`  <a name="cfn-kinesisanalytics-application-recordcolumn-mapping"></a>
Reference to the data element in the streaming input or the reference data source\. This element is required if the [RecordFormatType](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/API_RecordFormat.html#analytics-Type-RecordFormat-RecordFormatTypel) is `JSON`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kinesisanalytics-application-recordcolumn-name"></a>
Name of the column created in the in\-application input stream or reference table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqlType`  <a name="cfn-kinesisanalytics-application-recordcolumn-sqltype"></a>
Type of column created in the in\-application input stream or reference table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
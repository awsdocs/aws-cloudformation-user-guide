# AWS::KinesisAnalyticsV2::Application RecordColumn<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn"></a>

For a SQL\-based Kinesis Data Analytics application, describes the mapping of each data element in the streaming source to the corresponding column in the in\-application stream\.

Also used to describe the format of the reference data source\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-syntax.json"></a>

```
{
  "[Mapping](#cfn-kinesisanalyticsv2-application-recordcolumn-mapping)" : String,
  "[Name](#cfn-kinesisanalyticsv2-application-recordcolumn-name)" : String,
  "[SqlType](#cfn-kinesisanalyticsv2-application-recordcolumn-sqltype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-syntax.yaml"></a>

```
  [Mapping](#cfn-kinesisanalyticsv2-application-recordcolumn-mapping): String
  [Name](#cfn-kinesisanalyticsv2-application-recordcolumn-name): String
  [SqlType](#cfn-kinesisanalyticsv2-application-recordcolumn-sqltype): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn-properties"></a>

`Mapping`  <a name="cfn-kinesisanalyticsv2-application-recordcolumn-mapping"></a>
A reference to the data element in the streaming input or the reference data source\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kinesisanalyticsv2-application-recordcolumn-name"></a>
The name of the column that is created in the in\-application input stream or reference table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[^-\s<>&]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqlType`  <a name="cfn-kinesisanalyticsv2-application-recordcolumn-sqltype"></a>
The type of column created in the in\-application input stream or reference table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-recordcolumn--seealso"></a>
+  [RecordColumn](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_RecordColumn.html) in the *Amazon Kinesis Data Analytics API Reference* 


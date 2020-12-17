# AWS::KinesisAnalyticsV2::Application CSVMappingParameters<a name="aws-properties-kinesisanalyticsv2-application-csvmappingparameters"></a>

For a SQL\-based Kinesis Data Analytics application, provides additional mapping information when the record format uses delimiters, such as CSV\. For example, the following sample records use CSV format, where the records use the *'\\n'* as the row delimiter and a comma \(","\) as the column delimiter: 

 `"name1", "address1"` 

 `"name2", "address2"` 

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-csvmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-csvmappingparameters-syntax.json"></a>

```
{
  "[RecordColumnDelimiter](#cfn-kinesisanalyticsv2-application-csvmappingparameters-recordcolumndelimiter)" : String,
  "[RecordRowDelimiter](#cfn-kinesisanalyticsv2-application-csvmappingparameters-recordrowdelimiter)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-csvmappingparameters-syntax.yaml"></a>

```
  [RecordColumnDelimiter](#cfn-kinesisanalyticsv2-application-csvmappingparameters-recordcolumndelimiter): String
  [RecordRowDelimiter](#cfn-kinesisanalyticsv2-application-csvmappingparameters-recordrowdelimiter): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-csvmappingparameters-properties"></a>

`RecordColumnDelimiter`  <a name="cfn-kinesisanalyticsv2-application-csvmappingparameters-recordcolumndelimiter"></a>
The column delimiter\. For example, in a CSV format, a comma \(","\) is the typical column delimiter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordRowDelimiter`  <a name="cfn-kinesisanalyticsv2-application-csvmappingparameters-recordrowdelimiter"></a>
The row delimiter\. For example, in a CSV format, *'\\n'* is the typical row delimiter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-csvmappingparameters--seealso"></a>
+  [CSVMappingParameters](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_CSVMappingParameters.html) in the *Amazon Kinesis Data Analytics API Reference* 


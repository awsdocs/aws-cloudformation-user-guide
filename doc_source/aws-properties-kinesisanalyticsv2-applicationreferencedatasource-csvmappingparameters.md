# AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource CSVMappingParameters<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters"></a>

For an SQL\-based application, provides additional mapping information when the record format uses delimiters, such as CSV\. For example, the following sample records use CSV format, where the records use the *'\\n'* as the row delimiter and a comma \(","\) as the column delimiter: 

 `"name1", "address1"` 

 `"name2", "address2"` 

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-syntax.json"></a>

```
{
  "[RecordColumnDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter)" : String,
  "[RecordRowDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-syntax.yaml"></a>

```
  [RecordColumnDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter): String
  [RecordRowDelimiter](#cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-properties"></a>

`RecordColumnDelimiter`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordcolumndelimiter"></a>
The column delimiter\. For example, in a CSV format, a comma \(","\) is the typical column delimiter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordRowDelimiter`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters-recordrowdelimiter"></a>
The row delimiter\. For example, in a CSV format, *'\\n'* is the typical row delimiter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-csvmappingparameters--seealso"></a>
+  [CSVMappingParameters](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_CSVMappingParameters.html) in the *Amazon Kinesis Data Analytics API Reference* 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`

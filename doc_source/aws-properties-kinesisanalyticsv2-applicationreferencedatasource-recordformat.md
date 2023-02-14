# AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource RecordFormat<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat"></a>

 For a SQL\-based Kinesis Data Analytics application, describes the record format and relevant mapping information that should be applied to schematize the records on the stream\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-syntax.json"></a>

```
{
  "[MappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-mappingparameters)" : MappingParameters,
  "[RecordFormatType](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-recordformattype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-syntax.yaml"></a>

```
  [MappingParameters](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-mappingparameters): 
    MappingParameters
  [RecordFormatType](#cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-recordformattype): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat-properties"></a>

`MappingParameters`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-mappingparameters"></a>
When you configure application input at the time of creating or updating an application, provides additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the streaming source\.  
*Required*: No  
*Type*: [MappingParameters](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordFormatType`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-recordformat-recordformattype"></a>
The type of record format\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CSV | JSON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-recordformat--seealso"></a>
+  [RecordFormat](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_RecordFormat.html) in the *Amazon Kinesis Data Analytics API Reference* 


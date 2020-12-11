# AWS::KinesisAnalyticsV2::ApplicationOutput DestinationSchema<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema"></a>

Describes the data format when records are written to the destination in a SQL\-based Kinesis Data Analytics application\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema-syntax.json"></a>

```
{
  "[RecordFormatType](#cfn-kinesisanalyticsv2-applicationoutput-destinationschema-recordformattype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema-syntax.yaml"></a>

```
  [RecordFormatType](#cfn-kinesisanalyticsv2-applicationoutput-destinationschema-recordformattype): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema-properties"></a>

`RecordFormatType`  <a name="cfn-kinesisanalyticsv2-applicationoutput-destinationschema-recordformattype"></a>
Specifies the format of the records on the output stream\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CSV | JSON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema--seealso"></a>
+  [DestinationSchema](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_DestinationSchema.html) in the *Amazon Kinesis Data Analytics API Reference* 


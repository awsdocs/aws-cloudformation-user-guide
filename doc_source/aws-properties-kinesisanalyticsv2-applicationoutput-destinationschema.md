# Amazon Kinesis Data Analytics ApplicationOutput DestinationSchema<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema-description"></a>The `DestinationSchema` property type specifies the data format when records are written to the destination in an SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema-inheritance"></a> `DestinationSchema` is a property of the [Output](aws-properties-kinesisanalyticsv2-applicationoutput-output.md) property\.

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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
# Amazon Kinesis Data Analytics ApplicationOutput DestinationSchema<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema"></a>

The `DestinationSchema` property describes the data format when records are written to the destination\.

 `DestinationSchema` is a property of the [Kinesis Data Analytics ApplicationOutput Output](aws-properties-kinesisanalytics-applicationoutput-output.md) property type\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-syntax.json"></a>

```
{
  "[RecordFormatType](#cfn-kinesisanalytics-applicationoutput-destinationschema-recordformattype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-syntax.yaml"></a>

```
  [RecordFormatType](#cfn-kinesisanalytics-applicationoutput-destinationschema-recordformattype): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-properties"></a>

`RecordFormatType`  <a name="cfn-kinesisanalytics-applicationoutput-destinationschema-recordformattype"></a>
Specifies the format of the records on the output stream\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
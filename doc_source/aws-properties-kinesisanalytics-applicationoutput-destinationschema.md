# Amazon Kinesis Data Analytics ApplicationOutput DestinationSchema<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema"></a>

The `DestinationSchema` property describes the data format when records are written to the destination\.

 `DestinationSchema` is a property of the [Kinesis Data Analytics ApplicationOutput Output](aws-properties-kinesisanalytics-applicationoutput-output.md) property type\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-destinationschema-recordformattype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-destinationschema-recordformattype): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema-properties"></a>

`RecordFormatType`  
Specifies the format of the records on the output stream\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 
# AWS::KinesisAnalytics::ApplicationOutput DestinationSchema<a name="aws-properties-kinesisanalytics-applicationoutput-destinationschema"></a>

Describes the data format when records are written to the destination\. For more information, see [Configuring Application Output](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-output.html)\. 

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
*Allowed values*: `CSV | JSON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
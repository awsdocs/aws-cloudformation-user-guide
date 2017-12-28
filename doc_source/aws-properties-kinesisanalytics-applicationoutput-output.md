# Amazon Kinesis Data Analytics ApplicationOutput Output<a name="aws-properties-kinesisanalytics-applicationoutput-output"></a>

The `Output` property type specifies an array of output configuration objects for an Amazon Kinesis Data Analytics application\.

 `Output` is a property of the [AWS::KinesisAnalytics::ApplicationOutput](aws-resource-kinesisanalytics-applicationoutput.md) resource\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-destinationschema)" : DestinationSchema,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput)" : KinesisFirehoseOutput,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput)" : KinesisStreamsOutput,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-name)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-destinationschema): 
    DestinationSchema
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput): 
    KinesisFirehoseOutput
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput): 
    KinesisStreamsOutput
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output-name): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-output-properties"></a>

`DestinationSchema`  
The data format when records are written to the destination\.  
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationOutput DestinationSchema](aws-properties-kinesisanalytics-applicationoutput-destinationschema.md)  
 *Update requires*: No interruption 

`KinesisFirehoseOutput`  
Identifies an Amazon Kinesis Data Firehose delivery stream as the destination\.  
 *Required*: Conditional\.   
 *Type*: [Kinesis Data Analytics ApplicationOutput KinesisFirehoseOutput](aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput.md)  
 *Update requires*: No interruption 

`KinesisStreamsOutput`  
Identifies an Amazon Kinesis stream as the destination\.   
 *Required*: Conditional\.   
 *Type*: [Kinesis Data Analytics ApplicationOutput KinesisStreamsOutput](aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput.md)  
 *Update requires*: No interruption 

`Name`  
The name of the in\-application stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 
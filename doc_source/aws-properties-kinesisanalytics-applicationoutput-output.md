# Amazon Kinesis Data Analytics ApplicationOutput Output<a name="aws-properties-kinesisanalytics-applicationoutput-output"></a>

The `Output` property type specifies an array of output configuration objects for an Amazon Kinesis Data Analytics application\.

 `Output` is a property of the [AWS::KinesisAnalytics::ApplicationOutput](aws-resource-kinesisanalytics-applicationoutput.md) resource\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax.json"></a>

```
{
  "[DestinationSchema](#cfn-kinesisanalytics-applicationoutput-output-destinationschema)" : [*DestinationSchema*](aws-properties-kinesisanalytics-applicationoutput-destinationschema.md),
  "[KinesisFirehoseOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput)" : [*KinesisFirehoseOutput*](aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput.md),
  "[KinesisStreamsOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput)" : [*KinesisStreamsOutput*](aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput.md),
  "[LambdaOutput](#cfn-kinesisanalytics-applicationoutput-output-lambdaoutput)" : [*LambdaOutput*](aws-properties-kinesisanalytics-applicationoutput-lambdaoutput.md),
  "[Name](#cfn-kinesisanalytics-applicationoutput-output-name)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax.yaml"></a>

```
  [DestinationSchema](#cfn-kinesisanalytics-applicationoutput-output-destinationschema): 
    [*DestinationSchema*](aws-properties-kinesisanalytics-applicationoutput-destinationschema.md)
  [KinesisFirehoseOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput): 
    [*KinesisFirehoseOutput*](aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput.md)
  [KinesisStreamsOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput): 
    [*KinesisStreamsOutput*](aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput.md)
  [LambdaOutput](#cfn-kinesisanalytics-applicationoutput-output-lambdaoutput): 
    [*LambdaOutput*](aws-properties-kinesisanalytics-applicationoutput-lambdaoutput.md)
  [Name](#cfn-kinesisanalytics-applicationoutput-output-name): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-output-properties"></a>

`DestinationSchema`  <a name="cfn-kinesisanalytics-applicationoutput-output-destinationschema"></a>
The data format when records are written to the destination\.  
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationOutput DestinationSchema](aws-properties-kinesisanalytics-applicationoutput-destinationschema.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KinesisFirehoseOutput`  <a name="cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput"></a>
Identifies an Amazon Kinesis Data Firehose delivery stream as the destination\.  
 *Required*: Conditional\.   
 *Type*: [Kinesis Data Analytics ApplicationOutput KinesisFirehoseOutput](aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KinesisStreamsOutput`  <a name="cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput"></a>
Identifies an Amazon Kinesis stream as the destination\.   
 *Required*: Conditional\.   
 *Type*: [Kinesis Data Analytics ApplicationOutput KinesisStreamsOutput](aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LambdaOutput`  <a name="cfn-kinesisanalytics-applicationoutput-output-lambdaoutput"></a>
Identifies a Lambda function as the destination\.   
 *Required*: Conditional\.   
 *Type*: [Kinesis Data Analytics ApplicationOutput LambdaOutput](aws-properties-kinesisanalytics-applicationoutput-lambdaoutput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-kinesisanalytics-applicationoutput-output-name"></a>
The name of the in\-application stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 
# Amazon Kinesis Data Analytics ApplicationOutput Output<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-description"></a>The `Output` property type specifies a SQL\-based Amazon Kinesis Data Analytics application's output configuration\.

<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-inheritance"></a> `Output` is a property of the [AWS::KinesisAnalyticsV2::ApplicationOutput](aws-resource-kinesisanalyticsv2-applicationoutput.md) resource\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-syntax.json"></a>

```
{
  "[DestinationSchema](#cfn-kinesisanalyticsv2-applicationoutput-output-destinationschema)" : [*DestinationSchema*](aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema.md),
  "[LambdaOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-lambdaoutput)" : [*LambdaOutput*](aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput.md),
  "[KinesisFirehoseOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisfirehoseoutput)" : [*KinesisFirehoseOutput*](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput.md),
  "[KinesisStreamsOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisstreamsoutput)" : [*KinesisStreamsOutput*](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput.md)
  "[Name](#cfn-kinesisanalyticsv2-applicationoutput-output-name)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-syntax.yaml"></a>

```
[DestinationSchema](#cfn-kinesisanalyticsv2-applicationoutput-output-destinationschema): [*DestinationSchema*](aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema.md)
[LambdaOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-lambdaoutput): [*LambdaOutput*](aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput.md)
[KinesisFirehoseOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisfirehoseoutput): [*KinesisFirehoseOutput*](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput.md)
[KinesisStreamsOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisstreamsoutput): [*KinesisStreamsOutput*](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput.md)
[Name](#cfn-kinesisanalyticsv2-applicationoutput-output-name): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-properties"></a>

`DestinationSchema`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-destinationschema"></a>
Describes the data format when records are written to the destination\.   
 *Required*: Yes  
 *Type*: [DestinationSchema](aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LambdaOutput`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-lambdaoutput"></a>
Identifies an AWS Lambda function as the destination\.  
 *Required*: No  
 *Type*: [LambdaOutput](aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KinesisFirehoseOutput`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-kinesisfirehoseoutput"></a>
Identifies an Amazon Kinesis Data Firehose delivery stream as the destination\.  
 *Required*: No  
 *Type*: [KinesisFirehoseOutput](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KinesisStreamsOutput`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-kinesisstreamsoutput"></a>
Identifies an Amazon Kinesis data stream as the destination\.  
 *Required*: No  
 *Type*: [KinesisStreamsOutput](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-name"></a>
The name of the in\-application stream\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 
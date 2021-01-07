# AWS::KinesisAnalyticsV2::ApplicationOutput Output<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output"></a>

 Describes a SQL\-based Kinesis Data Analytics application's output configuration, in which you identify an in\-application stream and a destination where you want the in\-application stream data to be written\. The destination can be a Kinesis data stream or a Kinesis Data Firehose delivery stream\. 



## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-syntax.json"></a>

```
{
  "[DestinationSchema](#cfn-kinesisanalyticsv2-applicationoutput-output-destinationschema)" : DestinationSchema,
  "[KinesisFirehoseOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisfirehoseoutput)" : KinesisFirehoseOutput,
  "[KinesisStreamsOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisstreamsoutput)" : KinesisStreamsOutput,
  "[LambdaOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-lambdaoutput)" : LambdaOutput,
  "[Name](#cfn-kinesisanalyticsv2-applicationoutput-output-name)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-syntax.yaml"></a>

```
  [DestinationSchema](#cfn-kinesisanalyticsv2-applicationoutput-output-destinationschema): 
    DestinationSchema
  [KinesisFirehoseOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisfirehoseoutput): 
    KinesisFirehoseOutput
  [KinesisStreamsOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-kinesisstreamsoutput): 
    KinesisStreamsOutput
  [LambdaOutput](#cfn-kinesisanalyticsv2-applicationoutput-output-lambdaoutput): 
    LambdaOutput
  [Name](#cfn-kinesisanalyticsv2-applicationoutput-output-name): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output-properties"></a>

`DestinationSchema`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-destinationschema"></a>
Describes the data format when records are written to the destination\.   
*Required*: Yes  
*Type*: [DestinationSchema](aws-properties-kinesisanalyticsv2-applicationoutput-destinationschema.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisFirehoseOutput`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-kinesisfirehoseoutput"></a>
Identifies a Kinesis Data Firehose delivery stream as the destination\.  
*Required*: No  
*Type*: [KinesisFirehoseOutput](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisStreamsOutput`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-kinesisstreamsoutput"></a>
Identifies a Kinesis data stream as the destination\.  
*Required*: No  
*Type*: [KinesisStreamsOutput](aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaOutput`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-lambdaoutput"></a>
Identifies an AWS Lambda function as the destination\.  
*Required*: No  
*Type*: [LambdaOutput](aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output-name"></a>
The name of the in\-application stream\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[^-\s<>&]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-kinesisanalyticsv2-applicationoutput-output--seealso"></a>
+  [Output](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_Output.html) in the *Amazon Kinesis Data Analytics API Reference* 


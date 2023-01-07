# AWS::KinesisAnalytics::ApplicationOutput Output<a name="aws-properties-kinesisanalytics-applicationoutput-output"></a>

 Describes application output configuration in which you identify an in\-application stream and a destination where you want the in\-application stream data to be written\. The destination can be an Amazon Kinesis stream or an Amazon Kinesis Firehose delivery stream\. 



For limits on how many destinations an application can write and other limitations, see [Limits](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/limits.html)\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax.json"></a>

```
{
  "[DestinationSchema](#cfn-kinesisanalytics-applicationoutput-output-destinationschema)" : DestinationSchema,
  "[KinesisFirehoseOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput)" : KinesisFirehoseOutput,
  "[KinesisStreamsOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput)" : KinesisStreamsOutput,
  "[LambdaOutput](#cfn-kinesisanalytics-applicationoutput-output-lambdaoutput)" : LambdaOutput,
  "[Name](#cfn-kinesisanalytics-applicationoutput-output-name)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-output-syntax.yaml"></a>

```
  [DestinationSchema](#cfn-kinesisanalytics-applicationoutput-output-destinationschema): 
    DestinationSchema
  [KinesisFirehoseOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput): 
    KinesisFirehoseOutput
  [KinesisStreamsOutput](#cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput): 
    KinesisStreamsOutput
  [LambdaOutput](#cfn-kinesisanalytics-applicationoutput-output-lambdaoutput): 
    LambdaOutput
  [Name](#cfn-kinesisanalytics-applicationoutput-output-name): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-output-properties"></a>

`DestinationSchema`  <a name="cfn-kinesisanalytics-applicationoutput-output-destinationschema"></a>
Describes the data format when records are written to the destination\. For more information, see [Configuring Application Output](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-output.html)\.  
*Required*: Yes  
*Type*: [DestinationSchema](aws-properties-kinesisanalytics-applicationoutput-destinationschema.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisFirehoseOutput`  <a name="cfn-kinesisanalytics-applicationoutput-output-kinesisfirehoseoutput"></a>
Identifies an Amazon Kinesis Firehose delivery stream as the destination\.  
*Required*: No  
*Type*: [KinesisFirehoseOutput](aws-properties-kinesisanalytics-applicationoutput-kinesisfirehoseoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisStreamsOutput`  <a name="cfn-kinesisanalytics-applicationoutput-output-kinesisstreamsoutput"></a>
Identifies an Amazon Kinesis stream as the destination\.  
*Required*: No  
*Type*: [KinesisStreamsOutput](aws-properties-kinesisanalytics-applicationoutput-kinesisstreamsoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaOutput`  <a name="cfn-kinesisanalytics-applicationoutput-output-lambdaoutput"></a>
Identifies an AWS Lambda function as the destination\.  
*Required*: No  
*Type*: [LambdaOutput](aws-properties-kinesisanalytics-applicationoutput-lambdaoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kinesisanalytics-applicationoutput-output-name"></a>
Name of the in\-application stream\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
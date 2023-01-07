# AWS::KinesisAnalytics::Application Input<a name="aws-properties-kinesisanalytics-application-input"></a>

When you configure the application input, you specify the streaming source, the in\-application stream name that is created, and the mapping between the two\. For more information, see [Configuring Application Input](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-input.html)\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-input-syntax.json"></a>

```
{
  "[InputParallelism](#cfn-kinesisanalytics-application-input-inputparallelism)" : InputParallelism,
  "[InputProcessingConfiguration](#cfn-kinesisanalytics-application-input-inputprocessingconfiguration)" : InputProcessingConfiguration,
  "[InputSchema](#cfn-kinesisanalytics-application-input-inputschema)" : InputSchema,
  "[KinesisFirehoseInput](#cfn-kinesisanalytics-application-input-kinesisfirehoseinput)" : KinesisFirehoseInput,
  "[KinesisStreamsInput](#cfn-kinesisanalytics-application-input-kinesisstreamsinput)" : KinesisStreamsInput,
  "[NamePrefix](#cfn-kinesisanalytics-application-input-nameprefix)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-input-syntax.yaml"></a>

```
  [InputParallelism](#cfn-kinesisanalytics-application-input-inputparallelism): 
    InputParallelism
  [InputProcessingConfiguration](#cfn-kinesisanalytics-application-input-inputprocessingconfiguration): 
    InputProcessingConfiguration
  [InputSchema](#cfn-kinesisanalytics-application-input-inputschema): 
    InputSchema
  [KinesisFirehoseInput](#cfn-kinesisanalytics-application-input-kinesisfirehoseinput): 
    KinesisFirehoseInput
  [KinesisStreamsInput](#cfn-kinesisanalytics-application-input-kinesisstreamsinput): 
    KinesisStreamsInput
  [NamePrefix](#cfn-kinesisanalytics-application-input-nameprefix): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-input-properties"></a>

`InputParallelism`  <a name="cfn-kinesisanalytics-application-input-inputparallelism"></a>
Describes the number of in\-application streams to create\.  
Data from your source is routed to these in\-application input streams\.  
 See [Configuring Application Input](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-input.html)\.  
*Required*: No  
*Type*: [InputParallelism](aws-properties-kinesisanalytics-application-inputparallelism.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputProcessingConfiguration`  <a name="cfn-kinesisanalytics-application-input-inputprocessingconfiguration"></a>
The [InputProcessingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisanalytics-application-inputprocessingconfiguration.html) for the input\. An input processor transforms records as they are received from the stream, before the application's SQL code executes\. Currently, the only input processing configuration available is [InputLambdaProcessor](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisanalytics-application-inputlambdaprocessor.html)\.  
*Required*: No  
*Type*: [InputProcessingConfiguration](aws-properties-kinesisanalytics-application-inputprocessingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputSchema`  <a name="cfn-kinesisanalytics-application-input-inputschema"></a>
Describes the format of the data in the streaming source, and how each data element maps to corresponding columns in the in\-application stream that is being created\.  
Also used to describe the format of the reference data source\.  
*Required*: Yes  
*Type*: [InputSchema](aws-properties-kinesisanalytics-application-inputschema.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisFirehoseInput`  <a name="cfn-kinesisanalytics-application-input-kinesisfirehoseinput"></a>
If the streaming source is an Amazon Kinesis Firehose delivery stream, identifies the delivery stream's ARN and an IAM role that enables Amazon Kinesis Analytics to access the stream on your behalf\.  
Note: Either `KinesisStreamsInput` or `KinesisFirehoseInput` is required\.  
*Required*: Conditional  
*Type*: [KinesisFirehoseInput](aws-properties-kinesisanalytics-application-kinesisfirehoseinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisStreamsInput`  <a name="cfn-kinesisanalytics-application-input-kinesisstreamsinput"></a>
If the streaming source is an Amazon Kinesis stream, identifies the stream's Amazon Resource Name \(ARN\) and an IAM role that enables Amazon Kinesis Analytics to access the stream on your behalf\.  
Note: Either `KinesisStreamsInput` or `KinesisFirehoseInput` is required\.  
*Required*: Conditional  
*Type*: [KinesisStreamsInput](aws-properties-kinesisanalytics-application-kinesisstreamsinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamePrefix`  <a name="cfn-kinesisanalytics-application-input-nameprefix"></a>
Name prefix to use when creating an in\-application stream\. Suppose that you specify a prefix "MyInApplicationStream\." Amazon Kinesis Analytics then creates one or more \(as per the `InputParallelism` count you specified\) in\-application streams with names "MyInApplicationStream\_001," "MyInApplicationStream\_002," and so on\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
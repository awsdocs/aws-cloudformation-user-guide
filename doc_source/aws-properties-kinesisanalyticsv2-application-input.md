# AWS::KinesisAnalyticsV2::Application Input<a name="aws-properties-kinesisanalyticsv2-application-input"></a>

When you configure the application input for a SQL\-based Kinesis Data Analytics application, you specify the streaming source, the in\-application stream name that is created, and the mapping between the two\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-input-syntax.json"></a>

```
{
  "[InputParallelism](#cfn-kinesisanalyticsv2-application-input-inputparallelism)" : InputParallelism,
  "[InputProcessingConfiguration](#cfn-kinesisanalyticsv2-application-input-inputprocessingconfiguration)" : InputProcessingConfiguration,
  "[InputSchema](#cfn-kinesisanalyticsv2-application-input-inputschema)" : InputSchema,
  "[KinesisFirehoseInput](#cfn-kinesisanalyticsv2-application-input-kinesisfirehoseinput)" : KinesisFirehoseInput,
  "[KinesisStreamsInput](#cfn-kinesisanalyticsv2-application-input-kinesisstreamsinput)" : KinesisStreamsInput,
  "[NamePrefix](#cfn-kinesisanalyticsv2-application-input-nameprefix)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-input-syntax.yaml"></a>

```
  [InputParallelism](#cfn-kinesisanalyticsv2-application-input-inputparallelism): 
    InputParallelism
  [InputProcessingConfiguration](#cfn-kinesisanalyticsv2-application-input-inputprocessingconfiguration): 
    InputProcessingConfiguration
  [InputSchema](#cfn-kinesisanalyticsv2-application-input-inputschema): 
    InputSchema
  [KinesisFirehoseInput](#cfn-kinesisanalyticsv2-application-input-kinesisfirehoseinput): 
    KinesisFirehoseInput
  [KinesisStreamsInput](#cfn-kinesisanalyticsv2-application-input-kinesisstreamsinput): 
    KinesisStreamsInput
  [NamePrefix](#cfn-kinesisanalyticsv2-application-input-nameprefix): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-input-properties"></a>

`InputParallelism`  <a name="cfn-kinesisanalyticsv2-application-input-inputparallelism"></a>
Describes the number of in\-application streams to create\.   
*Required*: No  
*Type*: [InputParallelism](aws-properties-kinesisanalyticsv2-application-inputparallelism.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputProcessingConfiguration`  <a name="cfn-kinesisanalyticsv2-application-input-inputprocessingconfiguration"></a>
The [InputProcessingConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_InputProcessingConfiguration.html) for the input\. An input processor transforms records as they are received from the stream, before the application's SQL code executes\. Currently, the only input processing configuration available is [InputLambdaProcessor](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_InputLambdaProcessor.html)\.   
*Required*: No  
*Type*: [InputProcessingConfiguration](aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputSchema`  <a name="cfn-kinesisanalyticsv2-application-input-inputschema"></a>
Describes the format of the data in the streaming source, and how each data element maps to corresponding columns in the in\-application stream that is being created\.  
Also used to describe the format of the reference data source\.  
*Required*: Yes  
*Type*: [InputSchema](aws-properties-kinesisanalyticsv2-application-inputschema.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisFirehoseInput`  <a name="cfn-kinesisanalyticsv2-application-input-kinesisfirehoseinput"></a>
If the streaming source is an Amazon Kinesis Data Firehose delivery stream, identifies the delivery stream's ARN\.  
*Required*: No  
*Type*: [KinesisFirehoseInput](aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisStreamsInput`  <a name="cfn-kinesisanalyticsv2-application-input-kinesisstreamsinput"></a>
If the streaming source is an Amazon Kinesis data stream, identifies the stream's Amazon Resource Name \(ARN\)\.   
*Required*: No  
*Type*: [KinesisStreamsInput](aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamePrefix`  <a name="cfn-kinesisanalyticsv2-application-input-nameprefix"></a>
The name prefix to use when creating an in\-application stream\. Suppose that you specify a prefix "`MyInApplicationStream`\." Kinesis Data Analytics then creates one or more \(as per the `InputParallelism` count you specified\) in\-application streams with the names "`MyInApplicationStream_001`," "`MyInApplicationStream_002`," and so on\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[^-\s<>&]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-input--seealso"></a>
+  [Input](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_Input.html) in the *Amazon Kinesis Data Analytics API Reference* 


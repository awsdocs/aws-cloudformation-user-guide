# Amazon Kinesis Data Analytics Application Input<a name="aws-properties-kinesisanalyticsv2-application-input"></a>

<a name="aws-properties-kinesisanalyticsv2-application-input-description"></a>The `Input` property type specifies a SQL application's streaming source, the in\-application stream name that is created, and the mapping between the two\. 

<a name="aws-properties-kinesisanalyticsv2-application-input-inheritance"></a> `Input` is a property of the [SqlApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-input-syntax.json"></a>

```
{
  "[NamePrefix](#cfn-kinesisanalyticsv2-application-input-nameprefix)" : String,
  "[InputSchema](#cfn-kinesisanalyticsv2-application-input-inputschema)" : [*InputSchema*](aws-properties-kinesisanalyticsv2-application-inputschema.md),
  "[KinesisStreamsInput](#cfn-kinesisanalyticsv2-application-input-kinesisstreamsinput)" : [*KinesisStreamsInput*](aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput.md),
  "[KinesisFirehoseInput](#cfn-kinesisanalyticsv2-application-input-kinesisfirehoseinput)" : [*KinesisFirehoseInput*](aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput.md),
  "[InputProcessingConfiguration](#cfn-kinesisanalyticsv2-application-input-inputprocessingconfiguration)" : [*InputProcessingConfiguration*](aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration.md),
  "[InputParallelism](#cfn-kinesisanalyticsv2-application-input-inputparallelism)" : [*InputParallelism*](aws-properties-kinesisanalyticsv2-application-inputparallelism.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-input-syntax.yaml"></a>

```
[NamePrefix](#cfn-kinesisanalyticsv2-application-input-nameprefix): String
[InputSchema](#cfn-kinesisanalyticsv2-application-input-inputschema): [*InputSchema*](aws-properties-kinesisanalyticsv2-application-inputschema.md)
[KinesisStreamsInput](#cfn-kinesisanalyticsv2-application-input-kinesisstreamsinput): [*KinesisStreamsInput*](aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput.md)
[KinesisFirehoseInput](#cfn-kinesisanalyticsv2-application-input-kinesisfirehoseinput): [*KinesisFirehoseInput*](aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput.md)
[InputProcessingConfiguration](#cfn-kinesisanalyticsv2-application-input-inputprocessingconfiguration): [*InputProcessingConfiguration*](aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration.md)
[InputParallelism](#cfn-kinesisanalyticsv2-application-input-inputparallelism): [*InputParallelism*](aws-properties-kinesisanalyticsv2-application-inputparallelism.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-input-properties"></a>

`NamePrefix`  <a name="cfn-kinesisanalyticsv2-application-input-nameprefix"></a>
The name prefix to use when creating an in\-application stream\. Suppose that you specify a prefix "MyInApplicationStream\." Kinesis Data Analytics then creates one or more \(as per the InputParallelism count you specified\) in\-application streams with the names "MyInApplicationStream\_001," "MyInApplicationStream\_002," and so on\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InputSchema`  <a name="cfn-kinesisanalyticsv2-application-input-inputschema"></a>
Describes the format of the data in the streaming source, and how each data element maps to corresponding columns in the in\-application stream that is being created\.  
 *Required*: Yes  
 *Type*: [InputSchema](aws-properties-kinesisanalyticsv2-application-inputschema.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KinesisStreamsInput`  <a name="cfn-kinesisanalyticsv2-application-input-kinesisstreamsinput"></a>
If the streaming source is an Amazon Kinesis data stream, identifies the stream's Amazon Resource Name \(ARN\)\.   
 *Required*: No  
 *Type*: [KinesisStreamsInput](aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KinesisFirehoseInput`  <a name="cfn-kinesisanalyticsv2-application-input-kinesisfirehoseinput"></a>
If the streaming source is an Amazon Kinesis Data Firehose delivery stream, identifies the delivery stream's ARN\.   
 *Required*: No  
 *Type*: [KinesisFirehoseInput](aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InputProcessingConfiguration`  <a name="cfn-kinesisanalyticsv2-application-input-inputprocessingconfiguration"></a>
The `InputProcessingConfiguration` for the input\. An input processor transforms records as they are received from the stream, before the application's SQL code executes\. Currently, the only input processing configuration available is `InputLambdaProcessor`\.   
 *Required*: No  
 *Type*: [InputProcessingConfiguration](aws-properties-kinesisanalyticsv2-application-inputprocessingconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InputParallelism`  <a name="cfn-kinesisanalyticsv2-application-input-inputparallelism"></a>
Describes the number of in\-application streams to create\.   
 *Required*: No  
 *Type*: [InputParallelism](aws-properties-kinesisanalyticsv2-application-inputparallelism.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
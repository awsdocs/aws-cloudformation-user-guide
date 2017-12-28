# Amazon Kinesis Data Analytics Application Input<a name="aws-properties-kinesisanalytics-application-input"></a>

When you configure the application input, you specify the streaming source, the in\-application stream name that is created, and the mapping between the two\. 

 `Input` is a property of the [AWS::KinesisAnalytics::Application](aws-resource-kinesisanalytics-application.md) resource\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-input-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-nameprefix)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-inputparallelism)" : InputParallelism,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-inputschema)" : InputSchema,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-kinesisfirehoseinput)" : KinesisFirehoseInput,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-kinesisstreamsinput)" : KinesisStreamsInput,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-inputprocessingconfiguration) :  InputProcessingConfiguration          
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-input-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-nameprefix): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-inputparallelism): 
    InputParallelism
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-inputschema): 
    InputSchema
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-kinesisfirehoseinput): 
    KinesisFirehoseInput
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-kinesisstreamsinput): 
    KinesisStreamsInput
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-input-inputprocessingconfiguration): 
    InputProcessingConfiguration
```

## Properties<a name="aws-properties-kinesisanalytics-application-input-properties"></a>

`NamePrefix`  
The name prefix to use when creating the in\-application streams\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`InputParallelism`  
Describes the number of in\-application streams to create\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics Application InputParallelism](aws-properties-kinesisanalytics-application-inputparallelism.md)  
 *Update requires*: No interruption 

`InputSchema`  
Describes the format of the data in the streaming source, and how each data element maps to corresponding columns in the in\-application stream that is being created\.  
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics Application InputSchema](aws-properties-kinesisanalytics-application-inputschema.md)  
 *Update requires*: No interruption 

`KinesisFirehoseInput`  
If the streaming source is an Amazon Kinesis Firehose delivery stream, identifies the delivery stream's Amazon Resource Name \(ARN\) and an IAM role that enables Kinesis Data Analytics to access the stream on your behalf\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics Application KinesisFirehoseInput](aws-properties-kinesisanalytics-application-kinesisfirehoseinput.md)  
 *Update requires*: No interruption 

`KinesisStreamsInput`  
If the streaming source is an Amazon Kinesis stream, identifies the stream's ARN and an IAM role that enables Kinesis Data Analytics to access the stream on your behalf\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics Application KinesisStreamsInput](aws-properties-kinesisanalytics-application-kinesisstreamsinput.md)  
 *Update requires*: No interruption 

`InputProcessingConfiguration`  
The input processing configuration for the input\. An input processor transforms records as they are received from the stream, before the application's SQL code executes\. Currently, the only input processing configuration available is `InputLambdaProcessor`\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics Application InputProcessingConfiguration](aws-properties-kinesisanalytics-application-inputprocessingconfiguration.md)  
 *Update requires*: No interruption 
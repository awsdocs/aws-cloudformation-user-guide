# AWS::KinesisAnalyticsV2::Application KinesisStreamsInput<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput"></a>

 Identifies an Amazon Kinesis data stream as the streaming source\. You provide the stream's Amazon Resource Name \(ARN\)\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisstreamsinput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisstreamsinput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-application-kinesisstreamsinput-resourcearn"></a>
The ARN of the input Kinesis data stream to read\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-kinesisanalyticsv2-application-kinesisstreamsinput--seealso"></a>
+  [KinesisStreamsInput](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_KinesisStreamsInput.html) in the *Amazon Kinesis Data Analytics API Reference* 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`

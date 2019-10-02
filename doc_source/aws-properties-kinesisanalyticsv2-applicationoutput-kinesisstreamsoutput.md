# AWS::KinesisAnalyticsV2::ApplicationOutput KinesisStreamsOutput<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput"></a>

When you configure an SQL\-based Amazon Kinesis Data Analytics application's output, identifies a Kinesis data stream as the destination\. You provide the stream Amazon Resource Name \(ARN\)\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput-resourcearn"></a>
The ARN of the destination Kinesis data stream to write to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisstreamsoutput--seealso"></a>
+  [KinesisStreamsOutput](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_KinesisStreamsOutput.html) in the *Amazon Kinesis Data Analytics API Reference* 

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

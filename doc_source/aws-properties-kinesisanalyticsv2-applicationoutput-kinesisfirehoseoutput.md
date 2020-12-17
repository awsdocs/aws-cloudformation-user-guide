# AWS::KinesisAnalyticsV2::ApplicationOutput KinesisFirehoseOutput<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput"></a>

For a SQL\-based Kinesis Data Analytics application, when configuring application output, identifies a Kinesis Data Firehose delivery stream as the destination\. You provide the stream Amazon Resource Name \(ARN\) of the delivery stream\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput-resourcearn"></a>
The ARN of the destination delivery stream to write to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-applicationoutput-kinesisfirehoseoutput--seealso"></a>
+  [KinesisFirehoseOutput](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_KinesisFirehoseOutput.html) in the *Amazon Kinesis Data Analytics API Reference* 


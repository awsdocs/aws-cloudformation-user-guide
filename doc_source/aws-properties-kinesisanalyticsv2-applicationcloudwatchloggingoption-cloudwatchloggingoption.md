# AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption CloudWatchLoggingOption<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption"></a>

Provides a description of Amazon CloudWatch logging options, including the log stream Amazon Resource Name \(ARN\)\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-syntax.json"></a>

```
{
  "[LogStreamARN](#cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-logstreamarn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-syntax.yaml"></a>

```
  [LogStreamARN](#cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-logstreamarn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-properties"></a>

`LogStreamARN`  <a name="cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-logstreamarn"></a>
The ARN of the CloudWatch log to receive application messages\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption--seealso"></a>
+  [CloudWatchLoggingOption](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_CloudWatchLoggingOption.html) in the *Amazon Kinesis Data Analytics API Reference* 


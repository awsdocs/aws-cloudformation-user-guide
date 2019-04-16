# Amazon Kinesis Data Analytics ApplicationCloudWatchLoggingOption CloudWatchLoggingOption<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-description"></a>The `CloudWatchLoggingOption` property type specifies an Amazon CloudWatch log stream to monitor application configuration errors\.

<a name="aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption-inheritance"></a> `CloudWatchLoggingOption` is a property of the [AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption](aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption.md) resource\.

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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
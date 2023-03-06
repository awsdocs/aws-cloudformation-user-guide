# AWS::IVSChat::LoggingConfiguration DestinationConfiguration<a name="aws-properties-ivschat-loggingconfiguration-destinationconfiguration"></a>

The DestinationConfiguration property type describes a location where chat logs will be stored\. Each member represents the configuration of one log destination\. For logging, you define only one type of destination\.

## Syntax<a name="aws-properties-ivschat-loggingconfiguration-destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivschat-loggingconfiguration-destinationconfiguration-syntax.json"></a>

```
{
  "[CloudWatchLogs](#cfn-ivschat-loggingconfiguration-destinationconfiguration-cloudwatchlogs)" : CloudWatchLogsDestinationConfiguration,
  "[Firehose](#cfn-ivschat-loggingconfiguration-destinationconfiguration-firehose)" : FirehoseDestinationConfiguration,
  "[S3](#cfn-ivschat-loggingconfiguration-destinationconfiguration-s3)" : S3DestinationConfiguration
}
```

### YAML<a name="aws-properties-ivschat-loggingconfiguration-destinationconfiguration-syntax.yaml"></a>

```
  [CloudWatchLogs](#cfn-ivschat-loggingconfiguration-destinationconfiguration-cloudwatchlogs): 
    CloudWatchLogsDestinationConfiguration
  [Firehose](#cfn-ivschat-loggingconfiguration-destinationconfiguration-firehose): 
    FirehoseDestinationConfiguration
  [S3](#cfn-ivschat-loggingconfiguration-destinationconfiguration-s3): 
    S3DestinationConfiguration
```

## Properties<a name="aws-properties-ivschat-loggingconfiguration-destinationconfiguration-properties"></a>

`CloudWatchLogs`  <a name="cfn-ivschat-loggingconfiguration-destinationconfiguration-cloudwatchlogs"></a>
An Amazon CloudWatch Logs destination configuration where chat activity will be logged\.  
*Required*: No  
*Type*: [CloudWatchLogsDestinationConfiguration](aws-properties-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Firehose`  <a name="cfn-ivschat-loggingconfiguration-destinationconfiguration-firehose"></a>
An Amazon Kinesis Data Firehose destination configuration where chat activity will be logged\.  
*Required*: No  
*Type*: [FirehoseDestinationConfiguration](aws-properties-ivschat-loggingconfiguration-firehosedestinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-ivschat-loggingconfiguration-destinationconfiguration-s3"></a>
An Amazon S3 destination configuration where chat activity will be logged\.  
*Required*: No  
*Type*: [S3DestinationConfiguration](aws-properties-ivschat-loggingconfiguration-s3destinationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
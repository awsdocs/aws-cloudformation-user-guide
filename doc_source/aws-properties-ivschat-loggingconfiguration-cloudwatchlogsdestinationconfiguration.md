# AWS::IVSChat::LoggingConfiguration CloudWatchLogsDestinationConfiguration<a name="aws-properties-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration"></a>

The CloudWatchLogsDestinationConfiguration property type specifies a CloudWatch Logs location where chat logs will be stored\.

## Syntax<a name="aws-properties-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration-syntax.json"></a>

```
{
  "[LogGroupName](#cfn-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration-loggroupname)" : String
}
```

### YAML<a name="aws-properties-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration-syntax.yaml"></a>

```
  [LogGroupName](#cfn-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration-loggroupname): String
```

## Properties<a name="aws-properties-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration-properties"></a>

`LogGroupName`  <a name="cfn-ivschat-loggingconfiguration-cloudwatchlogsdestinationconfiguration-loggroupname"></a>
Name of the Amazon Cloudwatch Logs destination where chat activity will be logged\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `^[\.\-_/#A-Za-z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
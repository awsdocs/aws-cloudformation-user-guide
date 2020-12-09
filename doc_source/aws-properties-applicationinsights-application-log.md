# AWS::ApplicationInsights::Application Log<a name="aws-properties-applicationinsights-application-log"></a>

The `AWS::ApplicationInsights::Application Log` property type specifies a log to monitor for the component\.

## Syntax<a name="aws-properties-applicationinsights-application-log-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-log-syntax.json"></a>

```
{
  "[Encoding](#cfn-applicationinsights-application-log-encoding)" : String,
  "[LogGroupName](#cfn-applicationinsights-application-log-loggroupname)" : String,
  "[LogPath](#cfn-applicationinsights-application-log-logpath)" : String,
  "[LogType](#cfn-applicationinsights-application-log-logtype)" : String,
  "[PatternSet](#cfn-applicationinsights-application-log-patternset)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-log-syntax.yaml"></a>

```
  [Encoding](#cfn-applicationinsights-application-log-encoding): String
  [LogGroupName](#cfn-applicationinsights-application-log-loggroupname): String
  [LogPath](#cfn-applicationinsights-application-log-logpath): String
  [LogType](#cfn-applicationinsights-application-log-logtype): String
  [PatternSet](#cfn-applicationinsights-application-log-patternset): String
```

## Properties<a name="aws-properties-applicationinsights-application-log-properties"></a>

`Encoding`  <a name="cfn-applicationinsights-application-log-encoding"></a>
The type of encoding of the logs to be monitored\. The specified encoding should be included in the list of CloudWatch agent supported encodings\. If not provided, CloudWatch Application Insights uses the default encoding type for the log type:  
+ `APPLICATION/DEFAULT`: utf\-8 encoding
+ `SQL_SERVER`: utf\-16 encoding
+ `IIS`: ascii encoding
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogGroupName`  <a name="cfn-applicationinsights-application-log-loggroupname"></a>
The CloudWatch log group name to be associated with the monitored log\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogPath`  <a name="cfn-applicationinsights-application-log-logpath"></a>
The path of the logs to be monitored\. The log path must be an absolute Windows or Linux system file path\. For more information, see [CloudWatch Agent Configuration File: Logs Section](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Agent-Configuration-File-Details.html#CloudWatch-Agent-Configuration-File-Logssection)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogType`  <a name="cfn-applicationinsights-application-log-logtype"></a>
The log type decides the log patterns against which Application Insights analyzes the log\. The log type is selected from the following: `SQL_SERVER`, `IIS`, `APPLICATION`, and `DEFAULT`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatternSet`  <a name="cfn-applicationinsights-application-log-patternset"></a>
The log pattern set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
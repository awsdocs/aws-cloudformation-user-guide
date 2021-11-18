# AWS::MWAA::Environment ModuleLoggingConfiguration<a name="aws-properties-mwaa-environment-moduleloggingconfiguration"></a>

Defines the type of logs to send for the Apache Airflow log type \(e\.g\. `DagProcessingLogs`\)\. 

## Syntax<a name="aws-properties-mwaa-environment-moduleloggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-moduleloggingconfiguration-syntax.json"></a>

```
{
  "[CloudWatchLogGroupArn](#cfn-mwaa-environment-moduleloggingconfiguration-cloudwatchloggrouparn)" : String,
  "[Enabled](#cfn-mwaa-environment-moduleloggingconfiguration-enabled)" : Boolean,
  "[LogLevel](#cfn-mwaa-environment-moduleloggingconfiguration-loglevel)" : String
}
```

### YAML<a name="aws-properties-mwaa-environment-moduleloggingconfiguration-syntax.yaml"></a>

```
  [CloudWatchLogGroupArn](#cfn-mwaa-environment-moduleloggingconfiguration-cloudwatchloggrouparn): String
  [Enabled](#cfn-mwaa-environment-moduleloggingconfiguration-enabled): Boolean
  [LogLevel](#cfn-mwaa-environment-moduleloggingconfiguration-loglevel): String
```

## Properties<a name="aws-properties-mwaa-environment-moduleloggingconfiguration-properties"></a>

`CloudWatchLogGroupArn`  <a name="cfn-mwaa-environment-moduleloggingconfiguration-cloudwatchloggrouparn"></a>
The ARN of the CloudWatch Logs log group for each type of Apache Airflow log type that you have enabled\.  
 `CloudWatchLogGroupArn` is available only as a return value, accessible when specified as an attribute in the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html#aws-resource-mwaa-environment-return-values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html#aws-resource-mwaa-environment-return-values) intrinsic function\. Any value you provide for `CloudWatchLogGroupArn` is discarded by Amazon MWAA\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-mwaa-environment-moduleloggingconfiguration-enabled"></a>
Indicates whether to enable the Apache Airflow log type \(e\.g\. `DagProcessingLogs`\) in CloudWatch Logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogLevel`  <a name="cfn-mwaa-environment-moduleloggingconfiguration-loglevel"></a>
Defines the Apache Airflow logs to send for the log type \(e\.g\. `DagProcessingLogs`\) to CloudWatch Logs\. Valid values: `CRITICAL`, `ERROR`, `WARNING`, `INFO`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
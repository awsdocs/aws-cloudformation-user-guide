# AWS::MWAA::Environment ModuleLoggingConfiguration<a name="aws-properties-mwaa-environment-moduleloggingconfiguration"></a>

The logging configuration for the environment\.

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
Provides the ARN for the CloudWatch group where the logs will be published\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-mwaa-environment-moduleloggingconfiguration-enabled"></a>
Specifies whether to enable logging\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogLevel`  <a name="cfn-mwaa-environment-moduleloggingconfiguration-loglevel"></a>
Defines the log level, which can be CRITICAL, ERROR, WARNING, or INFO\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
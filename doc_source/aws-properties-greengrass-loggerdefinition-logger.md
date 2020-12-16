# AWS::Greengrass::LoggerDefinition Logger<a name="aws-properties-greengrass-loggerdefinition-logger"></a>

<a name="aws-properties-greengrass-loggerdefinition-logger-description"></a>A logger represents logging settings for the AWS IoT Greengrass group, which can be stored in CloudWatch and the local file system of your core device\. All log entries include a timestamp, log level, and information about the event\. For more information, see [Monitoring with AWS IoT Greengrass Logs](https://docs.aws.amazon.com/greengrass/latest/developerguide/greengrass-logs-overview.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-loggerdefinition-logger-inheritance"></a> In an AWS CloudFormation template, the `Loggers` property of the [ `LoggerDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-loggerdefinition-loggerdefinitionversion.html) property type contains a list of `Logger` property types\.

## Syntax<a name="aws-properties-greengrass-loggerdefinition-logger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-loggerdefinition-logger-syntax.json"></a>

```
{
  "[Component](#cfn-greengrass-loggerdefinition-logger-component)" : String,
  "[Id](#cfn-greengrass-loggerdefinition-logger-id)" : String,
  "[Level](#cfn-greengrass-loggerdefinition-logger-level)" : String,
  "[Space](#cfn-greengrass-loggerdefinition-logger-space)" : Integer,
  "[Type](#cfn-greengrass-loggerdefinition-logger-type)" : String
}
```

### YAML<a name="aws-properties-greengrass-loggerdefinition-logger-syntax.yaml"></a>

```
  [Component](#cfn-greengrass-loggerdefinition-logger-component): String
  [Id](#cfn-greengrass-loggerdefinition-logger-id): String
  [Level](#cfn-greengrass-loggerdefinition-logger-level): String
  [Space](#cfn-greengrass-loggerdefinition-logger-space): Integer
  [Type](#cfn-greengrass-loggerdefinition-logger-type): String
```

## Properties<a name="aws-properties-greengrass-loggerdefinition-logger-properties"></a>

`Component`  <a name="cfn-greengrass-loggerdefinition-logger-component"></a>
The source of the log event\. Valid values are `GreengrassSystem` or `Lambda`\. When `GreengrassSystem` is used, events from Greengrass system components are logged\. When `Lambda` is used, events from user\-defined Lambda functions are logged\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Id`  <a name="cfn-greengrass-loggerdefinition-logger-id"></a>
A descriptive or arbitrary ID for the logger\. This value must be unique within the logger definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Level`  <a name="cfn-greengrass-loggerdefinition-logger-level"></a>
The log\-level threshold\. Log events below this threshold are filtered out and aren't stored\. Valid values are `DEBUG`, `INFO` \(recommended\), `WARN`, `ERROR`, or `FATAL`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Space`  <a name="cfn-greengrass-loggerdefinition-logger-space"></a>
The amount of file space \(in KB\) to use when writing logs to the local file system\. This property does not apply for CloudWatch Logs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-greengrass-loggerdefinition-logger-type"></a>
The storage mechanism for log events\. Valid values are `FileSystem` or `AWSCloudWatch`\. When `AWSCloudWatch` is used, log events are sent to CloudWatch Logs\. When `FileSystem` is used, log events are stored on the local file system\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-loggerdefinition-logger--seealso"></a>
+  [Logger](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-logger.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 
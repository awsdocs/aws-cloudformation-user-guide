# AWS::Logs::LogStream<a name="aws-resource-logs-logstream"></a>

The `AWS::Logs::LogStream` resource creates an Amazon CloudWatch Logs log stream in a log group\. A log stream represents the sequence of events coming from an application instance or resource that you are monitoring\. For more information, see [Monitoring Log Files](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/WhatIsCloudWatchLogs.html) in the *Amazon CloudWatch User Guide*\.

**Topics**
+ [Syntax](#aws-resource-logs-logstream-syntax)
+ [Properties](#w3ab2c21c10d876b9)
+ [Return Values](#w3ab2c21c10d876c11)
+ [Example](#w3ab2c21c10d876c13)

## Syntax<a name="aws-resource-logs-logstream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-logstream-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::LogStream",
  "Properties" : {
    "[LogGroupName](#cfn-logs-logstream-loggroupname)" : String,
    "[LogStreamName](#cfn-logs-logstream-logstreamname)" : String
  }
}
```

### YAML<a name="aws-resource-logs-logstream-syntax.yaml"></a>

```
Type: "AWS::Logs::LogStream"
Properties: 
  [LogGroupName](#cfn-logs-logstream-loggroupname): String
  [LogStreamName](#cfn-logs-logstream-logstreamname): String
```

## Properties<a name="w3ab2c21c10d876b9"></a>

`LogGroupName`  <a name="cfn-logs-logstream-loggroupname"></a>
The name of the log group where the log stream is created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LogStreamName`  <a name="cfn-logs-logstream-logstreamname"></a>
The name of the log stream to create\. The name must be unique within the log group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d876c11"></a>

### Ref<a name="w3ab2c21c10d876c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name, such as `MyAppLogStream`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d876c13"></a>

### <a name="w3ab2c21c10d876c13b2"></a>

The following example creates a CloudWatch Logs log stream named `MyAppLogStream` in the `exampleLogGroup` log group\.

#### JSON<a name="aws-resource-logs-logstream-example.json"></a>

```
"LogStream": {
  "Type": "AWS::Logs::LogStream",
  "Properties": {
    "LogGroupName" : "exampleLogGroup",
    "LogStreamName": "MyAppLogStream"
  }
}
```

#### YAML<a name="aws-resource-logs-logstream-example.yaml"></a>

```
LogStream: 
  Type: "AWS::Logs::LogStream"
  Properties: 
    LogGroupName: "exampleLogGroup"
    LogStreamName: "MyAppLogStream"
```
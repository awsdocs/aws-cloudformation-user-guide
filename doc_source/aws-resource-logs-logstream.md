# AWS::Logs::LogStream<a name="aws-resource-logs-logstream"></a>

The `AWS::Logs::LogStream` resource specifies an Amazon CloudWatch Logs log stream in a specific log group\. A log stream represents the sequence of events coming from an application instance or resource that you are monitoring\.

There is no limit on the number of log streams that you can create for a log group\.

You must use the following guidelines when naming a log stream:
+ Log stream names must be unique within the log group\.
+ Log stream names can be between 1 and 512 characters long\.
+ The ':' \(colon\) and '\*' \(asterisk\) characters are not allowed\.

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
Type: AWS::Logs::LogStream
Properties: 
  [LogGroupName](#cfn-logs-logstream-loggroupname): String
  [LogStreamName](#cfn-logs-logstream-logstreamname): String
```

## Properties<a name="aws-resource-logs-logstream-properties"></a>

`LogGroupName`  <a name="cfn-logs-logstream-loggroupname"></a>
The name of the log group where the log stream is created\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\.\-_/#A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogStreamName`  <a name="cfn-logs-logstream-logstreamname"></a>
The name of the log stream\. The name must be unique within the log group\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[^:*]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-logs-logstream-return-values"></a>

### Ref<a name="aws-resource-logs-logstream-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name, such as ` MyAppLogStream`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-logs-logstream--examples"></a>



### Create a Log Stream<a name="aws-resource-logs-logstream--examples--Create_a_Log_Stream"></a>

The following example creates a log stream named `MyAppLogStream` in the `exampleLogGroup` log group\.

#### JSON<a name="aws-resource-logs-logstream--examples--Create_a_Log_Stream--json"></a>

```
"LogStream": {
  "Type": "AWS::Logs::LogStream",
  "Properties": {
    "LogGroupName" : "exampleLogGroup",
    "LogStreamName": "MyAppLogStream"
  }
}
```

#### YAML<a name="aws-resource-logs-logstream--examples--Create_a_Log_Stream--yaml"></a>

```
LogStream: 
  Type: AWS::Logs::LogStream
  Properties: 
    LogGroupName: "exampleLogGroup"
    LogStreamName: "MyAppLogStream"
```
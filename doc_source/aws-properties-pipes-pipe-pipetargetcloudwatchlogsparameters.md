# AWS::Pipes::Pipe PipeTargetCloudWatchLogsParameters<a name="aws-properties-pipes-pipe-pipetargetcloudwatchlogsparameters"></a>

The parameters for using an CloudWatch Logs log stream as a target\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetcloudwatchlogsparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetcloudwatchlogsparameters-syntax.json"></a>

```
{
  "[LogStreamName](#cfn-pipes-pipe-pipetargetcloudwatchlogsparameters-logstreamname)" : String,
  "[Timestamp](#cfn-pipes-pipe-pipetargetcloudwatchlogsparameters-timestamp)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetcloudwatchlogsparameters-syntax.yaml"></a>

```
  [LogStreamName](#cfn-pipes-pipe-pipetargetcloudwatchlogsparameters-logstreamname): String
  [Timestamp](#cfn-pipes-pipe-pipetargetcloudwatchlogsparameters-timestamp): String
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetcloudwatchlogsparameters-properties"></a>

`LogStreamName`  <a name="cfn-pipes-pipe-pipetargetcloudwatchlogsparameters-logstreamname"></a>
The name of the log stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timestamp`  <a name="cfn-pipes-pipe-pipetargetcloudwatchlogsparameters-timestamp"></a>
The time the event occurred, expressed as the number of milliseconds after Jan 1, 1970 00:00:00 UTC\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
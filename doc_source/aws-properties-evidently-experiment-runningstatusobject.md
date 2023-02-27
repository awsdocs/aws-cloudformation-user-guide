# AWS::Evidently::Experiment RunningStatusObject<a name="aws-properties-evidently-experiment-runningstatusobject"></a>

Use this structure to start and stop the experiment\.

## Syntax<a name="aws-properties-evidently-experiment-runningstatusobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-experiment-runningstatusobject-syntax.json"></a>

```
{
  "[AnalysisCompleteTime](#cfn-evidently-experiment-runningstatusobject-analysiscompletetime)" : String,
  "[DesiredState](#cfn-evidently-experiment-runningstatusobject-desiredstate)" : String,
  "[Reason](#cfn-evidently-experiment-runningstatusobject-reason)" : String,
  "[Status](#cfn-evidently-experiment-runningstatusobject-status)" : String
}
```

### YAML<a name="aws-properties-evidently-experiment-runningstatusobject-syntax.yaml"></a>

```
  [AnalysisCompleteTime](#cfn-evidently-experiment-runningstatusobject-analysiscompletetime): String
  [DesiredState](#cfn-evidently-experiment-runningstatusobject-desiredstate): String
  [Reason](#cfn-evidently-experiment-runningstatusobject-reason): String
  [Status](#cfn-evidently-experiment-runningstatusobject-status): String
```

## Properties<a name="aws-properties-evidently-experiment-runningstatusobject-properties"></a>

`AnalysisCompleteTime`  <a name="cfn-evidently-experiment-runningstatusobject-analysiscompletetime"></a>
If you are using AWS CloudFormation to start the experiment, use this field to specify when the experiment is to end\. The format is as a UNIX timestamp\. For more information about this format, see [The Current Epoch Unix Timestamp](https://www.unixtimestamp.com/index.php)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredState`  <a name="cfn-evidently-experiment-runningstatusobject-desiredstate"></a>
If you are using AWS CloudFormation to stop this experiment, specify either `COMPLETED` or `CANCELLED` here to indicate how to classify this experiment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Reason`  <a name="cfn-evidently-experiment-runningstatusobject-reason"></a>
If you are using AWS CloudFormation to stop this experiment, this is an optional field that you can use to record why the experiment is being stopped or cancelled\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-evidently-experiment-runningstatusobject-status"></a>
To start the experiment now, specify `START` for this parameter\. If this experiment is currently running and you want to stop it now, specify `STOP`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
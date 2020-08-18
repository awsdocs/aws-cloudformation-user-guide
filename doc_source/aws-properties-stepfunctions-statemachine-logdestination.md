# AWS::StepFunctions::StateMachine LogDestination<a name="aws-properties-stepfunctions-statemachine-logdestination"></a>

Defines a destination for `LoggingConfiguration`\.

**Note**  
For more information on logging with `EXPRESS` workflows, see [Logging Express Workflows Using CloudWatch Logs](https://docs.aws.amazon.com/step-functions/latest/dg/cw-logs.html)\.

## Syntax<a name="aws-properties-stepfunctions-statemachine-logdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-stepfunctions-statemachine-logdestination-syntax.json"></a>

```
{
  "[CloudWatchLogsLogGroup](#cfn-stepfunctions-statemachine-logdestination-cloudwatchlogsloggroup)" : CloudWatchLogsLogGroup
}
```

### YAML<a name="aws-properties-stepfunctions-statemachine-logdestination-syntax.yaml"></a>

```
  [CloudWatchLogsLogGroup](#cfn-stepfunctions-statemachine-logdestination-cloudwatchlogsloggroup): 
    CloudWatchLogsLogGroup
```

## Properties<a name="aws-properties-stepfunctions-statemachine-logdestination-properties"></a>

`CloudWatchLogsLogGroup`  <a name="cfn-stepfunctions-statemachine-logdestination-cloudwatchlogsloggroup"></a>
An object describing a CloudWatch log group\. For more information, see [AWS::Logs::LogGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-loggroup.html) in the AWS CloudFormation User Guide\.  
*Required*: No  
*Type*: [CloudWatchLogsLogGroup](aws-properties-stepfunctions-statemachine-cloudwatchlogsloggroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
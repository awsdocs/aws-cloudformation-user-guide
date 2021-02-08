# AWS::StepFunctions::StateMachine LoggingConfiguration<a name="aws-properties-stepfunctions-statemachine-loggingconfiguration"></a>

Defines what execution history events are logged and where they are logged\.

**Note**  
By default, the `level` is set to `OFF`\. For more information see [Log Levels](https://docs.aws.amazon.com/step-functions/latest/dg/cloudwatch-log-level.html) in the AWS Step Functions User Guide\.

## Syntax<a name="aws-properties-stepfunctions-statemachine-loggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-stepfunctions-statemachine-loggingconfiguration-syntax.json"></a>

```
{
  "[Destinations](#cfn-stepfunctions-statemachine-loggingconfiguration-destinations)" : [ LogDestination, ... ],
  "[IncludeExecutionData](#cfn-stepfunctions-statemachine-loggingconfiguration-includeexecutiondata)" : Boolean,
  "[Level](#cfn-stepfunctions-statemachine-loggingconfiguration-level)" : String
}
```

### YAML<a name="aws-properties-stepfunctions-statemachine-loggingconfiguration-syntax.yaml"></a>

```
  [Destinations](#cfn-stepfunctions-statemachine-loggingconfiguration-destinations): 
    - LogDestination
  [IncludeExecutionData](#cfn-stepfunctions-statemachine-loggingconfiguration-includeexecutiondata): Boolean
  [Level](#cfn-stepfunctions-statemachine-loggingconfiguration-level): String
```

## Properties<a name="aws-properties-stepfunctions-statemachine-loggingconfiguration-properties"></a>

`Destinations`  <a name="cfn-stepfunctions-statemachine-loggingconfiguration-destinations"></a>
An array of objects that describes where your execution history events will be logged\. Limited to size 1\. Required, if your log level is not set to `OFF`\.  
*Required*: No  
*Type*: List of [LogDestination](aws-properties-stepfunctions-statemachine-logdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeExecutionData`  <a name="cfn-stepfunctions-statemachine-loggingconfiguration-includeexecutiondata"></a>
Determines whether execution data is included in your log\. When set to `false`, data is excluded\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Level`  <a name="cfn-stepfunctions-statemachine-loggingconfiguration-level"></a>
Defines which category of execution history events are logged\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
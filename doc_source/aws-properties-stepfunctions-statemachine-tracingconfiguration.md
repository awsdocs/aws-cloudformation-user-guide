# AWS::StepFunctions::StateMachine TracingConfiguration<a name="aws-properties-stepfunctions-statemachine-tracingconfiguration"></a>

Selects whether or not the state machine's AWS X\-Ray tracing is enabled\. To configure your state machine to send trace data to X\-Ray, set `Enabled` to `true`\.

## Syntax<a name="aws-properties-stepfunctions-statemachine-tracingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-stepfunctions-statemachine-tracingconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-stepfunctions-statemachine-tracingconfiguration-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-stepfunctions-statemachine-tracingconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-stepfunctions-statemachine-tracingconfiguration-enabled): Boolean
```

## Properties<a name="aws-properties-stepfunctions-statemachine-tracingconfiguration-properties"></a>

`Enabled`  <a name="cfn-stepfunctions-statemachine-tracingconfiguration-enabled"></a>
When set to `true`, X\-Ray tracing is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
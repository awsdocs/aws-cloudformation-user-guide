# AWS::Batch::JobDefinition EvaluateOnExit<a name="aws-properties-batch-jobdefinition-evaluateonexit"></a>

Specifies a set of conditions to be met, and an action to take \(`RETRY` or `EXIT`\) if all conditions are met\.

## Syntax<a name="aws-properties-batch-jobdefinition-evaluateonexit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-evaluateonexit-syntax.json"></a>

```
{
  "[Action](#cfn-batch-jobdefinition-evaluateonexit-action)" : String,
  "[OnExitCode](#cfn-batch-jobdefinition-evaluateonexit-onexitcode)" : String,
  "[OnReason](#cfn-batch-jobdefinition-evaluateonexit-onreason)" : String,
  "[OnStatusReason](#cfn-batch-jobdefinition-evaluateonexit-onstatusreason)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-evaluateonexit-syntax.yaml"></a>

```
  [Action](#cfn-batch-jobdefinition-evaluateonexit-action): String
  [OnExitCode](#cfn-batch-jobdefinition-evaluateonexit-onexitcode): String
  [OnReason](#cfn-batch-jobdefinition-evaluateonexit-onreason): String
  [OnStatusReason](#cfn-batch-jobdefinition-evaluateonexit-onstatusreason): String
```

## Properties<a name="aws-properties-batch-jobdefinition-evaluateonexit-properties"></a>

`Action`  <a name="cfn-batch-jobdefinition-evaluateonexit-action"></a>
Specifies the action to take if all of the specified conditions \(`onStatusReason`, `onReason`, and `onExitCode`\) are met\. The values are not case sensitive\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EXIT | RETRY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnExitCode`  <a name="cfn-batch-jobdefinition-evaluateonexit-onexitcode"></a>
Contains a glob pattern to match against the decimal representation of the `ExitCode` returned for a job\. The patten can be up to 512 characters long, can contain only numbers, and can optionally end with an asterisk \(\*\) so that only the start of the string needs to be an exact match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnReason`  <a name="cfn-batch-jobdefinition-evaluateonexit-onreason"></a>
Contains a glob pattern to match against the `Reason` returned for a job\. The patten can be up to 512 characters long, can contain letters, numbers, periods \(\.\), colons \(:\), and white space \(spaces, tabs\), and can optionally end with an asterisk \(\*\) so that only the start of the string needs to be an exact match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnStatusReason`  <a name="cfn-batch-jobdefinition-evaluateonexit-onstatusreason"></a>
Contains a glob pattern to match against the `StatusReason` returned for a job\. The patten can be up to 512 characters long, can contain letters, numbers, periods \(\.\), colons \(:\), and white space \(spaces, tabs\)\. and can optionally end with an asterisk \(\*\) so that only the start of the string needs to be an exact match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
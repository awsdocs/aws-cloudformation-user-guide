# AWS Batch JobDefinition Timeout<a name="aws-properties-batch-jobdefinition-timeout"></a>

<a name="aws-properties-batch-jobdefinition-timeout-description"></a>The `Timeout` property type specifies a job timeout configuration\.

<a name="aws-properties-batch-jobdefinition-timeout-inheritance"></a> `Timeout` is a property of the [AWS::Batch::JobDefinition](aws-resource-batch-jobdefinition.md) resource\.

## Syntax<a name="aws-properties-batch-jobdefinition-timeout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-timeout-syntax.json"></a>

```
{
  "[AttemptDurationSeconds](#cfn-batch-jobdefinition-timeout-attemptdurationseconds)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobdefinition-timeout-syntax.yaml"></a>

```
[AttemptDurationSeconds](#cfn-batch-jobdefinition-timeout-attemptdurationseconds): Integer
```

## Properties<a name="aws-properties-batch-jobdefinition-timeout-properties"></a>

`AttemptDurationSeconds`  <a name="cfn-batch-jobdefinition-timeout-attemptdurationseconds"></a>
The time duration in seconds \(measured from the job attempt's `startedAt` timestamp\) after which AWS Batch terminates your jobs if they have not finished\.   
 *Required*: No  
 *Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-batch-jobdefinition-timeout-seealso"></a>
+ [JobTimeout](https://docs.aws.amazon.com/batch/latest/APIReference/API_JobTimeout.html) in the *AWS Batch API Reference*
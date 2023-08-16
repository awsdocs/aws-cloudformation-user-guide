# AWS::Batch::JobDefinition Timeout<a name="aws-properties-batch-jobdefinition-timeout"></a>

An object that represents a job timeout configuration\.

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
The job timeout time \(in seconds\) that's measured from the job attempt's `startedAt` timestamp\. After this time passes, AWS Batch terminates your jobs if they aren't finished\. The minimum value for the timeout is 60 seconds\.  
For array jobs, the timeout applies to the child jobs, not to the parent array job\.  
For multi\-node parallel \(MNP\) jobs, the timeout applies to the whole job, not to the individual nodes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-batch-jobdefinition-timeout--seealso"></a>
+  [JobTimeout](https://docs.aws.amazon.com/batch/latest/APIReference/API_JobTimeout.html) in the *AWS Batch API Reference*\.
# AWS::Batch::JobDefinition RetryStrategy<a name="aws-properties-batch-jobdefinition-retrystrategy"></a>

The retry strategy associated with a job\. For more information, see [Automated job retries](https://docs.aws.amazon.com/batch/latest/userguide/job_retries.html) in the *AWS Batch User Guide*\.

## Syntax<a name="aws-properties-batch-jobdefinition-retrystrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-retrystrategy-syntax.json"></a>

```
{
  "[Attempts](#cfn-batch-jobdefinition-retrystrategy-attempts)" : Integer,
  "[EvaluateOnExit](#cfn-batch-jobdefinition-retrystrategy-evaluateonexit)" : [ EvaluateOnExit, ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-retrystrategy-syntax.yaml"></a>

```
  [Attempts](#cfn-batch-jobdefinition-retrystrategy-attempts): Integer
  [EvaluateOnExit](#cfn-batch-jobdefinition-retrystrategy-evaluateonexit): 
    - EvaluateOnExit
```

## Properties<a name="aws-properties-batch-jobdefinition-retrystrategy-properties"></a>

`Attempts`  <a name="cfn-batch-jobdefinition-retrystrategy-attempts"></a>
The number of times to move a job to the `RUNNABLE` status\. You can specify between 1 and 10 attempts\. If the value of `attempts` is greater than one, the job is retried on failure the same number of attempts as the value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EvaluateOnExit`  <a name="cfn-batch-jobdefinition-retrystrategy-evaluateonexit"></a>
Array of up to 5 objects that specify conditions under which the job should be retried or failed\. If this parameter is specified, then the `attempts` parameter must also be specified\.  
*Required*: No  
*Type*: [List](aws-properties-batch-jobdefinition-evaluateonexit.md) of [EvaluateOnExit](aws-properties-batch-jobdefinition-evaluateonexit.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
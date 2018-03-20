# AWS Batch JobDefinition RetryStrategy<a name="aws-properties-batch-jobdefinition-retrystrategy"></a>

The `RetryStrategy` property type specifies the retry strategy to use for failed jobs that are submitted with this job definition\.

## Syntax<a name="aws-properties-batch-jobdefinition-retrystrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-retrystrategy-syntax.json"></a>

```
{
  "[Attempts](#cfn-batch-jobdefinition-retrystrategy-attempts)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobdefinition-retrystrategy-syntax.yaml"></a>

```
[Attempts](#cfn-batch-jobdefinition-retrystrategy-attempts): Integer
```

## Properties<a name="aws-properties-batch-jobdefinition-retrystrategy-properties"></a>

`Attempts`  <a name="cfn-batch-jobdefinition-retrystrategy-attempts"></a>
The number of times to move a job to the `RUNNABLE` status\. You may specify between 1 and 10 attempts\. If `attempts` is greater than one, the job is retried if it fails until it has moved to `RUNNABLE` that many times\.  
 *Required*: no  
*Type*: Integer  
 *Update requires*: No Interruption 
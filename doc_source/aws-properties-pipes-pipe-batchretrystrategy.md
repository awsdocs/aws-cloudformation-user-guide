# AWS::Pipes::Pipe BatchRetryStrategy<a name="aws-properties-pipes-pipe-batchretrystrategy"></a>

The retry strategy that's associated with a job\. For more information, see [ Automated job retries](https://docs.aws.amazon.com/batch/latest/userguide/job_retries.html) in the *AWS Batch User Guide*\.

## Syntax<a name="aws-properties-pipes-pipe-batchretrystrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-batchretrystrategy-syntax.json"></a>

```
{
  "[Attempts](#cfn-pipes-pipe-batchretrystrategy-attempts)" : Integer
}
```

### YAML<a name="aws-properties-pipes-pipe-batchretrystrategy-syntax.yaml"></a>

```
  [Attempts](#cfn-pipes-pipe-batchretrystrategy-attempts): Integer
```

## Properties<a name="aws-properties-pipes-pipe-batchretrystrategy-properties"></a>

`Attempts`  <a name="cfn-pipes-pipe-batchretrystrategy-attempts"></a>
The number of times to move a job to the `RUNNABLE` status\. If the value of `attempts` is greater than one, the job is retried on failure the same number of attempts as the value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
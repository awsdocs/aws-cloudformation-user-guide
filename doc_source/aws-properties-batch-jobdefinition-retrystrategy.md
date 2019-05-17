# AWS::Batch::JobDefinition RetryStrategy<a name="aws-properties-batch-jobdefinition-retrystrategy"></a>

The retry strategy associated with a job\.

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
The number of times to move a job to the `RUNNABLE` status\. You may specify between 1 and 10 attempts\. If the value of `attempts` is greater than one, the job is retried on failure the same number of attempts as the value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
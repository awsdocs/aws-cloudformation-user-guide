# AWS::Events::Rule BatchRetryStrategy<a name="aws-properties-events-rule-batchretrystrategy"></a>

The retry strategy to use for failed jobs, if the target is an AWS Batch job\. If you specify a retry strategy here, it overrides the retry strategy defined in the job definition\.

## Syntax<a name="aws-properties-events-rule-batchretrystrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-batchretrystrategy-syntax.json"></a>

```
{
  "[Attempts](#cfn-events-rule-batchretrystrategy-attempts)" : Integer
}
```

### YAML<a name="aws-properties-events-rule-batchretrystrategy-syntax.yaml"></a>

```
  [Attempts](#cfn-events-rule-batchretrystrategy-attempts): Integer
```

## Properties<a name="aws-properties-events-rule-batchretrystrategy-properties"></a>

`Attempts`  <a name="cfn-events-rule-batchretrystrategy-attempts"></a>
The number of times to attempt to retry, if the job fails\. Valid values are 1–10\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`

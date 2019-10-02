# AWS::Batch::JobDefinition Timeout<a name="aws-properties-batch-jobdefinition-timeout"></a>

An object representing a job timeout configuration\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-batch-jobdefinition-timeout--seealso"></a>
+  [JobTimeout](https://docs.aws.amazon.com/batch/latest/APIReference/API_JobTimeout.html) in the *AWS Batch API Reference*\.

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

# AWS::SageMaker::EndpointConfig ServerlessConfig<a name="aws-properties-sagemaker-endpointconfig-productionvariant-serverlessconfig"></a>

Specifies the serverless configuration for an endpoint variant\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-productionvariant-serverlessconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-productionvariant-serverlessconfig-syntax.json"></a>

```
{
  "[MaxConcurrency](#cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig-maxconcurrency)" : Integer,
  "[MemorySizeInMB](#cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig-memorysizeinmb)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-productionvariant-serverlessconfig-syntax.yaml"></a>

```
  [MaxConcurrency](#cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig-maxconcurrency): Integer
  [MemorySizeInMB](#cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig-memorysizeinmb): Integer
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-productionvariant-serverlessconfig-properties"></a>

`MaxConcurrency`  <a name="cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig-maxconcurrency"></a>
The maximum number of concurrent invocations your serverless endpoint can process\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `200`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MemorySizeInMB`  <a name="cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig-memorysizeinmb"></a>
The memory size of your serverless endpoint\. Valid values are in 1 GB increments: 1024 MB, 2048 MB, 3072 MB, 4096 MB, 5120 MB, or 6144 MB\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1024`  
*Maximum*: `6144`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
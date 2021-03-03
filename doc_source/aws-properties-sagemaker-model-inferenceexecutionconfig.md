# AWS::SageMaker::Model InferenceExecutionConfig<a name="aws-properties-sagemaker-model-inferenceexecutionconfig"></a>

<a name="aws-properties-sagemaker-model-inferenceexecutionconfig-description"></a>The `InferenceExecutionConfig` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::SageMaker::Model](aws-resource-sagemaker-model.md)\.

## Syntax<a name="aws-properties-sagemaker-model-inferenceexecutionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-inferenceexecutionconfig-syntax.json"></a>

```
{
  "[Mode](#cfn-sagemaker-model-inferenceexecutionconfig-mode)" : String
}
```

### YAML<a name="aws-properties-sagemaker-model-inferenceexecutionconfig-syntax.yaml"></a>

```
  [Mode](#cfn-sagemaker-model-inferenceexecutionconfig-mode): String
```

## Properties<a name="aws-properties-sagemaker-model-inferenceexecutionconfig-properties"></a>

`Mode`  <a name="cfn-sagemaker-model-inferenceexecutionconfig-mode"></a>
How containers in a multi\-container are run\. The following values are valid\.  
+ `SERIAL` \- Containers run as a serial pipeline\.
+ `DIRECT` \- Only the individual container that you specify is run\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
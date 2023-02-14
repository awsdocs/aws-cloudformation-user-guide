# AWS::SageMaker::Model MultiModelConfig<a name="aws-properties-sagemaker-model-containerdefinition-multimodelconfig"></a>

Specifies additional configuration for hosting multi\-model endpoints\.

## Syntax<a name="aws-properties-sagemaker-model-containerdefinition-multimodelconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-containerdefinition-multimodelconfig-syntax.json"></a>

```
{
  "[ModelCacheSetting](#cfn-sagemaker-model-containerdefinition-multimodelconfig-modelcachesetting)" : String
}
```

### YAML<a name="aws-properties-sagemaker-model-containerdefinition-multimodelconfig-syntax.yaml"></a>

```
  [ModelCacheSetting](#cfn-sagemaker-model-containerdefinition-multimodelconfig-modelcachesetting): String
```

## Properties<a name="aws-properties-sagemaker-model-containerdefinition-multimodelconfig-properties"></a>

`ModelCacheSetting`  <a name="cfn-sagemaker-model-containerdefinition-multimodelconfig-modelcachesetting"></a>
Whether to cache models for a multi\-model endpoint\. By default, multi\-model endpoints cache models so that a model does not have to be loaded into memory each time it is invoked\. Some use cases do not benefit from model caching\. For example, if an endpoint hosts a large number of models that are each invoked infrequently, the endpoint might perform better if you disable model caching\. To disable model caching, set the value of this parameter to Disabled\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
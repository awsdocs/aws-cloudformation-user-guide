# Amazon SageMaker Model ContainerDefinition<a name="aws-properties-sagemaker-model-containerdefinition"></a>

<a name="aws-properties-sagemaker-model-containerdefinition-description"></a>The `ContainerDefinition` property type specifies the definition of the container for a model\.

<a name="aws-properties-sagemaker-model-containerdefinition-inheritance"></a> `ContainerDefinition` is a property of the [AWS::SageMaker::Model](aws-resource-sagemaker-model.md) resource\.

## Syntax<a name="aws-properties-sagemaker-model-containerdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-containerdefinition-syntax.json"></a>

```
{
  "[ContainerHostname](#cfn-sagemaker-model-containerdefinition-containerhostname)" : String,
  "[Environment](#cfn-sagemaker-model-containerdefinition-environment)" : String,
  "[ModelDataUrl](#cfn-sagemaker-model-containerdefinition-modeldataurl)" : JSON,
  "[Image](#cfn-sagemaker-model-containerdefinition-image)" : String
}
```

### YAML<a name="aws-properties-sagemaker-model-containerdefinition-syntax.yaml"></a>

```
[ContainerHostname](#cfn-sagemaker-model-containerdefinition-containerhostname): String
[Environment](#cfn-sagemaker-model-containerdefinition-environment): String
[ModelDataUrl](#cfn-sagemaker-model-containerdefinition-modeldataurl): JSON
[Image](#cfn-sagemaker-model-containerdefinition-image): String
```

## Properties<a name="aws-properties-sagemaker-model-containerdefinition-properties"></a>

`ContainerHostname`  <a name="cfn-sagemaker-model-containerdefinition-containerhostname"></a>
The DNS host name for the container after Amazon SageMaker deploys it\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Environment`  <a name="cfn-sagemaker-model-containerdefinition-environment"></a>
The environment variables to set in the Docker container\. Each key and value in the `Environment` string to string map can have length of up to 1024\. We support up to 16 entries in the map\.   
 *Required*: No  
 *Type*: JSON  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ModelDataUrl`  <a name="cfn-sagemaker-model-containerdefinition-modeldataurl"></a>
The S3 path where the model artifacts, which result from model training, are stored\. This path must point to a single gzip compressed tar archive \(\.tar\.gz suffix\)  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Image`  <a name="cfn-sagemaker-model-containerdefinition-image"></a>
The Amazon EC2 Container Registry \(Amazon ECR\) path where inference code is stored\. If you are using your own custom algorithm instead of an algorithm provided by Amazon SageMaker, the inference code must meet Amazon SageMaker requirements\. For more information, see [Using Your Own Algorithms with Amazon SageMaker](http://docs.aws.amazon.com/sagemaker/latest/dg/your-algorithms.html)  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 
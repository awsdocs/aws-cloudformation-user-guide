# AWS::SageMaker::Model ContainerDefinition<a name="aws-properties-sagemaker-model-containerdefinition"></a>

Describes the container, as part of model definition\.

## Syntax<a name="aws-properties-sagemaker-model-containerdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-containerdefinition-syntax.json"></a>

```
{
  "[ContainerHostname](#cfn-sagemaker-model-containerdefinition-containerhostname)" : String,
  "[Environment](#cfn-sagemaker-model-containerdefinition-environment)" : Json,
  "[Image](#cfn-sagemaker-model-containerdefinition-image)" : String,
  "[ModelDataUrl](#cfn-sagemaker-model-containerdefinition-modeldataurl)" : String
}
```

### YAML<a name="aws-properties-sagemaker-model-containerdefinition-syntax.yaml"></a>

```
  [ContainerHostname](#cfn-sagemaker-model-containerdefinition-containerhostname): String
  [Environment](#cfn-sagemaker-model-containerdefinition-environment): Json
  [Image](#cfn-sagemaker-model-containerdefinition-image): String
  [ModelDataUrl](#cfn-sagemaker-model-containerdefinition-modeldataurl): String
```

## Properties<a name="aws-properties-sagemaker-model-containerdefinition-properties"></a>

`ContainerHostname`  <a name="cfn-sagemaker-model-containerdefinition-containerhostname"></a>
This parameter is ignored for models that contain only a `PrimaryContainer`\.  
When a `ContainerDefinition` is part of an inference pipeline, the value of ths parameter uniquely identifies the container for the purposes of logging and metrics\. For information, see [Use Logs and Metrics to Monitor an Inference Pipeline](http://docs.aws.amazon.com/sagemaker/latest/dg/inference-pipeline-logs-metrics.html)\. If you don't specify a value for this parameter for a `ContainerDefinition` that is part of an inference pipeline, a unique name is automatically assigned based on the position of the `ContainerDefinition` in the pipeline\. If you specify a value for the `ContainerHostName` for any `ContainerDefinition` that is part of an inference pipeline, you must specify a value for the `ContainerHostName` parameter of every `ContainerDefinition` in that pipeline\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Environment`  <a name="cfn-sagemaker-model-containerdefinition-environment"></a>
The environment variables to set in the Docker container\. Each key and value in the `Environment` string to string map can have length of up to 1024\. We support up to 16 entries in the map\.   
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Image`  <a name="cfn-sagemaker-model-containerdefinition-image"></a>
The Amazon EC2 Container Registry \(Amazon ECR\) path where inference code is stored\. If you are using your own custom algorithm instead of an algorithm provided by Amazon SageMaker, the inference code must meet Amazon SageMaker requirements\. Amazon SageMaker supports both `registry/repository[:tag]` and `registry/repository[@digest]` image path formats\. For more information, see [Using Your Own Algorithms with Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/your-algorithms.html)   
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `[\S]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelDataUrl`  <a name="cfn-sagemaker-model-containerdefinition-modeldataurl"></a>
The S3 path where the model artifacts, which result from model training, are stored\. This path must point to a single gzip compressed tar archive \(\.tar\.gz suffix\)\. The S3 path is required for Amazon SageMaker built\-in algorithms, but not if you use your own algorithms\. For more information on built\-in algorithms, see [Common Parameters](http://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-algo-docker-registry-paths.html)\.   
If you provide a value for this parameter, Amazon SageMaker uses AWS Security Token Service to download model artifacts from the S3 path you provide\. AWS STS is activated in your IAM user account by default\. If you previously deactivated AWS STS for a region, you need to reactivate AWS STS for that region\. For more information, see [Activating and Deactivating AWS STS in an AWS Region](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp_enable-regions.html) in the *AWS Identity and Access Management User Guide*\.  
If you use a built\-in algorithm to create a model, Amazon SageMaker requires that you provide a S3 path to the model artifacts in `ModelDataUrl`\.
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
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
  "[ImageConfig](#cfn-sagemaker-model-containerdefinition-imageconfig)" : ImageConfig,
  "[InferenceSpecificationName](#cfn-sagemaker-model-containerdefinition-inferencespecificationname)" : String,
  "[Mode](#cfn-sagemaker-model-containerdefinition-mode)" : String,
  "[ModelDataUrl](#cfn-sagemaker-model-containerdefinition-modeldataurl)" : String,
  "[ModelPackageName](#cfn-sagemaker-model-containerdefinition-modelpackagename)" : String,
  "[MultiModelConfig](#cfn-sagemaker-model-containerdefinition-multimodelconfig)" : MultiModelConfig
}
```

### YAML<a name="aws-properties-sagemaker-model-containerdefinition-syntax.yaml"></a>

```
  [ContainerHostname](#cfn-sagemaker-model-containerdefinition-containerhostname): String
  [Environment](#cfn-sagemaker-model-containerdefinition-environment): Json
  [Image](#cfn-sagemaker-model-containerdefinition-image): String
  [ImageConfig](#cfn-sagemaker-model-containerdefinition-imageconfig): 
    ImageConfig
  [InferenceSpecificationName](#cfn-sagemaker-model-containerdefinition-inferencespecificationname): String
  [Mode](#cfn-sagemaker-model-containerdefinition-mode): String
  [ModelDataUrl](#cfn-sagemaker-model-containerdefinition-modeldataurl): String
  [ModelPackageName](#cfn-sagemaker-model-containerdefinition-modelpackagename): String
  [MultiModelConfig](#cfn-sagemaker-model-containerdefinition-multimodelconfig): 
    MultiModelConfig
```

## Properties<a name="aws-properties-sagemaker-model-containerdefinition-properties"></a>

`ContainerHostname`  <a name="cfn-sagemaker-model-containerdefinition-containerhostname"></a>
This parameter is ignored for models that contain only a `PrimaryContainer`\.  
When a `ContainerDefinition` is part of an inference pipeline, the value of the parameter uniquely identifies the container for the purposes of logging and metrics\. For information, see [Use Logs and Metrics to Monitor an Inference Pipeline](https://docs.aws.amazon.com/sagemaker/latest/dg/inference-pipeline-logs-metrics.html)\. If you don't specify a value for this parameter for a `ContainerDefinition` that is part of an inference pipeline, a unique name is automatically assigned based on the position of the `ContainerDefinition` in the pipeline\. If you specify a value for the `ContainerHostName` for any `ContainerDefinition` that is part of an inference pipeline, you must specify a value for the `ContainerHostName` parameter of every `ContainerDefinition` in that pipeline\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Environment`  <a name="cfn-sagemaker-model-containerdefinition-environment"></a>
The environment variables to set in the Docker container\. Each key and value in the `Environment` string to string map can have length of up to 1024\. We support up to 16 entries in the map\.   
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Image`  <a name="cfn-sagemaker-model-containerdefinition-image"></a>
The path where inference code is stored\. This can be either in Amazon EC2 Container Registry or in a Docker registry that is accessible from the same VPC that you configure for your endpoint\. If you are using your own custom algorithm instead of an algorithm provided by SageMaker, the inference code must meet SageMaker requirements\. SageMaker supports both `registry/repository[:tag]` and `registry/repository[@digest]` image path formats\. For more information, see [Using Your Own Algorithms with Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/your-algorithms.html)\.   
The model artifacts in an Amazon S3 bucket and the Docker image for inference container in Amazon EC2 Container Registry must be in the same region as the model or endpoint you are creating\.
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `[\S]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageConfig`  <a name="cfn-sagemaker-model-containerdefinition-imageconfig"></a>
Specifies whether the model container is in Amazon ECR or a private Docker registry accessible from your Amazon Virtual Private Cloud \(VPC\)\. For information about storing containers in a private Docker registry, see [Use a Private Docker Registry for Real\-Time Inference Containers](https://docs.aws.amazon.com/sagemaker/latest/dg/your-algorithms-containers-inference-private.html)\.   
The model artifacts in an Amazon S3 bucket and the Docker image for inference container in Amazon EC2 Container Registry must be in the same region as the model or endpoint you are creating\.
*Required*: No  
*Type*: [ImageConfig](aws-properties-sagemaker-model-containerdefinition-imageconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InferenceSpecificationName`  <a name="cfn-sagemaker-model-containerdefinition-inferencespecificationname"></a>
The inference specification name in the model package version\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Mode`  <a name="cfn-sagemaker-model-containerdefinition-mode"></a>
Whether the container hosts a single model or multiple models\.  
*Required*: No  
*Type*: String  
*Allowed values*: `MultiModel | SingleModel`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelDataUrl`  <a name="cfn-sagemaker-model-containerdefinition-modeldataurl"></a>
The S3 path where the model artifacts, which result from model training, are stored\. This path must point to a single gzip compressed tar archive \(\.tar\.gz suffix\)\. The S3 path is required for SageMaker built\-in algorithms, but not if you use your own algorithms\. For more information on built\-in algorithms, see [Common Parameters](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-algo-docker-registry-paths.html)\.   
The model artifacts must be in an S3 bucket that is in the same region as the model or endpoint you are creating\.
If you provide a value for this parameter, SageMaker uses AWS Security Token Service to download model artifacts from the S3 path you provide\. AWS STS is activated in your AWS account by default\. If you previously deactivated AWS STS for a region, you need to reactivate AWS STS for that region\. For more information, see [Activating and Deactivating AWS STS in an AWS Region](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp_enable-regions.html) in the * AWS Identity and Access Management User Guide*\.  
If you use a built\-in algorithm to create a model, SageMaker requires that you provide a S3 path to the model artifacts in `ModelDataUrl`\.
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPackageName`  <a name="cfn-sagemaker-model-containerdefinition-modelpackagename"></a>
The name or Amazon Resource Name \(ARN\) of the model package to use to create the model\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `176`  
*Pattern*: `(arn:aws[a-z\-]*:sagemaker:[a-z0-9\-]*:[0-9]{12}:[a-z\-]*\/)?([a-zA-Z0-9]([a-zA-Z0-9-]){0,62})(?<!-)(\/[0-9]{1,5})?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MultiModelConfig`  <a name="cfn-sagemaker-model-containerdefinition-multimodelconfig"></a>
Specifies additional configuration for multi\-model endpoints\.  
*Required*: No  
*Type*: [MultiModelConfig](aws-properties-sagemaker-model-containerdefinition-multimodelconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
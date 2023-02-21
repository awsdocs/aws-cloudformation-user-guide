# AWS::SageMaker::ModelPackage ModelPackageContainerDefinition<a name="aws-properties-sagemaker-modelpackage-modelpackagecontainerdefinition"></a>

Describes the Docker container for the model package\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-modelpackagecontainerdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-modelpackagecontainerdefinition-syntax.json"></a>

```
{
  "[ContainerHostname](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-containerhostname)" : String,
  "[Environment](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-environment)" : {Key : Value, ...},
  "[Framework](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-framework)" : String,
  "[FrameworkVersion](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-frameworkversion)" : String,
  "[Image](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-image)" : String,
  "[ImageDigest](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-imagedigest)" : String,
  "[ModelDataUrl](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-modeldataurl)" : String,
  "[ModelInput](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-modelinput)" : ModelInput,
  "[NearestModelName](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-nearestmodelname)" : String,
  "[ProductId](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-productid)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-modelpackagecontainerdefinition-syntax.yaml"></a>

```
  [ContainerHostname](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-containerhostname): String
  [Environment](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-environment): 
    Key : Value
  [Framework](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-framework): String
  [FrameworkVersion](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-frameworkversion): String
  [Image](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-image): String
  [ImageDigest](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-imagedigest): String
  [ModelDataUrl](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-modeldataurl): String
  [ModelInput](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-modelinput): 
    ModelInput
  [NearestModelName](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-nearestmodelname): String
  [ProductId](#cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-productid): String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-modelpackagecontainerdefinition-properties"></a>

`ContainerHostname`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-containerhostname"></a>
The DNS host name for the Docker container\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Environment`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-environment"></a>
The environment variables to set in the Docker container\. Each key and value in the `Environment` string to string map can have length of up to 1024\. We support up to 16 entries in the map\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Framework`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-framework"></a>
The machine learning framework of the model package container image\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`FrameworkVersion`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-frameworkversion"></a>
The framework version of the Model Package Container Image\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `10`  
*Pattern*: `[0-9]\.[A-Za-z0-9.-]+`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Image`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-image"></a>
The Amazon EC2 Container Registry \(Amazon ECR\) path where inference code is stored\.  
If you are using your own custom algorithm instead of an algorithm provided by SageMaker, the inference code must meet SageMaker requirements\. SageMaker supports both `registry/repository[:tag]` and `registry/repository[@digest]` image path formats\. For more information, see [Using Your Own Algorithms with Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/your-algorithms.html)\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `[\S]+`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`ImageDigest`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-imagedigest"></a>
An MD5 hash of the training algorithm that identifies the Docker image used for training\.  
*Required*: No  
*Type*: String  
*Maximum*: `72`  
*Pattern*: `^[Ss][Hh][Aa]256:[0-9a-fA-F]{64}$`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`ModelDataUrl`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-modeldataurl"></a>
The Amazon S3 path where the model artifacts, which result from model training, are stored\. This path must point to a single `gzip` compressed tar archive \(`.tar.gz` suffix\)\.  
The model artifacts must be in an S3 bucket that is in the same region as the model package\.
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`ModelInput`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-modelinput"></a>
A structure with Model Input details\.  
*Required*: No  
*Type*: [ModelInput](aws-properties-sagemaker-modelpackage-modelinput.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`NearestModelName`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-nearestmodelname"></a>
The name of a pre\-trained machine learning benchmarked by Amazon SageMaker Inference Recommender model that matches your model\. You can find a list of benchmarked models by calling `ListModelMetadata`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`ProductId`  <a name="cfn-sagemaker-modelpackage-modelpackagecontainerdefinition-productid"></a>
The AWS Marketplace product ID of the model package\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*$`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)
# AWS::SageMaker::ModelPackage InferenceSpecification<a name="aws-properties-sagemaker-modelpackage-inferencespecification"></a>

Defines how to perform inference generation after a training job is run\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-inferencespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-inferencespecification-syntax.json"></a>

```
{
  "[Containers](#cfn-sagemaker-modelpackage-inferencespecification-containers)" : [ ModelPackageContainerDefinition, ... ],
  "[SupportedContentTypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedcontenttypes)" : [ String, ... ],
  "[SupportedRealtimeInferenceInstanceTypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedrealtimeinferenceinstancetypes)" : [ String, ... ],
  "[SupportedResponseMIMETypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedresponsemimetypes)" : [ String, ... ],
  "[SupportedTransformInstanceTypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedtransforminstancetypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-inferencespecification-syntax.yaml"></a>

```
  [Containers](#cfn-sagemaker-modelpackage-inferencespecification-containers): 
    - ModelPackageContainerDefinition
  [SupportedContentTypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedcontenttypes): 
    - String
  [SupportedRealtimeInferenceInstanceTypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedrealtimeinferenceinstancetypes): 
    - String
  [SupportedResponseMIMETypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedresponsemimetypes): 
    - String
  [SupportedTransformInstanceTypes](#cfn-sagemaker-modelpackage-inferencespecification-supportedtransforminstancetypes): 
    - String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-inferencespecification-properties"></a>

`Containers`  <a name="cfn-sagemaker-modelpackage-inferencespecification-containers"></a>
The Amazon ECR registry path of the Docker image that contains the inference code\.  
*Required*: Yes  
*Type*: List of [ModelPackageContainerDefinition](aws-properties-sagemaker-modelpackage-modelpackagecontainerdefinition.md)  
*Maximum*: `15`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SupportedContentTypes`  <a name="cfn-sagemaker-modelpackage-inferencespecification-supportedcontenttypes"></a>
The supported MIME types for the input data\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SupportedRealtimeInferenceInstanceTypes`  <a name="cfn-sagemaker-modelpackage-inferencespecification-supportedrealtimeinferenceinstancetypes"></a>
A list of the instance types that are used to generate inferences in real\-time\.  
This parameter is required for unversioned models, and optional for versioned models\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SupportedResponseMIMETypes`  <a name="cfn-sagemaker-modelpackage-inferencespecification-supportedresponsemimetypes"></a>
The supported MIME types for the output data\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SupportedTransformInstanceTypes`  <a name="cfn-sagemaker-modelpackage-inferencespecification-supportedtransforminstancetypes"></a>
A list of the instance types on which a transformation job can be run or on which an endpoint can be deployed\.  
This parameter is required for unversioned models, and optional for versioned models\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
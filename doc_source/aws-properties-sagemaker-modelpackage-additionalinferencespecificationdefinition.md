# AWS::SageMaker::ModelPackage AdditionalInferenceSpecificationDefinition<a name="aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition"></a>

A structure of additional Inference Specification\. Additional Inference Specification specifies details about inference jobs that can be run with models based on this model package

## Syntax<a name="aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition-syntax.json"></a>

```
{
  "[Containers](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-containers)" : [ ModelPackageContainerDefinition, ... ],
  "[Description](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-description)" : String,
  "[Name](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-name)" : String,
  "[SupportedContentTypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedcontenttypes)" : [ String, ... ],
  "[SupportedRealtimeInferenceInstanceTypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedrealtimeinferenceinstancetypes)" : [ String, ... ],
  "[SupportedResponseMIMETypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedresponsemimetypes)" : [ String, ... ],
  "[SupportedTransformInstanceTypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedtransforminstancetypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition-syntax.yaml"></a>

```
  [Containers](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-containers): 
    - ModelPackageContainerDefinition
  [Description](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-description): String
  [Name](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-name): String
  [SupportedContentTypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedcontenttypes): 
    - String
  [SupportedRealtimeInferenceInstanceTypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedrealtimeinferenceinstancetypes): 
    - String
  [SupportedResponseMIMETypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedresponsemimetypes): 
    - String
  [SupportedTransformInstanceTypes](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedtransforminstancetypes): 
    - String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition-properties"></a>

`Containers`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-containers"></a>
The Amazon ECR registry path of the Docker image that contains the inference code\.  
*Required*: Yes  
*Type*: List of [ModelPackageContainerDefinition](aws-properties-sagemaker-modelpackage-modelpackagecontainerdefinition.md)  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-description"></a>
A description of the additional Inference specification  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-name"></a>
A unique name to identify the additional inference specification\. The name must be unique within the list of your additional inference specifications for a particular model package\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportedContentTypes`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedcontenttypes"></a>
The supported MIME types for the input data\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportedRealtimeInferenceInstanceTypes`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedrealtimeinferenceinstancetypes"></a>
A list of the instance types that are used to generate inferences in real\-time\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportedResponseMIMETypes`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedresponsemimetypes"></a>
The supported MIME types for the output data\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportedTransformInstanceTypes`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition-supportedtransforminstancetypes"></a>
A list of the instance types on which a transformation job can be run or on which an endpoint can be deployed\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
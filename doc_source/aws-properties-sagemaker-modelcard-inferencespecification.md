# AWS::SageMaker::ModelCard InferenceSpecification<a name="aws-properties-sagemaker-modelcard-inferencespecification"></a>

Defines how to perform inference generation after a training job is run\.

## Syntax<a name="aws-properties-sagemaker-modelcard-inferencespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-inferencespecification-syntax.json"></a>

```
{
  "[Containers](#cfn-sagemaker-modelcard-inferencespecification-containers)" : [ Container, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-inferencespecification-syntax.yaml"></a>

```
  [Containers](#cfn-sagemaker-modelcard-inferencespecification-containers): 
    - Container
```

## Properties<a name="aws-properties-sagemaker-modelcard-inferencespecification-properties"></a>

`Containers`  <a name="cfn-sagemaker-modelcard-inferencespecification-containers"></a>
The Amazon ECR registry path of the Docker image that contains the inference code\.  
*Required*: Yes  
*Type*: List of [Container](aws-properties-sagemaker-modelcard-container.md)  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
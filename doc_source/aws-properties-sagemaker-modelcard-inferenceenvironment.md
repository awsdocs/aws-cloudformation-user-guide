# AWS::SageMaker::ModelCard InferenceEnvironment<a name="aws-properties-sagemaker-modelcard-inferenceenvironment"></a>

An overview of a model's inference environment\.

## Syntax<a name="aws-properties-sagemaker-modelcard-inferenceenvironment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-inferenceenvironment-syntax.json"></a>

```
{
  "[ContainerImage](#cfn-sagemaker-modelcard-inferenceenvironment-containerimage)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-inferenceenvironment-syntax.yaml"></a>

```
  [ContainerImage](#cfn-sagemaker-modelcard-inferenceenvironment-containerimage): 
    - String
```

## Properties<a name="aws-properties-sagemaker-modelcard-inferenceenvironment-properties"></a>

`ContainerImage`  <a name="cfn-sagemaker-modelcard-inferenceenvironment-containerimage"></a>
The container used to run the inference environment\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
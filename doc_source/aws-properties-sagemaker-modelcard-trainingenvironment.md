# AWS::SageMaker::ModelCard TrainingEnvironment<a name="aws-properties-sagemaker-modelcard-trainingenvironment"></a>

SageMaker training image\.

## Syntax<a name="aws-properties-sagemaker-modelcard-trainingenvironment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-trainingenvironment-syntax.json"></a>

```
{
  "[ContainerImage](#cfn-sagemaker-modelcard-trainingenvironment-containerimage)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-trainingenvironment-syntax.yaml"></a>

```
  [ContainerImage](#cfn-sagemaker-modelcard-trainingenvironment-containerimage): 
    - String
```

## Properties<a name="aws-properties-sagemaker-modelcard-trainingenvironment-properties"></a>

`ContainerImage`  <a name="cfn-sagemaker-modelcard-trainingenvironment-containerimage"></a>
SageMaker inference image URI\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
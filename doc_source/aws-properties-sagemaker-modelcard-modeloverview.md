# AWS::SageMaker::ModelCard ModelOverview<a name="aws-properties-sagemaker-modelcard-modeloverview"></a>

An overview about the model\.

## Syntax<a name="aws-properties-sagemaker-modelcard-modeloverview-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-modeloverview-syntax.json"></a>

```
{
  "[AlgorithmType](#cfn-sagemaker-modelcard-modeloverview-algorithmtype)" : String,
  "[InferenceEnvironment](#cfn-sagemaker-modelcard-modeloverview-inferenceenvironment)" : InferenceEnvironment,
  "[ModelArtifact](#cfn-sagemaker-modelcard-modeloverview-modelartifact)" : [ String, ... ],
  "[ModelCreator](#cfn-sagemaker-modelcard-modeloverview-modelcreator)" : String,
  "[ModelDescription](#cfn-sagemaker-modelcard-modeloverview-modeldescription)" : String,
  "[ModelId](#cfn-sagemaker-modelcard-modeloverview-modelid)" : String,
  "[ModelName](#cfn-sagemaker-modelcard-modeloverview-modelname)" : String,
  "[ModelOwner](#cfn-sagemaker-modelcard-modeloverview-modelowner)" : String,
  "[ModelVersion](#cfn-sagemaker-modelcard-modeloverview-modelversion)" : Double,
  "[ProblemType](#cfn-sagemaker-modelcard-modeloverview-problemtype)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-modeloverview-syntax.yaml"></a>

```
  [AlgorithmType](#cfn-sagemaker-modelcard-modeloverview-algorithmtype): String
  [InferenceEnvironment](#cfn-sagemaker-modelcard-modeloverview-inferenceenvironment): 
    InferenceEnvironment
  [ModelArtifact](#cfn-sagemaker-modelcard-modeloverview-modelartifact): 
    - String
  [ModelCreator](#cfn-sagemaker-modelcard-modeloverview-modelcreator): String
  [ModelDescription](#cfn-sagemaker-modelcard-modeloverview-modeldescription): String
  [ModelId](#cfn-sagemaker-modelcard-modeloverview-modelid): String
  [ModelName](#cfn-sagemaker-modelcard-modeloverview-modelname): String
  [ModelOwner](#cfn-sagemaker-modelcard-modeloverview-modelowner): String
  [ModelVersion](#cfn-sagemaker-modelcard-modeloverview-modelversion): Double
  [ProblemType](#cfn-sagemaker-modelcard-modeloverview-problemtype): String
```

## Properties<a name="aws-properties-sagemaker-modelcard-modeloverview-properties"></a>

`AlgorithmType`  <a name="cfn-sagemaker-modelcard-modeloverview-algorithmtype"></a>
The algorithm used to solve the problem\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InferenceEnvironment`  <a name="cfn-sagemaker-modelcard-modeloverview-inferenceenvironment"></a>
An overview about model inference\.  
*Required*: No  
*Type*: [InferenceEnvironment](aws-properties-sagemaker-modelcard-inferenceenvironment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelArtifact`  <a name="cfn-sagemaker-modelcard-modeloverview-modelartifact"></a>
The location of the model artifact\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelCreator`  <a name="cfn-sagemaker-modelcard-modeloverview-modelcreator"></a>
The creator of the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelDescription`  <a name="cfn-sagemaker-modelcard-modeloverview-modeldescription"></a>
A description of the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelId`  <a name="cfn-sagemaker-modelcard-modeloverview-modelid"></a>
The SageMaker Model ARN or non\-SageMaker Model ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelName`  <a name="cfn-sagemaker-modelcard-modeloverview-modelname"></a>
The name of the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelOwner`  <a name="cfn-sagemaker-modelcard-modeloverview-modelowner"></a>
The owner of the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelVersion`  <a name="cfn-sagemaker-modelcard-modeloverview-modelversion"></a>
The version of the model\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProblemType`  <a name="cfn-sagemaker-modelcard-modeloverview-problemtype"></a>
The problem being solved with the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
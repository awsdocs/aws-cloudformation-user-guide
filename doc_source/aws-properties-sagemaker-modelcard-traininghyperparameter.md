# AWS::SageMaker::ModelCard TrainingHyperParameter<a name="aws-properties-sagemaker-modelcard-traininghyperparameter"></a>

A hyper parameter that was configured in training the model\.

## Syntax<a name="aws-properties-sagemaker-modelcard-traininghyperparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-traininghyperparameter-syntax.json"></a>

```
{
  "[Name](#cfn-sagemaker-modelcard-traininghyperparameter-name)" : String,
  "[Value](#cfn-sagemaker-modelcard-traininghyperparameter-value)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-traininghyperparameter-syntax.yaml"></a>

```
  [Name](#cfn-sagemaker-modelcard-traininghyperparameter-name): String
  [Value](#cfn-sagemaker-modelcard-traininghyperparameter-value): String
```

## Properties<a name="aws-properties-sagemaker-modelcard-traininghyperparameter-properties"></a>

`Name`  <a name="cfn-sagemaker-modelcard-traininghyperparameter-name"></a>
The name of the hyper parameter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-sagemaker-modelcard-traininghyperparameter-value"></a>
The value specified for the hyper parameter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
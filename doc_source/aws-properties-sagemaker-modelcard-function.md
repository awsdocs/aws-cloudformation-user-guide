# AWS::SageMaker::ModelCard Function<a name="aws-properties-sagemaker-modelcard-function"></a>

Function details\.

## Syntax<a name="aws-properties-sagemaker-modelcard-function-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-function-syntax.json"></a>

```
{
  "[Condition](#cfn-sagemaker-modelcard-function-condition)" : String,
  "[Facet](#cfn-sagemaker-modelcard-function-facet)" : String,
  "[Function](#cfn-sagemaker-modelcard-function-function)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-function-syntax.yaml"></a>

```
  [Condition](#cfn-sagemaker-modelcard-function-condition): String
  [Facet](#cfn-sagemaker-modelcard-function-facet): String
  [Function](#cfn-sagemaker-modelcard-function-function): String
```

## Properties<a name="aws-properties-sagemaker-modelcard-function-properties"></a>

`Condition`  <a name="cfn-sagemaker-modelcard-function-condition"></a>
An optional description of any conditions of your objective function metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Facet`  <a name="cfn-sagemaker-modelcard-function-facet"></a>
The metric of the model's objective function\. For example, *loss* or *rmse*\. The following list shows examples of the values that you can specify for the metric:  
+ `ACCURACY`
+ `AUC`
+ `LOSS`
+ `MAE`
+ `RMSE`
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Function`  <a name="cfn-sagemaker-modelcard-function-function"></a>
The optimization direction of the model's objective function\. You must specify one of the following values:  
+ `Maximize`
+ `Minimize`
*Required*: No  
*Type*: [String](#aws-properties-sagemaker-modelcard-function)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
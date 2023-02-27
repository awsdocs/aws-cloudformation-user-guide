# AWS::SageMaker::ModelCard ObjectiveFunction<a name="aws-properties-sagemaker-modelcard-objectivefunction"></a>

The function that is optimized during model training\.

## Syntax<a name="aws-properties-sagemaker-modelcard-objectivefunction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-objectivefunction-syntax.json"></a>

```
{
  "[Function](#cfn-sagemaker-modelcard-objectivefunction-function)" : Function,
  "[Notes](#cfn-sagemaker-modelcard-objectivefunction-notes)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-objectivefunction-syntax.yaml"></a>

```
  [Function](#cfn-sagemaker-modelcard-objectivefunction-function): 
    Function
  [Notes](#cfn-sagemaker-modelcard-objectivefunction-notes): String
```

## Properties<a name="aws-properties-sagemaker-modelcard-objectivefunction-properties"></a>

`Function`  <a name="cfn-sagemaker-modelcard-objectivefunction-function"></a>
A function object that details optimization direction, metric, and additional descriptions\.  
*Required*: No  
*Type*: [Function](aws-properties-sagemaker-modelcard-function.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Notes`  <a name="cfn-sagemaker-modelcard-objectivefunction-notes"></a>
Notes about the object function, including other considerations for possible objective functions\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
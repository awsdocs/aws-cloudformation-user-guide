# AWS::SageMaker::ModelCard BusinessDetails<a name="aws-properties-sagemaker-modelcard-businessdetails"></a>

Information about how the model supports business goals\.

## Syntax<a name="aws-properties-sagemaker-modelcard-businessdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-businessdetails-syntax.json"></a>

```
{
  "[BusinessProblem](#cfn-sagemaker-modelcard-businessdetails-businessproblem)" : String,
  "[BusinessStakeholders](#cfn-sagemaker-modelcard-businessdetails-businessstakeholders)" : String,
  "[LineOfBusiness](#cfn-sagemaker-modelcard-businessdetails-lineofbusiness)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-businessdetails-syntax.yaml"></a>

```
  [BusinessProblem](#cfn-sagemaker-modelcard-businessdetails-businessproblem): String
  [BusinessStakeholders](#cfn-sagemaker-modelcard-businessdetails-businessstakeholders): String
  [LineOfBusiness](#cfn-sagemaker-modelcard-businessdetails-lineofbusiness): String
```

## Properties<a name="aws-properties-sagemaker-modelcard-businessdetails-properties"></a>

`BusinessProblem`  <a name="cfn-sagemaker-modelcard-businessdetails-businessproblem"></a>
The specific business problem that the model is trying to solve\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BusinessStakeholders`  <a name="cfn-sagemaker-modelcard-businessdetails-businessstakeholders"></a>
The relevant stakeholders for the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineOfBusiness`  <a name="cfn-sagemaker-modelcard-businessdetails-lineofbusiness"></a>
The broader business need that the model is serving\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
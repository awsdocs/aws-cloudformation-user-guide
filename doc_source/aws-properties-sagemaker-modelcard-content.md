# AWS::SageMaker::ModelCard Content<a name="aws-properties-sagemaker-modelcard-content"></a>

The content of the model card\. It follows the [model card json schema](https://docs.aws.amazon.com/sagemaker/latest/dg/model-cards.html#model-cards-json-schema)\.

## Syntax<a name="aws-properties-sagemaker-modelcard-content-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-content-syntax.json"></a>

```
{
  "[AdditionalInformation](#cfn-sagemaker-modelcard-content-additionalinformation)" : AdditionalInformation,
  "[BusinessDetails](#cfn-sagemaker-modelcard-content-businessdetails)" : BusinessDetails,
  "[EvaluationDetails](#cfn-sagemaker-modelcard-content-evaluationdetails)" : [ EvaluationDetail, ... ],
  "[IntendedUses](#cfn-sagemaker-modelcard-content-intendeduses)" : IntendedUses,
  "[ModelOverview](#cfn-sagemaker-modelcard-content-modeloverview)" : ModelOverview,
  "[TrainingDetails](#cfn-sagemaker-modelcard-content-trainingdetails)" : TrainingDetails
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-content-syntax.yaml"></a>

```
  [AdditionalInformation](#cfn-sagemaker-modelcard-content-additionalinformation): 
    AdditionalInformation
  [BusinessDetails](#cfn-sagemaker-modelcard-content-businessdetails): 
    BusinessDetails
  [EvaluationDetails](#cfn-sagemaker-modelcard-content-evaluationdetails): 
    - EvaluationDetail
  [IntendedUses](#cfn-sagemaker-modelcard-content-intendeduses): 
    IntendedUses
  [ModelOverview](#cfn-sagemaker-modelcard-content-modeloverview): 
    ModelOverview
  [TrainingDetails](#cfn-sagemaker-modelcard-content-trainingdetails): 
    TrainingDetails
```

## Properties<a name="aws-properties-sagemaker-modelcard-content-properties"></a>

`AdditionalInformation`  <a name="cfn-sagemaker-modelcard-content-additionalinformation"></a>
Additional information about the model\.  
*Required*: No  
*Type*: [AdditionalInformation](aws-properties-sagemaker-modelcard-additionalinformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BusinessDetails`  <a name="cfn-sagemaker-modelcard-content-businessdetails"></a>
Information about how the model supports business goals\.  
*Required*: No  
*Type*: [BusinessDetails](aws-properties-sagemaker-modelcard-businessdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EvaluationDetails`  <a name="cfn-sagemaker-modelcard-content-evaluationdetails"></a>
An overview about the model's evaluation\.  
*Required*: No  
*Type*: List of [EvaluationDetail](aws-properties-sagemaker-modelcard-evaluationdetail.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntendedUses`  <a name="cfn-sagemaker-modelcard-content-intendeduses"></a>
The intended usage of the model\.  
*Required*: No  
*Type*: [IntendedUses](aws-properties-sagemaker-modelcard-intendeduses.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelOverview`  <a name="cfn-sagemaker-modelcard-content-modeloverview"></a>
An overview about the model  
*Required*: No  
*Type*: [ModelOverview](aws-properties-sagemaker-modelcard-modeloverview.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrainingDetails`  <a name="cfn-sagemaker-modelcard-content-trainingdetails"></a>
An overview about model training\.  
*Required*: No  
*Type*: [TrainingDetails](aws-properties-sagemaker-modelcard-trainingdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
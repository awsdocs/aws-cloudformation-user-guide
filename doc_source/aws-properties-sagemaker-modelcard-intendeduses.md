# AWS::SageMaker::ModelCard IntendedUses<a name="aws-properties-sagemaker-modelcard-intendeduses"></a>

The intended uses of a model\.

## Syntax<a name="aws-properties-sagemaker-modelcard-intendeduses-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelcard-intendeduses-syntax.json"></a>

```
{
  "[ExplanationsForRiskRating](#cfn-sagemaker-modelcard-intendeduses-explanationsforriskrating)" : String,
  "[FactorsAffectingModelEfficiency](#cfn-sagemaker-modelcard-intendeduses-factorsaffectingmodelefficiency)" : String,
  "[IntendedUses](#cfn-sagemaker-modelcard-intendeduses-intendeduses)" : String,
  "[PurposeOfModel](#cfn-sagemaker-modelcard-intendeduses-purposeofmodel)" : String,
  "[RiskRating](#cfn-sagemaker-modelcard-intendeduses-riskrating)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelcard-intendeduses-syntax.yaml"></a>

```
  [ExplanationsForRiskRating](#cfn-sagemaker-modelcard-intendeduses-explanationsforriskrating): String
  [FactorsAffectingModelEfficiency](#cfn-sagemaker-modelcard-intendeduses-factorsaffectingmodelefficiency): String
  [IntendedUses](#cfn-sagemaker-modelcard-intendeduses-intendeduses): String
  [PurposeOfModel](#cfn-sagemaker-modelcard-intendeduses-purposeofmodel): String
  [RiskRating](#cfn-sagemaker-modelcard-intendeduses-riskrating): String
```

## Properties<a name="aws-properties-sagemaker-modelcard-intendeduses-properties"></a>

`ExplanationsForRiskRating`  <a name="cfn-sagemaker-modelcard-intendeduses-explanationsforriskrating"></a>
An explanation of why your organization categorizes the model with its risk rating\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FactorsAffectingModelEfficiency`  <a name="cfn-sagemaker-modelcard-intendeduses-factorsaffectingmodelefficiency"></a>
Factors affecting model efficacy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntendedUses`  <a name="cfn-sagemaker-modelcard-intendeduses-intendeduses"></a>
The intended use cases for the model\.  
*Required*: No  
*Type*: [String](#aws-properties-sagemaker-modelcard-intendeduses)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PurposeOfModel`  <a name="cfn-sagemaker-modelcard-intendeduses-purposeofmodel"></a>
The general purpose of the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RiskRating`  <a name="cfn-sagemaker-modelcard-intendeduses-riskrating"></a>
Your organization's risk rating\. You can specify one the following values as the risk rating:  
+ High
+ Medium
+ Low
+ Unknown
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Connect::EvaluationForm EvaluationFormSingleSelectQuestionAutomation<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomation"></a>

Information about the automation configuration in single select questions\. Automation options are evaluated in order, and the first matched option is applied\. If no automation option matches, and there is a default option, then the default option is applied\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomation-syntax.json"></a>

```
{
  "[DefaultOptionRefId](#cfn-connect-evaluationform-evaluationformsingleselectquestionautomation-defaultoptionrefid)" : String,
  "[Options](#cfn-connect-evaluationform-evaluationformsingleselectquestionautomation-options)" : [ EvaluationFormSingleSelectQuestionAutomationOption, ... ]
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomation-syntax.yaml"></a>

```
  [DefaultOptionRefId](#cfn-connect-evaluationform-evaluationformsingleselectquestionautomation-defaultoptionrefid): String
  [Options](#cfn-connect-evaluationform-evaluationformsingleselectquestionautomation-options): 
    - EvaluationFormSingleSelectQuestionAutomationOption
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomation-properties"></a>

`DefaultOptionRefId`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionautomation-defaultoptionrefid"></a>
The identifier of the default answer option, when none of the automation options match the criteria\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 40\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionautomation-options"></a>
The automation options of the single select question\.  
*Minimum*: 1  
*Maximum*: 20  
*Required*: Yes  
*Type*: List of [EvaluationFormSingleSelectQuestionAutomationOption](aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomationoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
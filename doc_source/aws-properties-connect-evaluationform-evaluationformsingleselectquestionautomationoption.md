# AWS::Connect::EvaluationForm EvaluationFormSingleSelectQuestionAutomationOption<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomationoption"></a>

The automation options of the single select question\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomationoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomationoption-syntax.json"></a>

```
{
  "[RuleCategory](#cfn-connect-evaluationform-evaluationformsingleselectquestionautomationoption-rulecategory)" : SingleSelectQuestionRuleCategoryAutomation
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomationoption-syntax.yaml"></a>

```
  [RuleCategory](#cfn-connect-evaluationform-evaluationformsingleselectquestionautomationoption-rulecategory): 
    SingleSelectQuestionRuleCategoryAutomation
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomationoption-properties"></a>

`RuleCategory`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionautomationoption-rulecategory"></a>
The automation option based on a rule category for the single select question\.  
*Required*: Yes  
*Type*: [SingleSelectQuestionRuleCategoryAutomation](aws-properties-connect-evaluationform-singleselectquestionrulecategoryautomation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
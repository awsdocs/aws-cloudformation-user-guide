# AWS::Connect::EvaluationForm SingleSelectQuestionRuleCategoryAutomation<a name="aws-properties-connect-evaluationform-singleselectquestionrulecategoryautomation"></a>

Information about the automation option based on a rule category for a single select question\.

*Length Constraints*: Minimum length of 1\. Maximum length of 50\.

## Syntax<a name="aws-properties-connect-evaluationform-singleselectquestionrulecategoryautomation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-singleselectquestionrulecategoryautomation-syntax.json"></a>

```
{
  "[Category](#cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-category)" : String,
  "[Condition](#cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-condition)" : String,
  "[OptionRefId](#cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-optionrefid)" : String
}
```

### YAML<a name="aws-properties-connect-evaluationform-singleselectquestionrulecategoryautomation-syntax.yaml"></a>

```
  [Category](#cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-category): String
  [Condition](#cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-condition): String
  [OptionRefId](#cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-optionrefid): String
```

## Properties<a name="aws-properties-connect-evaluationform-singleselectquestionrulecategoryautomation-properties"></a>

`Category`  <a name="cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-category"></a>
The category name, as defined in Rules\.  
*Minimum*: 1  
*Maximum*: 50  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Condition`  <a name="cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-condition"></a>
The condition to apply for the automation option\. If the condition is PRESENT, then the option is applied when the contact data includes the category\. Similarly, if the condition is NOT\_PRESENT, then the option is applied when the contact data does not include the category\.  
*Allowed values*: `PRESENT` \| `NOT_PRESENT`  
*Maximum*: 50  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionRefId`  <a name="cfn-connect-evaluationform-singleselectquestionrulecategoryautomation-optionrefid"></a>
The identifier of the answer option\. An identifier must be unique within the question\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 40\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
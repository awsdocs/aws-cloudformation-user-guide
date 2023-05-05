# AWS::Connect::EvaluationForm EvaluationFormSingleSelectQuestionProperties<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionproperties"></a>

Information about the options in single select questions\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionproperties-syntax.json"></a>

```
{
  "[Automation](#cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-automation)" : EvaluationFormSingleSelectQuestionAutomation,
  "[DisplayAs](#cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-displayas)" : String,
  "[Options](#cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-options)" : [ EvaluationFormSingleSelectQuestionOption, ... ]
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionproperties-syntax.yaml"></a>

```
  [Automation](#cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-automation): 
    EvaluationFormSingleSelectQuestionAutomation
  [DisplayAs](#cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-displayas): String
  [Options](#cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-options): 
    - EvaluationFormSingleSelectQuestionOption
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionproperties-properties"></a>

`Automation`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-automation"></a>
The display mode of the single select question\.  
*Required*: No  
*Type*: [EvaluationFormSingleSelectQuestionAutomation](aws-properties-connect-evaluationform-evaluationformsingleselectquestionautomation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayAs`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-displayas"></a>
The display mode of the single select question\.  
*Allowed values*: `DROPDOWN` \| `RADIO`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionproperties-options"></a>
The answer options of the single select question\.  
*Minimum*: 2  
*Maximum*: 256  
*Required*: Yes  
*Type*: List of [EvaluationFormSingleSelectQuestionOption](aws-properties-connect-evaluationform-evaluationformsingleselectquestionoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
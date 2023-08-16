# AWS::Connect::EvaluationForm EvaluationFormNumericQuestionProperties<a name="aws-properties-connect-evaluationform-evaluationformnumericquestionproperties"></a>

Information about properties for a numeric question in an evaluation form\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformnumericquestionproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformnumericquestionproperties-syntax.json"></a>

```
{
  "[Automation](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-automation)" : EvaluationFormNumericQuestionAutomation,
  "[MaxValue](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-maxvalue)" : Integer,
  "[MinValue](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-minvalue)" : Integer,
  "[Options](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-options)" : [ EvaluationFormNumericQuestionOption, ... ]
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformnumericquestionproperties-syntax.yaml"></a>

```
  [Automation](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-automation): 
    EvaluationFormNumericQuestionAutomation
  [MaxValue](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-maxvalue): Integer
  [MinValue](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-minvalue): Integer
  [Options](#cfn-connect-evaluationform-evaluationformnumericquestionproperties-options): 
    - EvaluationFormNumericQuestionOption
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformnumericquestionproperties-properties"></a>

`Automation`  <a name="cfn-connect-evaluationform-evaluationformnumericquestionproperties-automation"></a>
The automation properties of the numeric question\.  
*Required*: No  
*Type*: [EvaluationFormNumericQuestionAutomation](aws-properties-connect-evaluationform-evaluationformnumericquestionautomation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxValue`  <a name="cfn-connect-evaluationform-evaluationformnumericquestionproperties-maxvalue"></a>
The maximum answer value\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinValue`  <a name="cfn-connect-evaluationform-evaluationformnumericquestionproperties-minvalue"></a>
The minimum answer value\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-connect-evaluationform-evaluationformnumericquestionproperties-options"></a>
The scoring options of the numeric question\.  
*Required*: No  
*Type*: List of [EvaluationFormNumericQuestionOption](aws-properties-connect-evaluationform-evaluationformnumericquestionoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
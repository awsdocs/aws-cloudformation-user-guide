# AWS::Connect::EvaluationForm EvaluationFormQuestionTypeProperties<a name="aws-properties-connect-evaluationform-evaluationformquestiontypeproperties"></a>

Information about properties for a question in an evaluation form\. The question type properties must be either for a numeric question or a single select question\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformquestiontypeproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformquestiontypeproperties-syntax.json"></a>

```
{
  "[Numeric](#cfn-connect-evaluationform-evaluationformquestiontypeproperties-numeric)" : EvaluationFormNumericQuestionProperties,
  "[SingleSelect](#cfn-connect-evaluationform-evaluationformquestiontypeproperties-singleselect)" : EvaluationFormSingleSelectQuestionProperties
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformquestiontypeproperties-syntax.yaml"></a>

```
  [Numeric](#cfn-connect-evaluationform-evaluationformquestiontypeproperties-numeric): 
    EvaluationFormNumericQuestionProperties
  [SingleSelect](#cfn-connect-evaluationform-evaluationformquestiontypeproperties-singleselect): 
    EvaluationFormSingleSelectQuestionProperties
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformquestiontypeproperties-properties"></a>

`Numeric`  <a name="cfn-connect-evaluationform-evaluationformquestiontypeproperties-numeric"></a>
The properties of the numeric question\.  
*Required*: No  
*Type*: [EvaluationFormNumericQuestionProperties](aws-properties-connect-evaluationform-evaluationformnumericquestionproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleSelect`  <a name="cfn-connect-evaluationform-evaluationformquestiontypeproperties-singleselect"></a>
The properties of the numeric question\.  
*Required*: No  
*Type*: [EvaluationFormSingleSelectQuestionProperties](aws-properties-connect-evaluationform-evaluationformsingleselectquestionproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
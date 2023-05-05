# AWS::Connect::EvaluationForm EvaluationFormQuestion<a name="aws-properties-connect-evaluationform-evaluationformquestion"></a>

Information about a question from an evaluation form\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformquestion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformquestion-syntax.json"></a>

```
{
  "[Instructions](#cfn-connect-evaluationform-evaluationformquestion-instructions)" : String,
  "[NotApplicableEnabled](#cfn-connect-evaluationform-evaluationformquestion-notapplicableenabled)" : Boolean,
  "[QuestionType](#cfn-connect-evaluationform-evaluationformquestion-questiontype)" : String,
  "[QuestionTypeProperties](#cfn-connect-evaluationform-evaluationformquestion-questiontypeproperties)" : EvaluationFormQuestionTypeProperties,
  "[RefId](#cfn-connect-evaluationform-evaluationformquestion-refid)" : String,
  "[Title](#cfn-connect-evaluationform-evaluationformquestion-title)" : String,
  "[Weight](#cfn-connect-evaluationform-evaluationformquestion-weight)" : Double
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformquestion-syntax.yaml"></a>

```
  [Instructions](#cfn-connect-evaluationform-evaluationformquestion-instructions): String
  [NotApplicableEnabled](#cfn-connect-evaluationform-evaluationformquestion-notapplicableenabled): Boolean
  [QuestionType](#cfn-connect-evaluationform-evaluationformquestion-questiontype): String
  [QuestionTypeProperties](#cfn-connect-evaluationform-evaluationformquestion-questiontypeproperties): 
    EvaluationFormQuestionTypeProperties
  [RefId](#cfn-connect-evaluationform-evaluationformquestion-refid): String
  [Title](#cfn-connect-evaluationform-evaluationformquestion-title): String
  [Weight](#cfn-connect-evaluationform-evaluationformquestion-weight): Double
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformquestion-properties"></a>

`Instructions`  <a name="cfn-connect-evaluationform-evaluationformquestion-instructions"></a>
The instructions of the section\.  
*Length Constraints*: Minimum length of 0\. Maximum length of 1024\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotApplicableEnabled`  <a name="cfn-connect-evaluationform-evaluationformquestion-notapplicableenabled"></a>
The flag to enable not applicable answers to the question\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QuestionType`  <a name="cfn-connect-evaluationform-evaluationformquestion-questiontype"></a>
The type of the question\.  
*Allowed values*: `NUMERIC` \| `SINGLESELECT` \| `TEXT`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QuestionTypeProperties`  <a name="cfn-connect-evaluationform-evaluationformquestion-questiontypeproperties"></a>
The properties of the type of question\. Text questions do not have to define question type properties\.  
*Required*: No  
*Type*: [EvaluationFormQuestionTypeProperties](aws-properties-connect-evaluationform-evaluationformquestiontypeproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefId`  <a name="cfn-connect-evaluationform-evaluationformquestion-refid"></a>
The identifier of the question\. An identifier must be unique within the evaluation form\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 40\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-connect-evaluationform-evaluationformquestion-title"></a>
The title of the question\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 350\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-connect-evaluationform-evaluationformquestion-weight"></a>
The scoring weight of the section\.  
*Minimum*: 0  
*Maximum*: 100  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
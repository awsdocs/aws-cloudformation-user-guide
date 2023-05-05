# AWS::Connect::EvaluationForm EvaluationFormSingleSelectQuestionOption<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionoption"></a>

Information about the automation configuration in single select questions\.

## Syntax<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionoption-syntax.json"></a>

```
{
  "[AutomaticFail](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-automaticfail)" : Boolean,
  "[RefId](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-refid)" : String,
  "[Score](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-score)" : Integer,
  "[Text](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-text)" : String
}
```

### YAML<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionoption-syntax.yaml"></a>

```
  [AutomaticFail](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-automaticfail): Boolean
  [RefId](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-refid): String
  [Score](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-score): Integer
  [Text](#cfn-connect-evaluationform-evaluationformsingleselectquestionoption-text): String
```

## Properties<a name="aws-properties-connect-evaluationform-evaluationformsingleselectquestionoption-properties"></a>

`AutomaticFail`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionoption-automaticfail"></a>
The flag to mark the option as automatic fail\. If an automatic fail answer is provided, the overall evaluation gets a score of 0\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefId`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionoption-refid"></a>
The identifier of the answer option\. An identifier must be unique within the question\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 40\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Score`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionoption-score"></a>
The score assigned to the answer option\.  
*Minimum*: 0  
*Maximum*: 10  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Text`  <a name="cfn-connect-evaluationform-evaluationformsingleselectquestionoption-text"></a>
The title of the answer option\.  
*Length Constraints*: Minimum length of 1\. Maximum length of 128\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
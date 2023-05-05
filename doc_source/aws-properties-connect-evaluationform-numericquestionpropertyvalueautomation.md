# AWS::Connect::EvaluationForm NumericQuestionPropertyValueAutomation<a name="aws-properties-connect-evaluationform-numericquestionpropertyvalueautomation"></a>

Information about the property value used in automation of a numeric questions\.

## Syntax<a name="aws-properties-connect-evaluationform-numericquestionpropertyvalueautomation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-evaluationform-numericquestionpropertyvalueautomation-syntax.json"></a>

```
{
  "[Label](#cfn-connect-evaluationform-numericquestionpropertyvalueautomation-label)" : String
}
```

### YAML<a name="aws-properties-connect-evaluationform-numericquestionpropertyvalueautomation-syntax.yaml"></a>

```
  [Label](#cfn-connect-evaluationform-numericquestionpropertyvalueautomation-label): String
```

## Properties<a name="aws-properties-connect-evaluationform-numericquestionpropertyvalueautomation-properties"></a>

`Label`  <a name="cfn-connect-evaluationform-numericquestionpropertyvalueautomation-label"></a>
The property label of the automation\.  
*Allowed values*:` OVERALL_CUSTOMER_SENTIMENT_SCORE`, `OVERALL_AGENT_SENTIMENT_SCORE` \| `NON_TALK_TIME` \| `NON_TALK_TIME_PERCENTAGE` \| `NUMBER_OF_INTERRUPTIONS` \| `CONTACT_DURATION` \| `AGENT_INTERACTION_DURATION` \| `CUSTOMER_HOLD_TIME`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
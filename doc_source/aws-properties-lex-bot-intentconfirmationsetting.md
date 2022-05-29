# AWS::Lex::Bot IntentConfirmationSetting<a name="aws-properties-lex-bot-intentconfirmationsetting"></a>

Provides a prompt for making sure that the user is ready for the intent to be fulfilled\.

## Syntax<a name="aws-properties-lex-bot-intentconfirmationsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-intentconfirmationsetting-syntax.json"></a>

```
{
  "[DeclinationResponse](#cfn-lex-bot-intentconfirmationsetting-declinationresponse)" : ResponseSpecification,
  "[IsActive](#cfn-lex-bot-intentconfirmationsetting-isactive)" : Boolean,
  "[PromptSpecification](#cfn-lex-bot-intentconfirmationsetting-promptspecification)" : PromptSpecification
}
```

### YAML<a name="aws-properties-lex-bot-intentconfirmationsetting-syntax.yaml"></a>

```
  [DeclinationResponse](#cfn-lex-bot-intentconfirmationsetting-declinationresponse): 
    ResponseSpecification
  [IsActive](#cfn-lex-bot-intentconfirmationsetting-isactive): Boolean
  [PromptSpecification](#cfn-lex-bot-intentconfirmationsetting-promptspecification): 
    PromptSpecification
```

## Properties<a name="aws-properties-lex-bot-intentconfirmationsetting-properties"></a>

`DeclinationResponse`  <a name="cfn-lex-bot-intentconfirmationsetting-declinationresponse"></a>
When the user answers "no" to the question defined in PromptSpecification, Amazon Lex responds with this response to acknowledge that the intent was canceled\.  
*Required*: Yes  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-intentconfirmationsetting-isactive"></a>
Specifies whether the intent's confirmation is sent to the user\. When this field is false, confirmation and declination responses aren't sent and processing continues as if the responses aren't present\. If the active field isn't specified, the default is true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PromptSpecification`  <a name="cfn-lex-bot-intentconfirmationsetting-promptspecification"></a>
Prompts the user to confirm the intent\. This question should have a yes or no answer\.  
*Required*: Yes  
*Type*: [PromptSpecification](aws-properties-lex-bot-promptspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
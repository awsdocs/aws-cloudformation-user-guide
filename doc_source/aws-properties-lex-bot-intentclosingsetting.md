# AWS::Lex::Bot IntentClosingSetting<a name="aws-properties-lex-bot-intentclosingsetting"></a>

Provides a statement the Amazon Lex conveys to the user when the intent is successfully fulfilled\.

## Syntax<a name="aws-properties-lex-bot-intentclosingsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-intentclosingsetting-syntax.json"></a>

```
{
  "[ClosingResponse](#cfn-lex-bot-intentclosingsetting-closingresponse)" : ResponseSpecification,
  "[Conditional](#cfn-lex-bot-intentclosingsetting-conditional)" : ConditionalSpecification,
  "[IsActive](#cfn-lex-bot-intentclosingsetting-isactive)" : Boolean,
  "[NextStep](#cfn-lex-bot-intentclosingsetting-nextstep)" : DialogState
}
```

### YAML<a name="aws-properties-lex-bot-intentclosingsetting-syntax.yaml"></a>

```
  [ClosingResponse](#cfn-lex-bot-intentclosingsetting-closingresponse): 
    ResponseSpecification
  [Conditional](#cfn-lex-bot-intentclosingsetting-conditional): 
    ConditionalSpecification
  [IsActive](#cfn-lex-bot-intentclosingsetting-isactive): Boolean
  [NextStep](#cfn-lex-bot-intentclosingsetting-nextstep): 
    DialogState
```

## Properties<a name="aws-properties-lex-bot-intentclosingsetting-properties"></a>

`ClosingResponse`  <a name="cfn-lex-bot-intentclosingsetting-closingresponse"></a>
The response that Amazon Lex sends to the user when the intent is complete\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Conditional`  <a name="cfn-lex-bot-intentclosingsetting-conditional"></a>
A list of conditional branches associated with the intent's closing response\. These branches are executed when the `nextStep` attribute is set to `EvalutateConditional`\.  
*Required*: No  
*Type*: [ConditionalSpecification](aws-properties-lex-bot-conditionalspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-intentclosingsetting-isactive"></a>
Specifies whether an intent's closing response is used\. When this field is false, the closing response isn't sent to the user\. If the `IsActive` field isn't specified, the default is true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextStep`  <a name="cfn-lex-bot-intentclosingsetting-nextstep"></a>
Specifies the next step that the bot executes after playing the intent's closing response\.  
*Required*: No  
*Type*: [DialogState](aws-properties-lex-bot-dialogstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Lex::Bot DialogCodeHookInvocationSetting<a name="aws-properties-lex-bot-dialogcodehookinvocationsetting"></a>

Settings that specify the dialog code hook that is called by Amazon Lex at a step of the conversation\. 

## Syntax<a name="aws-properties-lex-bot-dialogcodehookinvocationsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-dialogcodehookinvocationsetting-syntax.json"></a>

```
{
  "[EnableCodeHookInvocation](#cfn-lex-bot-dialogcodehookinvocationsetting-enablecodehookinvocation)" : Boolean,
  "[InvocationLabel](#cfn-lex-bot-dialogcodehookinvocationsetting-invocationlabel)" : String,
  "[IsActive](#cfn-lex-bot-dialogcodehookinvocationsetting-isactive)" : Boolean,
  "[PostCodeHookSpecification](#cfn-lex-bot-dialogcodehookinvocationsetting-postcodehookspecification)" : PostDialogCodeHookInvocationSpecification
}
```

### YAML<a name="aws-properties-lex-bot-dialogcodehookinvocationsetting-syntax.yaml"></a>

```
  [EnableCodeHookInvocation](#cfn-lex-bot-dialogcodehookinvocationsetting-enablecodehookinvocation): Boolean
  [InvocationLabel](#cfn-lex-bot-dialogcodehookinvocationsetting-invocationlabel): String
  [IsActive](#cfn-lex-bot-dialogcodehookinvocationsetting-isactive): Boolean
  [PostCodeHookSpecification](#cfn-lex-bot-dialogcodehookinvocationsetting-postcodehookspecification): 
    PostDialogCodeHookInvocationSpecification
```

## Properties<a name="aws-properties-lex-bot-dialogcodehookinvocationsetting-properties"></a>

`EnableCodeHookInvocation`  <a name="cfn-lex-bot-dialogcodehookinvocationsetting-enablecodehookinvocation"></a>
Indicates whether a Lambda function should be invoked for the dialog\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationLabel`  <a name="cfn-lex-bot-dialogcodehookinvocationsetting-invocationlabel"></a>
A label that indicates the dialog step from which the dialog code hook is happening\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-dialogcodehookinvocationsetting-isactive"></a>
Determines whether a dialog code hook is used when the intent is activated\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostCodeHookSpecification`  <a name="cfn-lex-bot-dialogcodehookinvocationsetting-postcodehookspecification"></a>
Contains the responses and actions that Amazon Lex takes after the Lambda function is complete\.  
*Required*: Yes  
*Type*: [PostDialogCodeHookInvocationSpecification](aws-properties-lex-bot-postdialogcodehookinvocationspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Lex::Bot DialogState<a name="aws-properties-lex-bot-dialogstate"></a>

The current state of the conversation with the user\.

## Syntax<a name="aws-properties-lex-bot-dialogstate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-dialogstate-syntax.json"></a>

```
{
  "[DialogAction](#cfn-lex-bot-dialogstate-dialogaction)" : DialogAction,
  "[Intent](#cfn-lex-bot-dialogstate-intent)" : IntentOverride,
  "[SessionAttributes](#cfn-lex-bot-dialogstate-sessionattributes)" : [ SessionAttribute, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-dialogstate-syntax.yaml"></a>

```
  [DialogAction](#cfn-lex-bot-dialogstate-dialogaction): 
    DialogAction
  [Intent](#cfn-lex-bot-dialogstate-intent): 
    IntentOverride
  [SessionAttributes](#cfn-lex-bot-dialogstate-sessionattributes): 
    - SessionAttribute
```

## Properties<a name="aws-properties-lex-bot-dialogstate-properties"></a>

`DialogAction`  <a name="cfn-lex-bot-dialogstate-dialogaction"></a>
Defines the action that the bot executes at runtime when the conversation reaches this step\.  
*Required*: No  
*Type*: [DialogAction](aws-properties-lex-bot-dialogaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Intent`  <a name="cfn-lex-bot-dialogstate-intent"></a>
Override settings to configure the intent state\.  
*Required*: No  
*Type*: [IntentOverride](aws-properties-lex-bot-intentoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionAttributes`  <a name="cfn-lex-bot-dialogstate-sessionattributes"></a>
Map of key/value pairs representing session\-specific context information\. It contains application information passed between Amazon Lex and a client application\.  
*Required*: No  
*Type*: List of [SessionAttribute](aws-properties-lex-bot-sessionattribute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
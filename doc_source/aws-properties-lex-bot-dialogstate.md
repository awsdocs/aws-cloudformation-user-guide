# AWS::Lex::Bot DialogState<a name="aws-properties-lex-bot-dialogstate"></a>

<a name="aws-properties-lex-bot-dialogstate-description"></a>The `DialogState` property type specifies Property description not available\. for an [AWS::Lex::Bot](aws-resource-lex-bot.md)\.

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
Property description not available\.  
*Required*: No  
*Type*: [DialogAction](aws-properties-lex-bot-dialogaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Intent`  <a name="cfn-lex-bot-dialogstate-intent"></a>
Property description not available\.  
*Required*: No  
*Type*: [IntentOverride](aws-properties-lex-bot-intentoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionAttributes`  <a name="cfn-lex-bot-dialogstate-sessionattributes"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [SessionAttribute](aws-properties-lex-bot-sessionattribute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
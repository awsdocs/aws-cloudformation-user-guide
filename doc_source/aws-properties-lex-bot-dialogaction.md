# AWS::Lex::Bot DialogAction<a name="aws-properties-lex-bot-dialogaction"></a>

Defines the action that the bot executes at runtime when the conversation reaches this step\.

## Syntax<a name="aws-properties-lex-bot-dialogaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-dialogaction-syntax.json"></a>

```
{
  "[SlotToElicit](#cfn-lex-bot-dialogaction-slottoelicit)" : String,
  "[SuppressNextMessage](#cfn-lex-bot-dialogaction-suppressnextmessage)" : Boolean,
  "[Type](#cfn-lex-bot-dialogaction-type)" : String
}
```

### YAML<a name="aws-properties-lex-bot-dialogaction-syntax.yaml"></a>

```
  [SlotToElicit](#cfn-lex-bot-dialogaction-slottoelicit): String
  [SuppressNextMessage](#cfn-lex-bot-dialogaction-suppressnextmessage): Boolean
  [Type](#cfn-lex-bot-dialogaction-type): String
```

## Properties<a name="aws-properties-lex-bot-dialogaction-properties"></a>

`SlotToElicit`  <a name="cfn-lex-bot-dialogaction-slottoelicit"></a>
If the dialog action is `ElicitSlot`, defines the slot to elicit from the user\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuppressNextMessage`  <a name="cfn-lex-bot-dialogaction-suppressnextmessage"></a>
When true the next message for the intent is not used\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-lex-bot-dialogaction-type"></a>
The action that the bot should execute\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
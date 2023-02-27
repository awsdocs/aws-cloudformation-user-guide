# AWS::Lex::Bot SlotValue<a name="aws-properties-lex-bot-slotvalue"></a>

The value to set in a slot\.

## Syntax<a name="aws-properties-lex-bot-slotvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotvalue-syntax.json"></a>

```
{
  "[InterpretedValue](#cfn-lex-bot-slotvalue-interpretedvalue)" : String
}
```

### YAML<a name="aws-properties-lex-bot-slotvalue-syntax.yaml"></a>

```
  [InterpretedValue](#cfn-lex-bot-slotvalue-interpretedvalue): String
```

## Properties<a name="aws-properties-lex-bot-slotvalue-properties"></a>

`InterpretedValue`  <a name="cfn-lex-bot-slotvalue-interpretedvalue"></a>
The value that Amazon Lex determines for the slot\. The actual value depends on the setting of the value selection strategy for the bot\. You can choose to use the value entered by the user, or you can have Amazon Lex choose the first value in the `resolvedValues` list\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
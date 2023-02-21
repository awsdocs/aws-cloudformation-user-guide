# AWS::Lex::Bot SlotPriority<a name="aws-properties-lex-bot-slotpriority"></a>

Sets the priority that Amazon Lex should use when eliciting slot values from a user\.

## Syntax<a name="aws-properties-lex-bot-slotpriority-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotpriority-syntax.json"></a>

```
{
  "[Priority](#cfn-lex-bot-slotpriority-priority)" : Integer,
  "[SlotName](#cfn-lex-bot-slotpriority-slotname)" : String
}
```

### YAML<a name="aws-properties-lex-bot-slotpriority-syntax.yaml"></a>

```
  [Priority](#cfn-lex-bot-slotpriority-priority): Integer
  [SlotName](#cfn-lex-bot-slotpriority-slotname): String
```

## Properties<a name="aws-properties-lex-bot-slotpriority-properties"></a>

`Priority`  <a name="cfn-lex-bot-slotpriority-priority"></a>
The priority that Amazon Lex should apply to the slot\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotName`  <a name="cfn-lex-bot-slotpriority-slotname"></a>
The name of the slot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
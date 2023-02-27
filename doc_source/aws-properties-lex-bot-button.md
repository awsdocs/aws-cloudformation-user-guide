# AWS::Lex::Bot Button<a name="aws-properties-lex-bot-button"></a>

Describes a button to use on a response card used to gather slot values from a user\.

## Syntax<a name="aws-properties-lex-bot-button-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-button-syntax.json"></a>

```
{
  "[Text](#cfn-lex-bot-button-text)" : String,
  "[Value](#cfn-lex-bot-button-value)" : String
}
```

### YAML<a name="aws-properties-lex-bot-button-syntax.yaml"></a>

```
  [Text](#cfn-lex-bot-button-text): String
  [Value](#cfn-lex-bot-button-value): String
```

## Properties<a name="aws-properties-lex-bot-button-properties"></a>

`Text`  <a name="cfn-lex-bot-button-text"></a>
The text that appears on the button\. Use this to tell the user what value is returned when they choose this button\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-lex-bot-button-value"></a>
The value returned to Amazon Lex when the user chooses this button\. This must be one of the slot values configured for the slot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
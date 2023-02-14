# AWS::Lex::Bot DialogCodeHookSetting<a name="aws-properties-lex-bot-dialogcodehooksetting"></a>

Specifies whether an intent uses the dialog code hook during conversations with a user\.

## Syntax<a name="aws-properties-lex-bot-dialogcodehooksetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-dialogcodehooksetting-syntax.json"></a>

```
{
  "[Enabled](#cfn-lex-bot-dialogcodehooksetting-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-lex-bot-dialogcodehooksetting-syntax.yaml"></a>

```
  [Enabled](#cfn-lex-bot-dialogcodehooksetting-enabled): Boolean
```

## Properties<a name="aws-properties-lex-bot-dialogcodehooksetting-properties"></a>

`Enabled`  <a name="cfn-lex-bot-dialogcodehooksetting-enabled"></a>
Indicates whether an intent uses the dialog code hook during a conversation with a user\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
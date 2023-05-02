# AWS::Lex::Bot DialogCodeHookSetting<a name="aws-properties-lex-bot-dialogcodehooksetting"></a>

Settings that determine the Lambda function that Amazon Lex uses for processing user responses\.

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
Enables the dialog code hook so that it processes user requests\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
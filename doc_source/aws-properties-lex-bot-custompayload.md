# AWS::Lex::Bot CustomPayload<a name="aws-properties-lex-bot-custompayload"></a>

A custom response string that Amazon Lex sends to your application\. You define the content and structure the string\.

## Syntax<a name="aws-properties-lex-bot-custompayload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-custompayload-syntax.json"></a>

```
{
  "[Value](#cfn-lex-bot-custompayload-value)" : String
}
```

### YAML<a name="aws-properties-lex-bot-custompayload-syntax.yaml"></a>

```
  [Value](#cfn-lex-bot-custompayload-value): String
```

## Properties<a name="aws-properties-lex-bot-custompayload-properties"></a>

`Value`  <a name="cfn-lex-bot-custompayload-value"></a>
The string that is sent to your application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
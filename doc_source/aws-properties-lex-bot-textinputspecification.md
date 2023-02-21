# AWS::Lex::Bot TextInputSpecification<a name="aws-properties-lex-bot-textinputspecification"></a>

Specifies the text input specifications\.

## Syntax<a name="aws-properties-lex-bot-textinputspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-textinputspecification-syntax.json"></a>

```
{
  "[StartTimeoutMs](#cfn-lex-bot-textinputspecification-starttimeoutms)" : Integer
}
```

### YAML<a name="aws-properties-lex-bot-textinputspecification-syntax.yaml"></a>

```
  [StartTimeoutMs](#cfn-lex-bot-textinputspecification-starttimeoutms): Integer
```

## Properties<a name="aws-properties-lex-bot-textinputspecification-properties"></a>

`StartTimeoutMs`  <a name="cfn-lex-bot-textinputspecification-starttimeoutms"></a>
Time for which a bot waits before re\-prompting a customer for text input\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
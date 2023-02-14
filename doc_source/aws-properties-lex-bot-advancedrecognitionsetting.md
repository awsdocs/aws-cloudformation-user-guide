# AWS::Lex::Bot AdvancedRecognitionSetting<a name="aws-properties-lex-bot-advancedrecognitionsetting"></a>

Specifies settings that enable advanced audio recognition for slot values\.

## Syntax<a name="aws-properties-lex-bot-advancedrecognitionsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-advancedrecognitionsetting-syntax.json"></a>

```
{
  "[AudioRecognitionStrategy](#cfn-lex-bot-advancedrecognitionsetting-audiorecognitionstrategy)" : String
}
```

### YAML<a name="aws-properties-lex-bot-advancedrecognitionsetting-syntax.yaml"></a>

```
  [AudioRecognitionStrategy](#cfn-lex-bot-advancedrecognitionsetting-audiorecognitionstrategy): String
```

## Properties<a name="aws-properties-lex-bot-advancedrecognitionsetting-properties"></a>

`AudioRecognitionStrategy`  <a name="cfn-lex-bot-advancedrecognitionsetting-audiorecognitionstrategy"></a>
Specifies that Amazon Lex should use slot values as a custom vocabulary when recognizing user utterances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
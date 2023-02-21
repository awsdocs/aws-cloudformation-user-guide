# AWS::Lex::Bot AdvancedRecognitionSetting<a name="aws-properties-lex-bot-advancedrecognitionsetting"></a>

Provides settings that enable advanced recognition settings for slot values\.

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
Enables using the slot values as a custom vocabulary for recognizing user utterances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
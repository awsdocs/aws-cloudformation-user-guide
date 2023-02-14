# AWS::Lex::Bot VoiceSettings<a name="aws-properties-lex-bot-voicesettings"></a>

Identifies the Amazon Polly voice used for audio interaction with the user\.

## Syntax<a name="aws-properties-lex-bot-voicesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-voicesettings-syntax.json"></a>

```
{
  "[Engine](#cfn-lex-bot-voicesettings-engine)" : String,
  "[VoiceId](#cfn-lex-bot-voicesettings-voiceid)" : String
}
```

### YAML<a name="aws-properties-lex-bot-voicesettings-syntax.yaml"></a>

```
  [Engine](#cfn-lex-bot-voicesettings-engine): String
  [VoiceId](#cfn-lex-bot-voicesettings-voiceid): String
```

## Properties<a name="aws-properties-lex-bot-voicesettings-properties"></a>

`Engine`  <a name="cfn-lex-bot-voicesettings-engine"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VoiceId`  <a name="cfn-lex-bot-voicesettings-voiceid"></a>
The Amazon Polly voice used for voice interaction with the user\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
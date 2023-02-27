# AWS::Lex::Bot VoiceSettings<a name="aws-properties-lex-bot-voicesettings"></a>

Defines settings for using an Amazon Polly voice to communicate with a user\.

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
Indicates the type of Amazon Polly voice that Amazon Lex should use for voice interaction with the user\. For more information, see the [`engine` parameter of the `SynthesizeSpeech` operation](https://docs.aws.amazon.com/polly/latest/dg/API_SynthesizeSpeech.html#polly-SynthesizeSpeech-request-Engine) in the *Amazon Polly developer guide*\.  
If you do not specify a value, the default is `standard`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VoiceId`  <a name="cfn-lex-bot-voicesettings-voiceid"></a>
The identifier of the Amazon Polly voice to use\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Lex::Bot BotLocale<a name="aws-properties-lex-bot-botlocale"></a>

Provides configuration information for a locale\.

## Syntax<a name="aws-properties-lex-bot-botlocale-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-botlocale-syntax.json"></a>

```
{
  "[CustomVocabulary](#cfn-lex-bot-botlocale-customvocabulary)" : CustomVocabulary,
  "[Description](#cfn-lex-bot-botlocale-description)" : String,
  "[Intents](#cfn-lex-bot-botlocale-intents)" : [ Intent, ... ],
  "[LocaleId](#cfn-lex-bot-botlocale-localeid)" : String,
  "[NluConfidenceThreshold](#cfn-lex-bot-botlocale-nluconfidencethreshold)" : Double,
  "[SlotTypes](#cfn-lex-bot-botlocale-slottypes)" : [ SlotType, ... ],
  "[VoiceSettings](#cfn-lex-bot-botlocale-voicesettings)" : VoiceSettings
}
```

### YAML<a name="aws-properties-lex-bot-botlocale-syntax.yaml"></a>

```
  [CustomVocabulary](#cfn-lex-bot-botlocale-customvocabulary): 
    CustomVocabulary
  [Description](#cfn-lex-bot-botlocale-description): String
  [Intents](#cfn-lex-bot-botlocale-intents): 
    - Intent
  [LocaleId](#cfn-lex-bot-botlocale-localeid): String
  [NluConfidenceThreshold](#cfn-lex-bot-botlocale-nluconfidencethreshold): Double
  [SlotTypes](#cfn-lex-bot-botlocale-slottypes): 
    - SlotType
  [VoiceSettings](#cfn-lex-bot-botlocale-voicesettings): 
    VoiceSettings
```

## Properties<a name="aws-properties-lex-bot-botlocale-properties"></a>

`CustomVocabulary`  <a name="cfn-lex-bot-botlocale-customvocabulary"></a>
Specifies a custom vocabulary to use with a specific locale\.  
*Required*: No  
*Type*: [CustomVocabulary](aws-properties-lex-bot-customvocabulary.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-lex-bot-botlocale-description"></a>
A description of the bot locale\. Use this to help identify the bot locale in lists\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Intents`  <a name="cfn-lex-bot-botlocale-intents"></a>
One or more intents defined for the locale\.  
*Required*: No  
*Type*: List of [Intent](aws-properties-lex-bot-intent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocaleId`  <a name="cfn-lex-bot-botlocale-localeid"></a>
The identifier of the language and locale that the bot will be used in\. The string must match one of the supported locales\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NluConfidenceThreshold`  <a name="cfn-lex-bot-botlocale-nluconfidencethreshold"></a>
Determines the threshold where Amazon Lex will insert the `AMAZON.FallbackIntent`, `AMAZON.KendraSearchIntent`, or both when returning alternative intents\. You must configure an `AMAZON.FallbackIntent`\. `AMAZON.KendraSearchIntent` is only inserted if it is configured for the bot\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotTypes`  <a name="cfn-lex-bot-botlocale-slottypes"></a>
One or more slot types defined for the locale\.  
*Required*: No  
*Type*: List of [SlotType](aws-properties-lex-bot-slottype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VoiceSettings`  <a name="cfn-lex-bot-botlocale-voicesettings"></a>
Defines settings for using an Amazon Polly voice to communicate with a user\.  
*Required*: No  
*Type*: [VoiceSettings](aws-properties-lex-bot-voicesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
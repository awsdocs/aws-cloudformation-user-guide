# AWS::Lex::Bot TestBotAliasSettings<a name="aws-properties-lex-bot-testbotaliassettings"></a>

Specifies configuration settings for the alias used to test the bot\. If the `TestBotAliasSettings` property is not specified, the settings are configured with default values\.

## Syntax<a name="aws-properties-lex-bot-testbotaliassettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-testbotaliassettings-syntax.json"></a>

```
{
  "[BotAliasLocaleSettings](#cfn-lex-bot-testbotaliassettings-botaliaslocalesettings)" : [ BotAliasLocaleSettingsItem, ... ],
  "[ConversationLogSettings](#cfn-lex-bot-testbotaliassettings-conversationlogsettings)" : ConversationLogSettings,
  "[Description](#cfn-lex-bot-testbotaliassettings-description)" : String,
  "[SentimentAnalysisSettings](#cfn-lex-bot-testbotaliassettings-sentimentanalysissettings)" : SentimentAnalysisSettings
}
```

### YAML<a name="aws-properties-lex-bot-testbotaliassettings-syntax.yaml"></a>

```
  [BotAliasLocaleSettings](#cfn-lex-bot-testbotaliassettings-botaliaslocalesettings): 
    - BotAliasLocaleSettingsItem
  [ConversationLogSettings](#cfn-lex-bot-testbotaliassettings-conversationlogsettings): 
    ConversationLogSettings
  [Description](#cfn-lex-bot-testbotaliassettings-description): String
  [SentimentAnalysisSettings](#cfn-lex-bot-testbotaliassettings-sentimentanalysissettings): 
    SentimentAnalysisSettings
```

## Properties<a name="aws-properties-lex-bot-testbotaliassettings-properties"></a>

`BotAliasLocaleSettings`  <a name="cfn-lex-bot-testbotaliassettings-botaliaslocalesettings"></a>
Specifies settings that are unique to a locale\. For example, you can use a different Lambda function depending on the bot's locale\.  
*Required*: No  
*Type*: [List](aws-properties-lex-bot-botaliaslocalesettings.md) of [BotAliasLocaleSettingsItem](aws-properties-lex-bot-botaliaslocalesettingsitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConversationLogSettings`  <a name="cfn-lex-bot-testbotaliassettings-conversationlogsettings"></a>
Specifies settings for conversation logs that save audio, text, and metadata information for conversations with your users\.  
*Required*: No  
*Type*: [ConversationLogSettings](aws-properties-lex-bot-conversationlogsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-lex-bot-testbotaliassettings-description"></a>
Specifies a description for the test bot alias\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SentimentAnalysisSettings`  <a name="cfn-lex-bot-testbotaliassettings-sentimentanalysissettings"></a>
Specifies whether Amazon Lex will use Amazon Comprehend to detect the sentiment of user utterances\.  
*Required*: No  
*Type*: [SentimentAnalysisSettings](aws-properties-lex-bot-sentimentanalysissettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Lex::Bot BotAliasLocaleSettingsItem<a name="aws-properties-lex-bot-botaliaslocalesettingsitem"></a>

Specifies locale settings for a single locale\.

## Syntax<a name="aws-properties-lex-bot-botaliaslocalesettingsitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-botaliaslocalesettingsitem-syntax.json"></a>

```
{
  "[BotAliasLocaleSetting](#cfn-lex-bot-botaliaslocalesettingsitem-botaliaslocalesetting)" : BotAliasLocaleSettings,
  "[LocaleId](#cfn-lex-bot-botaliaslocalesettingsitem-localeid)" : String
}
```

### YAML<a name="aws-properties-lex-bot-botaliaslocalesettingsitem-syntax.yaml"></a>

```
  [BotAliasLocaleSetting](#cfn-lex-bot-botaliaslocalesettingsitem-botaliaslocalesetting): 
    BotAliasLocaleSettings
  [LocaleId](#cfn-lex-bot-botaliaslocalesettingsitem-localeid): String
```

## Properties<a name="aws-properties-lex-bot-botaliaslocalesettingsitem-properties"></a>

`BotAliasLocaleSetting`  <a name="cfn-lex-bot-botaliaslocalesettingsitem-botaliaslocalesetting"></a>
Specifies locale settings for a locale\.  
*Required*: Yes  
*Type*: [BotAliasLocaleSettings](aws-properties-lex-bot-botaliaslocalesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocaleId`  <a name="cfn-lex-bot-botaliaslocalesettingsitem-localeid"></a>
Specifies the locale that the settings apply to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
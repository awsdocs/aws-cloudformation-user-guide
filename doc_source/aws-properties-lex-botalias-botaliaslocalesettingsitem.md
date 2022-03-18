# AWS::Lex::BotAlias BotAliasLocaleSettingsItem<a name="aws-properties-lex-botalias-botaliaslocalesettingsitem"></a>

Specifies settings that are unique to a locale\. For example, you can use different Lambda function depending on the bot's locale\.

## Syntax<a name="aws-properties-lex-botalias-botaliaslocalesettingsitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-botaliaslocalesettingsitem-syntax.json"></a>

```
{
  "[BotAliasLocaleSetting](#cfn-lex-botalias-botaliaslocalesettingsitem-botaliaslocalesetting)" : BotAliasLocaleSettings,
  "[LocaleId](#cfn-lex-botalias-botaliaslocalesettingsitem-localeid)" : String
}
```

### YAML<a name="aws-properties-lex-botalias-botaliaslocalesettingsitem-syntax.yaml"></a>

```
  [BotAliasLocaleSetting](#cfn-lex-botalias-botaliaslocalesettingsitem-botaliaslocalesetting): 
    BotAliasLocaleSettings
  [LocaleId](#cfn-lex-botalias-botaliaslocalesettingsitem-localeid): String
```

## Properties<a name="aws-properties-lex-botalias-botaliaslocalesettingsitem-properties"></a>

`BotAliasLocaleSetting`  <a name="cfn-lex-botalias-botaliaslocalesettingsitem-botaliaslocalesetting"></a>
Specifies settings that are unique to a locale\.  
*Required*: Yes  
*Type*: [BotAliasLocaleSettings](aws-properties-lex-botalias-botaliaslocalesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocaleId`  <a name="cfn-lex-botalias-botaliaslocalesettingsitem-localeid"></a>
The unique identifier of the locale\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
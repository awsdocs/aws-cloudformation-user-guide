# AWS::Lex::Bot BotAliasLocaleSettings<a name="aws-properties-lex-bot-botaliaslocalesettings"></a>

Specifies settings that are unique to a locale\. For example, you can use a different Lambda function for each locale\.

## Syntax<a name="aws-properties-lex-bot-botaliaslocalesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-botaliaslocalesettings-syntax.json"></a>

```
{
  "[CodeHookSpecification](#cfn-lex-bot-botaliaslocalesettings-codehookspecification)" : CodeHookSpecification,
  "[Enabled](#cfn-lex-bot-botaliaslocalesettings-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-lex-bot-botaliaslocalesettings-syntax.yaml"></a>

```
  [CodeHookSpecification](#cfn-lex-bot-botaliaslocalesettings-codehookspecification): 
    CodeHookSpecification
  [Enabled](#cfn-lex-bot-botaliaslocalesettings-enabled): Boolean
```

## Properties<a name="aws-properties-lex-bot-botaliaslocalesettings-properties"></a>

`CodeHookSpecification`  <a name="cfn-lex-bot-botaliaslocalesettings-codehookspecification"></a>
Specifies the Lambda function to use in this locale\.  
*Required*: No  
*Type*: [CodeHookSpecification](aws-properties-lex-bot-codehookspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-lex-bot-botaliaslocalesettings-enabled"></a>
Specifies whether the locale is enabled for the bot\. If the value is false, the locale isn't available for use\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
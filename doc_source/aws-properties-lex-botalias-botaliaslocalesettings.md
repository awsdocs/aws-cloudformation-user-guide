# AWS::Lex::BotAlias BotAliasLocaleSettings<a name="aws-properties-lex-botalias-botaliaslocalesettings"></a>

Specifies settings that are unique to a locale\. For example, you can use different Lambda function depending on the bot's locale\.

## Syntax<a name="aws-properties-lex-botalias-botaliaslocalesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-botaliaslocalesettings-syntax.json"></a>

```
{
  "[CodeHookSpecification](#cfn-lex-botalias-botaliaslocalesettings-codehookspecification)" : CodeHookSpecification,
  "[Enabled](#cfn-lex-botalias-botaliaslocalesettings-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-lex-botalias-botaliaslocalesettings-syntax.yaml"></a>

```
  [CodeHookSpecification](#cfn-lex-botalias-botaliaslocalesettings-codehookspecification): 
    CodeHookSpecification
  [Enabled](#cfn-lex-botalias-botaliaslocalesettings-enabled): Boolean
```

## Properties<a name="aws-properties-lex-botalias-botaliaslocalesettings-properties"></a>

`CodeHookSpecification`  <a name="cfn-lex-botalias-botaliaslocalesettings-codehookspecification"></a>
Specifies the Lambda function that should be used in the locale\.  
*Required*: No  
*Type*: [CodeHookSpecification](aws-properties-lex-botalias-codehookspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-lex-botalias-botaliaslocalesettings-enabled"></a>
Determines whether the locale is enabled for the bot\. If the value is `false`, the locale isn't available for use\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Lex::Bot ObfuscationSetting<a name="aws-properties-lex-bot-obfuscationsetting"></a>

Determines whether Amazon Lex obscures slot values in conversation logs\. 

## Syntax<a name="aws-properties-lex-bot-obfuscationsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-obfuscationsetting-syntax.json"></a>

```
{
  "[ObfuscationSettingType](#cfn-lex-bot-obfuscationsetting-obfuscationsettingtype)" : String
}
```

### YAML<a name="aws-properties-lex-bot-obfuscationsetting-syntax.yaml"></a>

```
  [ObfuscationSettingType](#cfn-lex-bot-obfuscationsetting-obfuscationsettingtype): String
```

## Properties<a name="aws-properties-lex-bot-obfuscationsetting-properties"></a>

`ObfuscationSettingType`  <a name="cfn-lex-bot-obfuscationsetting-obfuscationsettingtype"></a>
Value that determines whether Amazon Lex obscures slot values in conversation logs\. The default is to obscure the values\. The valid values are `None` and `DefaultObfuscation.`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
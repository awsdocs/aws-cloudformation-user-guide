# AWS::Lex::BotAlias ConversationLogSettings<a name="aws-properties-lex-botalias-conversationlogsettings"></a>

Configures conversation logging that saves audio, text, and metadata for the conversations with your users\.

## Syntax<a name="aws-properties-lex-botalias-conversationlogsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-conversationlogsettings-syntax.json"></a>

```
{
  "[AudioLogSettings](#cfn-lex-botalias-conversationlogsettings-audiologsettings)" : [ AudioLogSetting, ... ],
  "[TextLogSettings](#cfn-lex-botalias-conversationlogsettings-textlogsettings)" : [ TextLogSetting, ... ]
}
```

### YAML<a name="aws-properties-lex-botalias-conversationlogsettings-syntax.yaml"></a>

```
  [AudioLogSettings](#cfn-lex-botalias-conversationlogsettings-audiologsettings): 
    - AudioLogSetting
  [TextLogSettings](#cfn-lex-botalias-conversationlogsettings-textlogsettings): 
    - TextLogSetting
```

## Properties<a name="aws-properties-lex-botalias-conversationlogsettings-properties"></a>

`AudioLogSettings`  <a name="cfn-lex-botalias-conversationlogsettings-audiologsettings"></a>
The Amazon S3 settings for logging audio to an S3 bucket\.  
*Required*: No  
*Type*: List of [AudioLogSetting](aws-properties-lex-botalias-audiologsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextLogSettings`  <a name="cfn-lex-botalias-conversationlogsettings-textlogsettings"></a>
The Amazon CloudWatch Logs settings for logging text and metadata\.  
*Required*: No  
*Type*: List of [TextLogSetting](aws-properties-lex-botalias-textlogsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
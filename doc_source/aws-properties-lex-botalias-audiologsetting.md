# AWS::Lex::BotAlias AudioLogSetting<a name="aws-properties-lex-botalias-audiologsetting"></a>

<a name="aws-properties-lex-botalias-audiologsetting-description"></a>The `AudioLogSetting` property type specifies Property description not available\. for an [AWS::Lex::BotAlias](aws-resource-lex-botalias.md)\.

## Syntax<a name="aws-properties-lex-botalias-audiologsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-audiologsetting-syntax.json"></a>

```
{
  "[Destination](#cfn-lex-botalias-audiologsetting-destination)" : AudioLogDestination,
  "[Enabled](#cfn-lex-botalias-audiologsetting-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-lex-botalias-audiologsetting-syntax.yaml"></a>

```
  [Destination](#cfn-lex-botalias-audiologsetting-destination): 
    AudioLogDestination
  [Enabled](#cfn-lex-botalias-audiologsetting-enabled): Boolean
```

## Properties<a name="aws-properties-lex-botalias-audiologsetting-properties"></a>

`Destination`  <a name="cfn-lex-botalias-audiologsetting-destination"></a>
The location of audio log files collected when conversation logging is enabled for a bot\.  
*Required*: Yes  
*Type*: [AudioLogDestination](aws-properties-lex-botalias-audiologdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-lex-botalias-audiologsetting-enabled"></a>
Property description not available\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
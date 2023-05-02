# AWS::Lex::Bot ExternalSourceSetting<a name="aws-properties-lex-bot-externalsourcesetting"></a>

Provides information about the external source of the slot type's definition\.

## Syntax<a name="aws-properties-lex-bot-externalsourcesetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-externalsourcesetting-syntax.json"></a>

```
{
  "[GrammarSlotTypeSetting](#cfn-lex-bot-externalsourcesetting-grammarslottypesetting)" : GrammarSlotTypeSetting
}
```

### YAML<a name="aws-properties-lex-bot-externalsourcesetting-syntax.yaml"></a>

```
  [GrammarSlotTypeSetting](#cfn-lex-bot-externalsourcesetting-grammarslottypesetting): 
    GrammarSlotTypeSetting
```

## Properties<a name="aws-properties-lex-bot-externalsourcesetting-properties"></a>

`GrammarSlotTypeSetting`  <a name="cfn-lex-bot-externalsourcesetting-grammarslottypesetting"></a>
Settings required for a slot type based on a grammar that you provide\.  
*Required*: No  
*Type*: [GrammarSlotTypeSetting](aws-properties-lex-bot-grammarslottypesetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
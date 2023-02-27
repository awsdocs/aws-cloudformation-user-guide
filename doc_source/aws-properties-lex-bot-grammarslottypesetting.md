# AWS::Lex::Bot GrammarSlotTypeSetting<a name="aws-properties-lex-bot-grammarslottypesetting"></a>

Settings requried for a slot type based on a grammar that you provide\.

## Syntax<a name="aws-properties-lex-bot-grammarslottypesetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-grammarslottypesetting-syntax.json"></a>

```
{
  "[Source](#cfn-lex-bot-grammarslottypesetting-source)" : GrammarSlotTypeSource
}
```

### YAML<a name="aws-properties-lex-bot-grammarslottypesetting-syntax.yaml"></a>

```
  [Source](#cfn-lex-bot-grammarslottypesetting-source): 
    GrammarSlotTypeSource
```

## Properties<a name="aws-properties-lex-bot-grammarslottypesetting-properties"></a>

`Source`  <a name="cfn-lex-bot-grammarslottypesetting-source"></a>
The source of the grammar used to create the slot type\.  
*Required*: No  
*Type*: [GrammarSlotTypeSource](aws-properties-lex-bot-grammarslottypesource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
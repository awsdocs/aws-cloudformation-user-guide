# AWS::Lex::Bot IntentOverride<a name="aws-properties-lex-bot-intentoverride"></a>

Override settings to configure the intent state\.

## Syntax<a name="aws-properties-lex-bot-intentoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-intentoverride-syntax.json"></a>

```
{
  "[Name](#cfn-lex-bot-intentoverride-name)" : String,
  "[Slots](#cfn-lex-bot-intentoverride-slots)" : [ SlotValueOverrideMap, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-intentoverride-syntax.yaml"></a>

```
  [Name](#cfn-lex-bot-intentoverride-name): String
  [Slots](#cfn-lex-bot-intentoverride-slots): 
    - SlotValueOverrideMap
```

## Properties<a name="aws-properties-lex-bot-intentoverride-properties"></a>

`Name`  <a name="cfn-lex-bot-intentoverride-name"></a>
The name of the intent\. Only required when you're switching intents\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slots`  <a name="cfn-lex-bot-intentoverride-slots"></a>
A map of all of the slot value overrides for the intent\. The name of the slot maps to the value of the slot\. Slots that are not included in the map aren't overridden\.  
*Required*: No  
*Type*: List of [SlotValueOverrideMap](aws-properties-lex-bot-slotvalueoverridemap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
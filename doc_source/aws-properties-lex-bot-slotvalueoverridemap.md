# AWS::Lex::Bot SlotValueOverrideMap<a name="aws-properties-lex-bot-slotvalueoverridemap"></a>

Maps a slot name to the [SlotValueOverride](https://docs.aws.amazon.com/lexv2/latest/APIReference/API_SlotValueOverride.html) object\.

## Syntax<a name="aws-properties-lex-bot-slotvalueoverridemap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotvalueoverridemap-syntax.json"></a>

```
{
  "[SlotName](#cfn-lex-bot-slotvalueoverridemap-slotname)" : String,
  "[SlotValueOverride](#cfn-lex-bot-slotvalueoverridemap-slotvalueoverride)" : SlotValueOverride
}
```

### YAML<a name="aws-properties-lex-bot-slotvalueoverridemap-syntax.yaml"></a>

```
  [SlotName](#cfn-lex-bot-slotvalueoverridemap-slotname): String
  [SlotValueOverride](#cfn-lex-bot-slotvalueoverridemap-slotvalueoverride): 
    SlotValueOverride
```

## Properties<a name="aws-properties-lex-bot-slotvalueoverridemap-properties"></a>

`SlotName`  <a name="cfn-lex-bot-slotvalueoverridemap-slotname"></a>
The name of the slot\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotValueOverride`  <a name="cfn-lex-bot-slotvalueoverridemap-slotvalueoverride"></a>
The SlotValueOverride object to which the slot name will be mapped\.  
*Required*: No  
*Type*: [SlotValueOverride](aws-properties-lex-bot-slotvalueoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
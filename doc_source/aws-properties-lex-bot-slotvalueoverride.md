# AWS::Lex::Bot SlotValueOverride<a name="aws-properties-lex-bot-slotvalueoverride"></a>

The slot values that Amazon Lex uses when it sets slot values in a dialog step\.

## Syntax<a name="aws-properties-lex-bot-slotvalueoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotvalueoverride-syntax.json"></a>

```
{
  "[Shape](#cfn-lex-bot-slotvalueoverride-shape)" : String,
  "[Value](#cfn-lex-bot-slotvalueoverride-value)" : SlotValue,
  "[Values](#cfn-lex-bot-slotvalueoverride-values)" : [ SlotValueOverride, ... ]
}
```

### YAML<a name="aws-properties-lex-bot-slotvalueoverride-syntax.yaml"></a>

```
  [Shape](#cfn-lex-bot-slotvalueoverride-shape): String
  [Value](#cfn-lex-bot-slotvalueoverride-value): 
    SlotValue
  [Values](#cfn-lex-bot-slotvalueoverride-values): 
    - SlotValueOverride
```

## Properties<a name="aws-properties-lex-bot-slotvalueoverride-properties"></a>

`Shape`  <a name="cfn-lex-bot-slotvalueoverride-shape"></a>
When the shape value is `List`, it indicates that the `values` field contains a list of slot values\. When the value is `Scalar`, it indicates that the `value` field contains a single value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-lex-bot-slotvalueoverride-value"></a>
The current value of the slot\.  
*Required*: No  
*Type*: [SlotValue](aws-properties-lex-bot-slotvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-lex-bot-slotvalueoverride-values"></a>
A list of one or more values that the user provided for the slot\. For example, for a slot that elicits pizza toppings, the values might be "pepperoni" and "pineapple\."  
*Required*: No  
*Type*: List of [SlotValueOverride](#aws-properties-lex-bot-slotvalueoverride)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
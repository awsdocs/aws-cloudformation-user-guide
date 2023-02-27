# AWS::Lex::Bot SlotType<a name="aws-properties-lex-bot-slottype"></a>

Describes a slot type\.

## Syntax<a name="aws-properties-lex-bot-slottype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slottype-syntax.json"></a>

```
{
  "[Description](#cfn-lex-bot-slottype-description)" : String,
  "[ExternalSourceSetting](#cfn-lex-bot-slottype-externalsourcesetting)" : ExternalSourceSetting,
  "[Name](#cfn-lex-bot-slottype-name)" : String,
  "[ParentSlotTypeSignature](#cfn-lex-bot-slottype-parentslottypesignature)" : String,
  "[SlotTypeValues](#cfn-lex-bot-slottype-slottypevalues)" : [ SlotTypeValue, ... ],
  "[ValueSelectionSetting](#cfn-lex-bot-slottype-valueselectionsetting)" : SlotValueSelectionSetting
}
```

### YAML<a name="aws-properties-lex-bot-slottype-syntax.yaml"></a>

```
  [Description](#cfn-lex-bot-slottype-description): String
  [ExternalSourceSetting](#cfn-lex-bot-slottype-externalsourcesetting): 
    ExternalSourceSetting
  [Name](#cfn-lex-bot-slottype-name): String
  [ParentSlotTypeSignature](#cfn-lex-bot-slottype-parentslottypesignature): String
  [SlotTypeValues](#cfn-lex-bot-slottype-slottypevalues): 
    - SlotTypeValue
  [ValueSelectionSetting](#cfn-lex-bot-slottype-valueselectionsetting): 
    SlotValueSelectionSetting
```

## Properties<a name="aws-properties-lex-bot-slottype-properties"></a>

`Description`  <a name="cfn-lex-bot-slottype-description"></a>
A description of the slot type\. Use the description to help identify the slot type in lists\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExternalSourceSetting`  <a name="cfn-lex-bot-slottype-externalsourcesetting"></a>
Sets the type of external information used to create the slot type\.  
*Required*: No  
*Type*: [ExternalSourceSetting](aws-properties-lex-bot-externalsourcesetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lex-bot-slottype-name"></a>
The name of the slot type\. A slot type name must be unique withing the account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParentSlotTypeSignature`  <a name="cfn-lex-bot-slottype-parentslottypesignature"></a>
The built\-in slot type used as a parent of this slot type\. When you define a parent slot type, the new slot type has the configuration of the parent lot type\.  
Only `AMAZON.AlphaNumeric` is supported\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotTypeValues`  <a name="cfn-lex-bot-slottype-slottypevalues"></a>
A list of SlotTypeValue objects that defines the values that the slot type can take\. Each value can have a list of synonyms, additional values that help train the machine learning model about the values that it resolves for the slot\.  
*Required*: No  
*Type*: List of [SlotTypeValue](aws-properties-lex-bot-slottypevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueSelectionSetting`  <a name="cfn-lex-bot-slottype-valueselectionsetting"></a>
Determines the slot resolution strategy that Amazon Lex uses to return slot type values\. The field can be set to one of the following values:  
+  `ORIGINAL_VALUE` \- Returns the value entered by the user, if the user value is similar to the slot value\.
+  `TOP_RESOLUTION` \- If there is a resolution list for the slot, return the first value in the resolution list as the slot type value\. If there is no resolution list, null is returned\.
If you don't specify the `valueSelectionStrategy`, the default is `ORIGINAL_VALUE`\.  
*Required*: No  
*Type*: [SlotValueSelectionSetting](aws-properties-lex-bot-slotvalueselectionsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
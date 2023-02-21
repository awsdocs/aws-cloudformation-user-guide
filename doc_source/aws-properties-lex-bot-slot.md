# AWS::Lex::Bot Slot<a name="aws-properties-lex-bot-slot"></a>

Specifies the definition of a slot\. Amazon Lex elicits slot values from uses to fulfill the user's intent\.

## Syntax<a name="aws-properties-lex-bot-slot-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slot-syntax.json"></a>

```
{
  "[Description](#cfn-lex-bot-slot-description)" : String,
  "[MultipleValuesSetting](#cfn-lex-bot-slot-multiplevaluessetting)" : MultipleValuesSetting,
  "[Name](#cfn-lex-bot-slot-name)" : String,
  "[ObfuscationSetting](#cfn-lex-bot-slot-obfuscationsetting)" : ObfuscationSetting,
  "[SlotTypeName](#cfn-lex-bot-slot-slottypename)" : String,
  "[ValueElicitationSetting](#cfn-lex-bot-slot-valueelicitationsetting)" : SlotValueElicitationSetting
}
```

### YAML<a name="aws-properties-lex-bot-slot-syntax.yaml"></a>

```
  [Description](#cfn-lex-bot-slot-description): String
  [MultipleValuesSetting](#cfn-lex-bot-slot-multiplevaluessetting): 
    MultipleValuesSetting
  [Name](#cfn-lex-bot-slot-name): String
  [ObfuscationSetting](#cfn-lex-bot-slot-obfuscationsetting): 
    ObfuscationSetting
  [SlotTypeName](#cfn-lex-bot-slot-slottypename): String
  [ValueElicitationSetting](#cfn-lex-bot-slot-valueelicitationsetting): 
    SlotValueElicitationSetting
```

## Properties<a name="aws-properties-lex-bot-slot-properties"></a>

`Description`  <a name="cfn-lex-bot-slot-description"></a>
The description of the slot\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultipleValuesSetting`  <a name="cfn-lex-bot-slot-multiplevaluessetting"></a>
Indicates whether a slot can return multiple values\.  
*Required*: No  
*Type*: [MultipleValuesSetting](aws-properties-lex-bot-multiplevaluessetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lex-bot-slot-name"></a>
The name given to the slot\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^([0-9a-zA-Z][_-]?)+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObfuscationSetting`  <a name="cfn-lex-bot-slot-obfuscationsetting"></a>
Determines whether the contents of the slot are obfuscated in Amazon CloudWatch Logs logs\. Use obfuscated slots to protect information such as personally identifiable information \(PII\) in logs\.  
*Required*: No  
*Type*: [ObfuscationSetting](aws-properties-lex-bot-obfuscationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlotTypeName`  <a name="cfn-lex-bot-slot-slottypename"></a>
The name of the slot type that this slot is based on\. The slot type defines the acceptable values for the slot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueElicitationSetting`  <a name="cfn-lex-bot-slot-valueelicitationsetting"></a>
Determines the slot resolution strategy that Amazon Lex uses to return slot type values\. The field can be set to one of the following values:  
+ ORIGINAL\_VALUE \- Returns the value entered by the user, if the user value is similar to a slot value\.
+ TOP\_RESOLUTION \- If there is a resolution list for the slot, return the first value in the resolution list as the slot type value\. If there is no resolution list, null is returned\.
If you don't specify the `valueSelectionStrategy`, the default is `ORIGINAL_VALUE`\.  
*Required*: Yes  
*Type*: [SlotValueElicitationSetting](aws-properties-lex-bot-slotvalueelicitationsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
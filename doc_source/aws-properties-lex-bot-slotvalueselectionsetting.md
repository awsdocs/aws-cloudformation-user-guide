# AWS::Lex::Bot SlotValueSelectionSetting<a name="aws-properties-lex-bot-slotvalueselectionsetting"></a>

Contains settings used by Amazon Lex to select a slot value\.

## Syntax<a name="aws-properties-lex-bot-slotvalueselectionsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotvalueselectionsetting-syntax.json"></a>

```
{
  "[RegexFilter](#cfn-lex-bot-slotvalueselectionsetting-regexfilter)" : SlotValueRegexFilter,
  "[ResolutionStrategy](#cfn-lex-bot-slotvalueselectionsetting-resolutionstrategy)" : String
}
```

### YAML<a name="aws-properties-lex-bot-slotvalueselectionsetting-syntax.yaml"></a>

```
  [RegexFilter](#cfn-lex-bot-slotvalueselectionsetting-regexfilter): 
    SlotValueRegexFilter
  [ResolutionStrategy](#cfn-lex-bot-slotvalueselectionsetting-resolutionstrategy): String
```

## Properties<a name="aws-properties-lex-bot-slotvalueselectionsetting-properties"></a>

`RegexFilter`  <a name="cfn-lex-bot-slotvalueselectionsetting-regexfilter"></a>
A regular expression used to validate the value of a slot\.  
*Required*: No  
*Type*: [SlotValueRegexFilter](aws-properties-lex-bot-slotvalueregexfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResolutionStrategy`  <a name="cfn-lex-bot-slotvalueselectionsetting-resolutionstrategy"></a>
Determines the slot resolution strategy that Amazon Lex uses to return slot type values\. The field can be set to one of the following values:  
+ OriginalValue \- Returns the value entered by the user, if the user value is similar to a slot value\.
+ TopResolution \- If there is a resolution list for the slot, return the first value in the resolution list as the slot type value\. If there is no resolution list, null is returned\.
If you don't specify the valueSelectionStrategy, the default is OriginalValue\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
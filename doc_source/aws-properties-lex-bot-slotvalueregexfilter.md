# AWS::Lex::Bot SlotValueRegexFilter<a name="aws-properties-lex-bot-slotvalueregexfilter"></a>

Provides a regular expression used to validate the value of a slot\.

## Syntax<a name="aws-properties-lex-bot-slotvalueregexfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-slotvalueregexfilter-syntax.json"></a>

```
{
  "[Pattern](#cfn-lex-bot-slotvalueregexfilter-pattern)" : String
}
```

### YAML<a name="aws-properties-lex-bot-slotvalueregexfilter-syntax.yaml"></a>

```
  [Pattern](#cfn-lex-bot-slotvalueregexfilter-pattern): String
```

## Properties<a name="aws-properties-lex-bot-slotvalueregexfilter-properties"></a>

`Pattern`  <a name="cfn-lex-bot-slotvalueregexfilter-pattern"></a>
A regular expression used to validate the value of a slot\.  
 Use a standard regular expression\. Amazon Lex supports the following characters in the regular expression:   
+ A\-Z, a\-z
+ 0\-9
+ Unicode characters \("\\u<Unicode>"\)
 Represent Unicode characters with four digits, for example "\\u0041" or "\\u005A"\.   
 The following regular expression operators are not supported:   
+ Infinite repeaters: \*, \+, or \{x,\} with no upper bound\.
+ Wild card \(\.\)
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::WAFv2::RuleGroup RegexMatchStatement<a name="aws-properties-wafv2-rulegroup-regexmatchstatement"></a>

A rule statement used to search web request components for a match against a single regular expression\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-regexmatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-regexmatchstatement-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafv2-rulegroup-regexmatchstatement-fieldtomatch)" : FieldToMatch,
  "[RegexString](#cfn-wafv2-rulegroup-regexmatchstatement-regexstring)" : String,
  "[TextTransformations](#cfn-wafv2-rulegroup-regexmatchstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-regexmatchstatement-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafv2-rulegroup-regexmatchstatement-fieldtomatch): 
    FieldToMatch
  [RegexString](#cfn-wafv2-rulegroup-regexmatchstatement-regexstring): 
    String
  [TextTransformations](#cfn-wafv2-rulegroup-regexmatchstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-rulegroup-regexmatchstatement-properties"></a>

`FieldToMatch`  <a name="cfn-wafv2-rulegroup-regexmatchstatement-fieldtomatch"></a>
The part of the web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-rulegroup-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexString`  <a name="cfn-wafv2-rulegroup-regexmatchstatement-regexstring"></a>
The string representing the regular expression\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-rulegroup-regexmatchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content of the request component identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-rulegroup-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
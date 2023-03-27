# AWS::WAFv2::WebACL RegexPatternSetReferenceStatement<a name="aws-properties-wafv2-webacl-regexpatternsetreferencestatement"></a>

A rule statement used to search web request components for matches with regular expressions\. To use this, create a [AWS::WAFv2::RegexPatternSet](aws-resource-wafv2-regexpatternset.md) that specifies the expressions that you want to detect, then use that set in this statement\. A web request matches the pattern set rule statement if the request component matches any of the patterns in the set\. 

Each regex pattern set rule statement references a regex pattern set\. You create and maintain the set independent of your rules\. This allows you to use the single set in multiple rules\. When you update the referenced set, AWS WAF automatically updates all rules that reference it\.

## Syntax<a name="aws-properties-wafv2-webacl-regexpatternsetreferencestatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-regexpatternsetreferencestatement-syntax.json"></a>

```
{
  "[Arn](#cfn-wafv2-webacl-regexpatternsetreferencestatement-arn)" : String,
  "[FieldToMatch](#cfn-wafv2-webacl-regexpatternsetreferencestatement-fieldtomatch)" : FieldToMatch,
  "[TextTransformations](#cfn-wafv2-webacl-regexpatternsetreferencestatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-regexpatternsetreferencestatement-syntax.yaml"></a>

```
  [Arn](#cfn-wafv2-webacl-regexpatternsetreferencestatement-arn): String
  [FieldToMatch](#cfn-wafv2-webacl-regexpatternsetreferencestatement-fieldtomatch): 
    FieldToMatch
  [TextTransformations](#cfn-wafv2-webacl-regexpatternsetreferencestatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-webacl-regexpatternsetreferencestatement-properties"></a>

`Arn`  <a name="cfn-wafv2-webacl-regexpatternsetreferencestatement-arn"></a>
The Amazon Resource Name \(ARN\) of the [AWS::WAFv2::RegexPatternSet](aws-resource-wafv2-regexpatternset.md) that this statement references\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldToMatch`  <a name="cfn-wafv2-webacl-regexpatternsetreferencestatement-fieldtomatch"></a>
The part of the web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-webacl-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-webacl-regexpatternsetreferencestatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content of the request component identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
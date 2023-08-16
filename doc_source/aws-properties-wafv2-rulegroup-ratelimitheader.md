# AWS::WAFv2::RuleGroup RateLimitHeader<a name="aws-properties-wafv2-rulegroup-ratelimitheader"></a>

Specifies a header as an aggregate key for a rate\-based rule\. Each distinct value in the header contributes to the aggregation instance\. If you use a single header as your custom key, then each value fully defines an aggregation instance\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-ratelimitheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-ratelimitheader-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-rulegroup-ratelimitheader-name)" : String,
  "[TextTransformations](#cfn-wafv2-rulegroup-ratelimitheader-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-ratelimitheader-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-rulegroup-ratelimitheader-name): String
  [TextTransformations](#cfn-wafv2-rulegroup-ratelimitheader-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-rulegroup-ratelimitheader-properties"></a>

`Name`  <a name="cfn-wafv2-rulegroup-ratelimitheader-name"></a>
The name of the header to use\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-rulegroup-ratelimitheader-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. Text transformations are used in rule match statements, to transform the `FieldToMatch` request component before inspecting it, and they're used in rate\-based rule statements, to transform request components before using them as custom aggregation keys\. If you specify one or more transformations to apply, AWS WAF performs all transformations on the specified content, starting from the lowest priority setting, and then uses the component contents\.   
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-rulegroup-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
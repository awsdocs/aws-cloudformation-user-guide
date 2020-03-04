# AWS::WAFv2::WebACL TextTransformations<a name="aws-properties-wafv2-webacl-texttransformations"></a>

Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content identified by FieldToMatch, from the lowest priority setting up, before inspecting the content for a match\.

## Syntax<a name="aws-properties-wafv2-webacl-texttransformations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-texttransformations-syntax.json"></a>

```
{
  "[TextTransformations](#cfn-wafv2-webacl-texttransformations-texttransformations)" : [ [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-texttransformations-syntax.yaml"></a>

```
  [TextTransformations](#cfn-wafv2-webacl-texttransformations-texttransformations): 
    - [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)
```

## Properties<a name="aws-properties-wafv2-webacl-texttransformations-properties"></a>

`TextTransformations`  <a name="cfn-wafv2-webacl-texttransformations-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content identified by FieldToMatch, from the lowest priority setting up, before inspecting the content for a match\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-webacl-texttransformations) of [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::WAFv2::WebACL SqliMatchStatement<a name="aws-properties-wafv2-webacl-sqlimatchstatement"></a>

Attackers sometimes insert malicious SQL code into web requests in an effort to extract data from your database\. To allow or block web requests that appear to contain malicious SQL code, create one or more SQL injection match conditions\. An SQL injection match condition identifies the part of web requests, such as the URI or the query string, that you want AWS WAF to inspect\. Later in the process, when you create a web ACL, you specify whether to allow or block requests that appear to contain malicious SQL code\.

## Syntax<a name="aws-properties-wafv2-webacl-sqlimatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-sqlimatchstatement-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafv2-webacl-sqlimatchstatement-fieldtomatch)" : FieldToMatch,
  "[TextTransformations](#cfn-wafv2-webacl-sqlimatchstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-sqlimatchstatement-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafv2-webacl-sqlimatchstatement-fieldtomatch): 
    FieldToMatch
  [TextTransformations](#cfn-wafv2-webacl-sqlimatchstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-webacl-sqlimatchstatement-properties"></a>

`FieldToMatch`  <a name="cfn-wafv2-webacl-sqlimatchstatement-fieldtomatch"></a>
The part of a web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-webacl-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-webacl-sqlimatchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
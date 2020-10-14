# AWS::WAFv2::RuleGroup SqliMatchStatement<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Attackers sometimes insert malicious SQL code into web requests in an effort to extract data from your database\. To allow or block web requests that appear to contain malicious SQL code, create one or more SQL injection match conditions\. An SQL injection match condition identifies the part of web requests, such as the URI or the query string, that you want AWS WAF to inspect\. Later in the process, when you create a web ACL, you specify whether to allow or block requests that appear to contain malicious SQL code\.

## Syntax<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafv2-rulegroup-sqlimatchstatement-fieldtomatch)" : FieldToMatch,
  "[TextTransformations](#cfn-wafv2-rulegroup-sqlimatchstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafv2-rulegroup-sqlimatchstatement-fieldtomatch): 
    FieldToMatch
  [TextTransformations](#cfn-wafv2-rulegroup-sqlimatchstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-properties"></a>

`FieldToMatch`  <a name="cfn-wafv2-rulegroup-sqlimatchstatement-fieldtomatch"></a>
The part of a web request that you want AWS WAF to inspect\. For more information, see FieldToMatch\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-rulegroup-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-rulegroup-sqlimatchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-rulegroup-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
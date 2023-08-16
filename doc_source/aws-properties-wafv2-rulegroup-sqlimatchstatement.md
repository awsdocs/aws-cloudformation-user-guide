# AWS::WAFv2::RuleGroup SqliMatchStatement<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement"></a>

A rule statement that inspects for malicious SQL code\. Attackers insert malicious SQL code into web requests to do things like modify your database or extract data from it\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafv2-rulegroup-sqlimatchstatement-fieldtomatch)" : FieldToMatch,
  "[SensitivityLevel](#cfn-wafv2-rulegroup-sqlimatchstatement-sensitivitylevel)" : String,
  "[TextTransformations](#cfn-wafv2-rulegroup-sqlimatchstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafv2-rulegroup-sqlimatchstatement-fieldtomatch): 
    FieldToMatch
  [SensitivityLevel](#cfn-wafv2-rulegroup-sqlimatchstatement-sensitivitylevel): String
  [TextTransformations](#cfn-wafv2-rulegroup-sqlimatchstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-rulegroup-sqlimatchstatement-properties"></a>

`FieldToMatch`  <a name="cfn-wafv2-rulegroup-sqlimatchstatement-fieldtomatch"></a>
The part of the web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-rulegroup-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SensitivityLevel`  <a name="cfn-wafv2-rulegroup-sqlimatchstatement-sensitivitylevel"></a>
The sensitivity that you want AWS WAF to use to inspect for SQL injection attacks\.   
 `HIGH` detects more attacks, but might generate more false positives, especially if your web requests frequently contain unusual strings\. For information about identifying and mitigating false positives, see [Testing and tuning](https://docs.aws.amazon.com/waf/latest/developerguide/web-acl-testing.html) in the * AWS WAF Developer Guide*\.  
 `LOW` is generally a better choice for resources that already have other protections against SQL injection attacks or that have a low tolerance for false positives\.   
Default: `LOW`   
*Required*: No  
*Type*: String  
*Allowed values*: `HIGH | LOW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-rulegroup-sqlimatchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content of the request component identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-rulegroup-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::WAFv2::WebACL XssMatchStatement<a name="aws-properties-wafv2-webacl-xssmatchstatement"></a>

A rule statement that inspects for cross\-site scripting \(XSS\) attacks\. In XSS attacks, the attacker uses vulnerabilities in a benign website as a vehicle to inject malicious client\-site scripts into other legitimate web browsers\. 

## Syntax<a name="aws-properties-wafv2-webacl-xssmatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-xssmatchstatement-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafv2-webacl-xssmatchstatement-fieldtomatch)" : FieldToMatch,
  "[TextTransformations](#cfn-wafv2-webacl-xssmatchstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-xssmatchstatement-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafv2-webacl-xssmatchstatement-fieldtomatch): 
    FieldToMatch
  [TextTransformations](#cfn-wafv2-webacl-xssmatchstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-webacl-xssmatchstatement-properties"></a>

`FieldToMatch`  <a name="cfn-wafv2-webacl-xssmatchstatement-fieldtomatch"></a>
The part of the web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-webacl-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-webacl-xssmatchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content of the request component identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
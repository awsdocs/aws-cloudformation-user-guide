# AWS::WAFv2::WebACL XssMatchStatement<a name="aws-properties-wafv2-webacl-xssmatchstatement"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A rule statement that defines a cross\-site scripting \(XSS\) match search for AWS WAF to apply to web requests\. XSS attacks are those where the attacker uses vulnerabilities in a benign website as a vehicle to inject malicious client\-site scripts into other legitimate web browsers\. The XSS match statement provides the location in requests that you want AWS WAF to search and text transformations to use on the search area before AWS WAF searches for character sequences that are likely to be malicious strings\. 

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
The part of a web request that you want AWS WAF to inspect\. For more information, see FieldToMatch\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-webacl-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-webacl-xssmatchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
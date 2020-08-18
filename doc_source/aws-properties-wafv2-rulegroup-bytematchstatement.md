# AWS::WAFv2::RuleGroup ByteMatchStatement<a name="aws-properties-wafv2-rulegroup-bytematchstatement"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A rule statement that defines a string match search for AWS WAF to apply to web requests\. The byte match statement provides the bytes to search for, the location in requests that you want AWS WAF to search, and other settings\. The bytes to search for are typically a string that corresponds with ASCII characters\. In the AWS WAF console and the developer guide, this is refered to as a string match statement\.

## Syntax<a name="aws-properties-wafv2-rulegroup-bytematchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-bytematchstatement-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafv2-rulegroup-bytematchstatement-fieldtomatch)" : FieldToMatch,
  "[PositionalConstraint](#cfn-wafv2-rulegroup-bytematchstatement-positionalconstraint)" : String,
  "[SearchString](#cfn-wafv2-rulegroup-bytematchstatement-searchstring)" : String,
  "[SearchStringBase64](#cfn-wafv2-rulegroup-bytematchstatement-searchstringbase64)" : String,
  "[TextTransformations](#cfn-wafv2-rulegroup-bytematchstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-bytematchstatement-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafv2-rulegroup-bytematchstatement-fieldtomatch): 
    FieldToMatch
  [PositionalConstraint](#cfn-wafv2-rulegroup-bytematchstatement-positionalconstraint): String
  [SearchString](#cfn-wafv2-rulegroup-bytematchstatement-searchstring): 
    String
  [SearchStringBase64](#cfn-wafv2-rulegroup-bytematchstatement-searchstringbase64): 
    String
  [TextTransformations](#cfn-wafv2-rulegroup-bytematchstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-rulegroup-bytematchstatement-properties"></a>

`FieldToMatch`  <a name="cfn-wafv2-rulegroup-bytematchstatement-fieldtomatch"></a>
The part of a web request that you want AWS WAF to inspect\. For more information, see FieldToMatch\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-rulegroup-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PositionalConstraint`  <a name="cfn-wafv2-rulegroup-bytematchstatement-positionalconstraint"></a>
The area within the portion of a web request that you want AWS WAF to search for `SearchString`\. Valid values include the following:  
 **CONTAINS**   
The specified part of the web request must include the value of `SearchString`, but the location doesn't matter\.  
 **CONTAINS\_WORD**   
The specified part of the web request must include the value of `SearchString`, and `SearchString` must contain only alphanumeric characters or underscore \(A\-Z, a\-z, 0\-9, or \_\)\. In addition, `SearchString` must be a word, which means that both of the following are true:  
+ `SearchString` is at the beginning of the specified part of the web request or is preceded by a character other than an alphanumeric character or underscore \(\_\)\. Examples include the value of a header and `;BadBot`\.
+ `SearchString` is at the end of the specified part of the web request or is followed by a character other than an alphanumeric character or underscore \(\_\), for example, `BadBot;` and `-BadBot;`\.
 **EXACTLY**   
The value of the specified part of the web request must exactly match the value of `SearchString`\.  
 **STARTS\_WITH**   
The value of `SearchString` must appear at the beginning of the specified part of the web request\.  
 **ENDS\_WITH**   
The value of `SearchString` must appear at the end of the specified part of the web request\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTAINS | CONTAINS_WORD | ENDS_WITH | EXACTLY | STARTS_WITH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SearchString`  <a name="cfn-wafv2-rulegroup-bytematchstatement-searchstring"></a>
A string value that you want AWS WAF to search for\. AWS WAF searches only in the part of web requests that you designate for inspection in `FieldToMatch`\. The maximum length of the value is 50 bytes\. For alphabetic characters A\-Z and a\-z, the value is case sensitive\.   
Don't encode this string\. Provide the value that you want AWS WAF to search for\. AWS CloudFormation automatically base64 encodes the value for you\.  
For example, suppose the value of `Type` is `HEADER` and the value of `Data` is `User-Agent`\. If you want to search the `User-Agent` header for the value `BadBot`, you provide the string `BadBot` in the value of `SearchString`\.  
You must specify either `SearchString` or `SearchStringBase64` in a `ByteMatchStatement`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SearchStringBase64`  <a name="cfn-wafv2-rulegroup-bytematchstatement-searchstringbase64"></a>
String to search for in a web request component, base64\-encoded\. If you don't want to encode the string, specify the unencoded value in `SearchString` instead\.   
You must specify either `SearchString` or `SearchStringBase64` in a `ByteMatchStatement`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-rulegroup-bytematchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-rulegroup-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
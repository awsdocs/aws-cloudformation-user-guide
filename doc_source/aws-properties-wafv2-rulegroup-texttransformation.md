# AWS::WAFv2::RuleGroup TextTransformation<a name="aws-properties-wafv2-rulegroup-texttransformation"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-texttransformation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-texttransformation-syntax.json"></a>

```
{
  "[Priority](#cfn-wafv2-rulegroup-texttransformation-priority)" : Integer,
  "[Type](#cfn-wafv2-rulegroup-texttransformation-type)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-texttransformation-syntax.yaml"></a>

```
  [Priority](#cfn-wafv2-rulegroup-texttransformation-priority): Integer
  [Type](#cfn-wafv2-rulegroup-texttransformation-type): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-texttransformation-properties"></a>

`Priority`  <a name="cfn-wafv2-rulegroup-texttransformation-priority"></a>
Sets the relative processing order for multiple transformations that are defined for a rule statement\. AWS WAF processes all transformations, from lowest priority to highest, before inspecting the transformed content\. The priorities don't need to be consecutive, but they must all be different\.   
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-wafv2-rulegroup-texttransformation-type"></a>
You can specify the following transformation types:  
 **CMD\_LINE**   
When you're concerned that attackers are injecting an operating system command line command and using unusual formatting to disguise some or all of the command, use this option to perform the following transformations:  
+ Delete the following characters: \\ " ' ^
+ Delete spaces before the following characters: / \(
+ Replace the following characters with a space: , ;
+ Replace multiple spaces with one space
+ Convert uppercase letters \(A\-Z\) to lowercase \(a\-z\)
 **COMPRESS\_WHITE\_SPACE**   
Use this option to replace the following characters with a space character \(decimal 32\):  
+ \\f, formfeed, decimal 12
+ \\t, tab, decimal 9
+ \\n, newline, decimal 10
+ \\r, carriage return, decimal 13
+ \\v, vertical tab, decimal 11
+ non\-breaking space, decimal 160
`COMPRESS_WHITE_SPACE` also replaces multiple spaces with one space\.  
 **HTML\_ENTITY\_DECODE**   
Use this option to replace HTML\-encoded characters with unencoded characters\. `HTML_ENTITY_DECODE` performs the following operations:  
+ Replaces `(ampersand)quot;` with `"` 
+ Replaces `(ampersand)nbsp;` with a non\-breaking space, decimal 160
+ Replaces `(ampersand)lt;` with a "less than" symbol
+ Replaces `(ampersand)gt;` with `>` 
+ Replaces characters that are represented in hexadecimal format, `(ampersand)#xhhhh;`, with the corresponding characters
+ Replaces characters that are represented in decimal format, `(ampersand)#nnnn;`, with the corresponding characters
 **LOWERCASE**   
Use this option to convert uppercase letters \(A\-Z\) to lowercase \(a\-z\)\.  
 **URL\_DECODE**   
Use this option to decode a URL\-encoded value\.  
 **NONE**   
Specify `NONE` if you don't want any text transformations\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CMD_LINE | COMPRESS_WHITE_SPACE | HTML_ENTITY_DECODE | LOWERCASE | NONE | URL_DECODE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
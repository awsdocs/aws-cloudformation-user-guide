# AWS::WAFRegional::XssMatchSet XssMatchTuple<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple"></a>

**Note**  
This is **AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF**, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

Specifies the part of a web request that you want AWS WAF to inspect for cross\-site scripting attacks and, if you want AWS WAF to inspect a header, the name of the header\.

## Syntax<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch)" : FieldToMatch,
  "[TextTransformation](#cfn-wafregional-xssmatchset-xssmatchtuple-texttransformation)" : String
}
```

### YAML<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch): 
    FieldToMatch
  [TextTransformation](#cfn-wafregional-xssmatchset-xssmatchtuple-texttransformation): String
```

## Properties<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-properties"></a>

`FieldToMatch`  <a name="cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch"></a>
Specifies where in a web request to look for cross\-site scripting attacks\.  
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafregional-xssmatchset-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformation`  <a name="cfn-wafregional-xssmatchset-xssmatchtuple-texttransformation"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass AWS WAF\. If you specify a transformation, AWS WAF performs the transformation on `FieldToMatch` before inspecting it for a match\.  
You can only specify a single type of TextTransformation\.  
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
Specify `NONE` if you don't want to perform any text transformations\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CMD_LINE | COMPRESS_WHITE_SPACE | HTML_ENTITY_DECODE | LOWERCASE | NONE | URL_DECODE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
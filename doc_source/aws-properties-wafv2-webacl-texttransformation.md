# AWS::WAFv2::WebACL TextTransformation<a name="aws-properties-wafv2-webacl-texttransformation"></a>

Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. 

## Syntax<a name="aws-properties-wafv2-webacl-texttransformation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-texttransformation-syntax.json"></a>

```
{
  "[Priority](#cfn-wafv2-webacl-texttransformation-priority)" : Integer,
  "[Type](#cfn-wafv2-webacl-texttransformation-type)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-texttransformation-syntax.yaml"></a>

```
  [Priority](#cfn-wafv2-webacl-texttransformation-priority): Integer
  [Type](#cfn-wafv2-webacl-texttransformation-type): String
```

## Properties<a name="aws-properties-wafv2-webacl-texttransformation-properties"></a>

`Priority`  <a name="cfn-wafv2-webacl-texttransformation-priority"></a>
Sets the relative processing order for multiple transformations\. AWS WAF processes all transformations, from lowest priority to highest, before inspecting the transformed content\. The priorities don't need to be consecutive, but they must all be different\.   
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-wafv2-webacl-texttransformation-type"></a>
For detailed descriptions of each of the transformation types, see [Text transformations](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-transformation.html) in the * AWS WAF Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `BASE64_DECODE | BASE64_DECODE_EXT | CMD_LINE | COMPRESS_WHITE_SPACE | CSS_DECODE | ESCAPE_SEQ_DECODE | HEX_DECODE | HTML_ENTITY_DECODE | JS_DECODE | LOWERCASE | MD5 | NONE | NORMALIZE_PATH | NORMALIZE_PATH_WIN | REMOVE_NULLS | REPLACE_COMMENTS | REPLACE_NULLS | SQL_HEX_DECODE | URL_DECODE | URL_DECODE_UNI | UTF8_TO_UNICODE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::WAFv2::WebACL Cookies<a name="aws-properties-wafv2-webacl-cookies"></a>

Inspect the cookies in the web request\. You can specify the parts of the cookies to inspect and you can narrow the set of cookies to inspect by including or excluding specific keys\.

This is used to indicate the web request component to inspect, in the `FieldToMatch` specification\. 

Example JSON: `"Cookies": { "MatchPattern": { "All": {} }, "MatchScope": "KEY", "OversizeHandling": "MATCH" }` 

## Syntax<a name="aws-properties-wafv2-webacl-cookies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-cookies-syntax.json"></a>

```
{
  "[MatchPattern](#cfn-wafv2-webacl-cookies-matchpattern)" : CookieMatchPattern,
  "[MatchScope](#cfn-wafv2-webacl-cookies-matchscope)" : String,
  "[OversizeHandling](#cfn-wafv2-webacl-cookies-oversizehandling)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-cookies-syntax.yaml"></a>

```
  [MatchPattern](#cfn-wafv2-webacl-cookies-matchpattern): 
    CookieMatchPattern
  [MatchScope](#cfn-wafv2-webacl-cookies-matchscope): String
  [OversizeHandling](#cfn-wafv2-webacl-cookies-oversizehandling): String
```

## Properties<a name="aws-properties-wafv2-webacl-cookies-properties"></a>

`MatchPattern`  <a name="cfn-wafv2-webacl-cookies-matchpattern"></a>
The filter to use to identify the subset of cookies to inspect in a web request\.   
You must specify exactly one setting: either `All`, `IncludedCookies`, or `ExcludedCookies`\.  
Example JSON: `"MatchPattern": { "IncludedCookies": {"KeyToInclude1", "KeyToInclude2", "KeyToInclude3"} }`   
*Required*: Yes  
*Type*: [CookieMatchPattern](aws-properties-wafv2-webacl-cookiematchpattern.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchScope`  <a name="cfn-wafv2-webacl-cookies-matchscope"></a>
The parts of the cookies to inspect with the rule inspection criteria\. If you specify `All`, AWS WAF inspects both keys and values\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL | KEY | VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OversizeHandling`  <a name="cfn-wafv2-webacl-cookies-oversizehandling"></a>
What AWS WAF should do if the cookies of the request are larger than AWS WAF can inspect\. AWS WAF does not support inspecting the entire contents of request cookies when they exceed 8 KB \(8192 bytes\) or 200 total cookies\. The underlying host service forwards a maximum of 200 cookies and at most 8 KB of cookie contents to AWS WAF\.   
The options for oversize handling are the following:  
+  `CONTINUE` \- Inspect the cookies normally, according to the rule inspection criteria\. 
+  `MATCH` \- Treat the web request as matching the rule statement\. AWS WAF applies the rule action to the request\.
+  `NO_MATCH` \- Treat the web request as not matching the rule statement\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTINUE | MATCH | NO_MATCH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-cookies--examples"></a>



### Set the Cookies specification<a name="aws-properties-wafv2-webacl-cookies--examples--Set_the_Cookies_specification_"></a>

The following shows an example Cookies field to match specification\. 

#### YAML<a name="aws-properties-wafv2-webacl-cookies--examples--Set_the_Cookies_specification_--yaml"></a>

```
FieldToMatch:
  Cookies:
    MatchPattern:
      IncludedCookies:
      - "session-id"
      - "session-id-time"
    MatchScope: ALL 
    OversizeHandling: MATCH
```

#### JSON<a name="aws-properties-wafv2-webacl-cookies--examples--Set_the_Cookies_specification_--json"></a>

```
"FieldToMatch": {
  "Cookies": {
    "MatchPattern": {
      "IncludedCookies": [
        "session-id",
        "session-id-time"
      ]
    },
    "MatchScope": "ALL",
    "OversizeHandling": "MATCH" 
  }
}
```
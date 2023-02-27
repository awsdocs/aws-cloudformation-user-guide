# AWS::WAFv2::RuleGroup Headers<a name="aws-properties-wafv2-rulegroup-headers"></a>

Inspect all headers in the web request\. You can specify the parts of the headers to inspect and you can narrow the set of headers to inspect by including or excluding specific keys\.

This is used to indicate the web request component to inspect, in the `FieldToMatch` specification\. 

If you want to inspect just the value of a single header, use the `SingleHeader` `FieldToMatch` setting instead\.

Example JSON: `"Headers": { "MatchPattern": { "All": {} }, "MatchScope": "KEY", "OversizeHandling": "MATCH" }` 

## Syntax<a name="aws-properties-wafv2-rulegroup-headers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-headers-syntax.json"></a>

```
{
  "[MatchPattern](#cfn-wafv2-rulegroup-headers-matchpattern)" : HeaderMatchPattern,
  "[MatchScope](#cfn-wafv2-rulegroup-headers-matchscope)" : String,
  "[OversizeHandling](#cfn-wafv2-rulegroup-headers-oversizehandling)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-headers-syntax.yaml"></a>

```
  [MatchPattern](#cfn-wafv2-rulegroup-headers-matchpattern): 
    HeaderMatchPattern
  [MatchScope](#cfn-wafv2-rulegroup-headers-matchscope): String
  [OversizeHandling](#cfn-wafv2-rulegroup-headers-oversizehandling): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-headers-properties"></a>

`MatchPattern`  <a name="cfn-wafv2-rulegroup-headers-matchpattern"></a>
The filter to use to identify the subset of headers to inspect in a web request\.   
You must specify exactly one setting: either `All`, `IncludedHeaders`, or `ExcludedHeaders`\.  
Example JSON: `"MatchPattern": { "ExcludedHeaders": {"KeyToExclude1", "KeyToExclude2"} }`   
*Required*: Yes  
*Type*: [HeaderMatchPattern](aws-properties-wafv2-rulegroup-headermatchpattern.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchScope`  <a name="cfn-wafv2-rulegroup-headers-matchscope"></a>
The parts of the headers to match with the rule inspection criteria\. If you specify `All`, AWS WAF inspects both keys and values\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL | KEY | VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OversizeHandling`  <a name="cfn-wafv2-rulegroup-headers-oversizehandling"></a>
What AWS WAF should do if the headers of the request are larger than AWS WAF can inspect\. AWS WAF does not support inspecting the entire contents of request headers when they exceed 8 KB \(8192 bytes\) or 200 total headers\. The underlying host service forwards a maximum of 200 headers and at most 8 KB of header contents to AWS WAF\.   
The options for oversize handling are the following:  
+  `CONTINUE` \- Inspect the headers normally, according to the rule inspection criteria\. 
+  `MATCH` \- Treat the web request as matching the rule statement\. AWS WAF applies the rule action to the request\.
+  `NO_MATCH` \- Treat the web request as not matching the rule statement\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTINUE | MATCH | NO_MATCH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-rulegroup-headers--examples"></a>



### Set the Headers specification<a name="aws-properties-wafv2-rulegroup-headers--examples--Set_the_Headers_specification_"></a>

The following shows an example Headers field to match specification\. 

#### YAML<a name="aws-properties-wafv2-rulegroup-headers--examples--Set_the_Headers_specification_--yaml"></a>

```
FieldToMatch:
  Headers:
    MatchPattern:
      IncludedHeaders:
      - "User-Agent"
      - "Referer"
    MatchScope: ALL 
    OversizeHandling: MATCH
```

#### JSON<a name="aws-properties-wafv2-rulegroup-headers--examples--Set_the_Headers_specification_--json"></a>

```
"FieldToMatch": {
  "Headers": {
    "MatchPattern": {
      "IncludedHeaders": [
        "User-Agent",
        "Referer"
      ]
    },
    "MatchScope": "ALL",
    "OversizeHandling": "MATCH" 
  }
}
```
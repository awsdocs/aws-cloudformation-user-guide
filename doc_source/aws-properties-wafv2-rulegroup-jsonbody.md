# AWS::WAFv2::RuleGroup JsonBody<a name="aws-properties-wafv2-rulegroup-jsonbody"></a>

Inspect the body of the web request as JSON\. The body immediately follows the request headers\. 

This is used to indicate the web request component to inspect, in the [FieldToMatch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-xssmatchstatement.html#cfn-wafv2-rulegroup-xssmatchstatement-fieldtomatch) specification\. 

Use the specifications in this object to indicate which parts of the JSON body to inspect using the rule's inspection criteria\. AWS WAF inspects only the parts of the JSON that result from the matches that you indicate\. 

Example JSON: `"JsonBody": { "MatchPattern": { "All": {} }, "MatchScope": "ALL" }` 

## Syntax<a name="aws-properties-wafv2-rulegroup-jsonbody-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-jsonbody-syntax.json"></a>

```
{
  "[InvalidFallbackBehavior](#cfn-wafv2-rulegroup-jsonbody-invalidfallbackbehavior)" : String,
  "[MatchPattern](#cfn-wafv2-rulegroup-jsonbody-matchpattern)" : JsonMatchPattern,
  "[MatchScope](#cfn-wafv2-rulegroup-jsonbody-matchscope)" : String,
  "[OversizeHandling](#cfn-wafv2-rulegroup-jsonbody-oversizehandling)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-jsonbody-syntax.yaml"></a>

```
  [InvalidFallbackBehavior](#cfn-wafv2-rulegroup-jsonbody-invalidfallbackbehavior): String
  [MatchPattern](#cfn-wafv2-rulegroup-jsonbody-matchpattern): 
    JsonMatchPattern
  [MatchScope](#cfn-wafv2-rulegroup-jsonbody-matchscope): String
  [OversizeHandling](#cfn-wafv2-rulegroup-jsonbody-oversizehandling): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-jsonbody-properties"></a>

`InvalidFallbackBehavior`  <a name="cfn-wafv2-rulegroup-jsonbody-invalidfallbackbehavior"></a>
What AWS WAF should do if it fails to completely parse the JSON body\. The options are the following:  
+  `EVALUATE_AS_STRING` \- Inspect the body as plain text\. AWS WAF applies the text transformations and inspection criteria that you defined for the JSON inspection to the body text string\.
+  `MATCH` \- Treat the web request as matching the rule statement\. AWS WAF applies the rule action to the request\.
+  `NO_MATCH` \- Treat the web request as not matching the rule statement\.
If you don't provide this setting, AWS WAF parses and evaluates the content only up to the first parsing failure that it encounters\.   
 AWS WAF does its best to parse the entire JSON body, but might be forced to stop for reasons such as invalid characters, duplicate keys, truncation, and any content whose root node isn't an object or an array\.   
 AWS WAF parses the JSON in the following examples as two valid key, value pairs:   
+ Missing comma: `{"key1":"value1""key2":"value2"}` 
+ Missing colon: `{"key1":"value1","key2""value2"}` 
+ Extra colons: `{"key1"::"value1","key2""value2"}` 
*Required*: No  
*Type*: String  
*Allowed values*: `EVALUATE_AS_STRING | MATCH | NO_MATCH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchPattern`  <a name="cfn-wafv2-rulegroup-jsonbody-matchpattern"></a>
The patterns to look for in the JSON body\. AWS WAF inspects the results of these pattern matches against the rule inspection criteria\.   
*Required*: Yes  
*Type*: [JsonMatchPattern](aws-properties-wafv2-rulegroup-jsonmatchpattern.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchScope`  <a name="cfn-wafv2-rulegroup-jsonbody-matchscope"></a>
The parts of the JSON to match against using the `MatchPattern`\. If you specify `All`, AWS WAF matches against keys and values\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL | KEY | VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OversizeHandling`  <a name="cfn-wafv2-rulegroup-jsonbody-oversizehandling"></a>
What AWS WAF should do if the body is larger than AWS WAF can inspect\. AWS WAF does not support inspecting the entire contents of the body of a web request when the body exceeds 8 KB \(8192 bytes\)\. Only the first 8 KB of the request body are forwarded to AWS WAF by the underlying host service\.   
The options for oversize handling are the following:  
+  `CONTINUE` \- Inspect the body normally, according to the rule inspection criteria\. 
+  `MATCH` \- Treat the web request as matching the rule statement\. AWS WAF applies the rule action to the request\.
+  `NO_MATCH` \- Treat the web request as not matching the rule statement\.
You can combine the `MATCH` or `NO_MATCH` settings for oversize handling with your rule and web ACL action settings, so that you block any request whose body is over 8 KB\.   
Default: `CONTINUE`   
*Required*: No  
*Type*: String  
*Allowed values*: `CONTINUE | MATCH | NO_MATCH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-rulegroup-jsonbody--examples"></a>



### Set the JSON body specification<a name="aws-properties-wafv2-rulegroup-jsonbody--examples--Set_the_JSON_body_specification_"></a>

The following shows an example JSON body field to match specification\. 

#### YAML<a name="aws-properties-wafv2-rulegroup-jsonbody--examples--Set_the_JSON_body_specification_--yaml"></a>

```
FieldToMatch:
  JsonBody:
    MatchPattern:
      IncludedPaths:
      - "/dogs/0/name"
      - "/cats/0/name"
    MatchScope: ALL
    InvalidFallbackBehavior: EVALUATE_AS_STRING 
    OversizeHandling: MATCH
```

#### JSON<a name="aws-properties-wafv2-rulegroup-jsonbody--examples--Set_the_JSON_body_specification_--json"></a>

```
"FieldToMatch": {
  "JsonBody": {
    "MatchPattern": {
      "IncludedPaths": [
        "/dogs/0/name",
        "/cats/0/name"
      ]
    },
    "MatchScope": "ALL",
    "InvalidFallbackBehavior": "EVALUATE_AS_STRING",
    "OversizeHandling": "MATCH" 
  }
}
```
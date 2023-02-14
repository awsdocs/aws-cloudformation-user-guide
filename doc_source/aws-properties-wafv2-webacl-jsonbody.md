# AWS::WAFv2::WebACL JsonBody<a name="aws-properties-wafv2-webacl-jsonbody"></a>

The body of a web request, inspected as JSON\. The body immediately follows the request headers\. This is used in the `FieldToMatch` specification\.

Use the specifications in this object to indicate which parts of the JSON body to inspect using the rule's inspection criteria\. AWS WAF inspects only the parts of the JSON that result from the matches that you indicate\. 

## Syntax<a name="aws-properties-wafv2-webacl-jsonbody-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-jsonbody-syntax.json"></a>

```
{
  "[InvalidFallbackBehavior](#cfn-wafv2-webacl-jsonbody-invalidfallbackbehavior)" : String,
  "[MatchPattern](#cfn-wafv2-webacl-jsonbody-matchpattern)" : JsonMatchPattern,
  "[MatchScope](#cfn-wafv2-webacl-jsonbody-matchscope)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-jsonbody-syntax.yaml"></a>

```
  [InvalidFallbackBehavior](#cfn-wafv2-webacl-jsonbody-invalidfallbackbehavior): String
  [MatchPattern](#cfn-wafv2-webacl-jsonbody-matchpattern): 
    JsonMatchPattern
  [MatchScope](#cfn-wafv2-webacl-jsonbody-matchscope): String
```

## Properties<a name="aws-properties-wafv2-webacl-jsonbody-properties"></a>

`InvalidFallbackBehavior`  <a name="cfn-wafv2-webacl-jsonbody-invalidfallbackbehavior"></a>
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

`MatchPattern`  <a name="cfn-wafv2-webacl-jsonbody-matchpattern"></a>
The patterns to look for in the JSON body\. AWS WAF inspects the results of these pattern matches against the rule inspection criteria\.   
*Required*: Yes  
*Type*: [JsonMatchPattern](aws-properties-wafv2-webacl-jsonmatchpattern.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchScope`  <a name="cfn-wafv2-webacl-jsonbody-matchscope"></a>
The parts of the JSON to match against using the `MatchPattern`\. If you specify `All`, AWS WAF matches against keys and values\.   
Valid Values: `ALL` \| `KEY` \| `VALUE`  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL | KEY | VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-jsonbody--examples"></a>



### Set the JSON body specification<a name="aws-properties-wafv2-webacl-jsonbody--examples--Set_the_JSON_body_specification_"></a>

The following shows an example JSON body field to match specification\. 

#### YAML<a name="aws-properties-wafv2-webacl-jsonbody--examples--Set_the_JSON_body_specification_--yaml"></a>

```
FieldToMatch:
  JsonBody:
    MatchPattern:
      IncludedPaths:
      - "/dogs/0/name"
      - "/cats/0/name"
    MatchScope: ALL
    InvalidFallbackBehavior: EVALUATE_AS_STRING
```

#### JSON<a name="aws-properties-wafv2-webacl-jsonbody--examples--Set_the_JSON_body_specification_--json"></a>

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
    "InvalidFallbackBehavior": "EVALUATE_AS_STRING"
   }
```
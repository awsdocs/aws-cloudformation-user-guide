# AWS::WAFv2::WebACL HeaderMatchPattern<a name="aws-properties-wafv2-webacl-headermatchpattern"></a>

The filter to use to identify the subset of headers to inspect in a web request\. 

You must specify exactly one setting: either `All`, `IncludedHeaders`, or `ExcludedHeaders`\.

Example JSON: `"MatchPattern": { "ExcludedHeaders": {"KeyToExclude1", "KeyToExclude2"} }` 

## Syntax<a name="aws-properties-wafv2-webacl-headermatchpattern-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-headermatchpattern-syntax.json"></a>

```
{
  "[All](#cfn-wafv2-webacl-headermatchpattern-all)" : Json,
  "[ExcludedHeaders](#cfn-wafv2-webacl-headermatchpattern-excludedheaders)" : [ String, ... ],
  "[IncludedHeaders](#cfn-wafv2-webacl-headermatchpattern-includedheaders)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-headermatchpattern-syntax.yaml"></a>

```
  [All](#cfn-wafv2-webacl-headermatchpattern-all): Json
  [ExcludedHeaders](#cfn-wafv2-webacl-headermatchpattern-excludedheaders): 
    - String
  [IncludedHeaders](#cfn-wafv2-webacl-headermatchpattern-includedheaders): 
    - String
```

## Properties<a name="aws-properties-wafv2-webacl-headermatchpattern-properties"></a>

`All`  <a name="cfn-wafv2-webacl-headermatchpattern-all"></a>
Inspect all headers\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludedHeaders`  <a name="cfn-wafv2-webacl-headermatchpattern-excludedheaders"></a>
Inspect only the headers whose keys don't match any of the strings specified here\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `199`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludedHeaders`  <a name="cfn-wafv2-webacl-headermatchpattern-includedheaders"></a>
Inspect only the headers that have a key that matches one of the strings specified here\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `199`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-headermatchpattern--examples"></a>



### Set a header match pattern for all paths<a name="aws-properties-wafv2-webacl-headermatchpattern--examples--Set_a_header_match_pattern_for_all_paths_"></a>

The following shows an example header match pattern specification for all paths\. 

#### YAML<a name="aws-properties-wafv2-webacl-headermatchpattern--examples--Set_a_header_match_pattern_for_all_paths_--yaml"></a>

```
MatchPattern:
  All: {}
```

#### JSON<a name="aws-properties-wafv2-webacl-headermatchpattern--examples--Set_a_header_match_pattern_for_all_paths_--json"></a>

```
"MatchPattern": {
  "All": {}
}
```

### Set a header match pattern with included paths<a name="aws-properties-wafv2-webacl-headermatchpattern--examples--Set_a_header_match_pattern_with_included_paths_"></a>

The following shows an example header match pattern specification with included paths\. 

#### YAML<a name="aws-properties-wafv2-webacl-headermatchpattern--examples--Set_a_header_match_pattern_with_included_paths_--yaml"></a>

```
MatchPattern:
  IncludedHeaders:
      - "User-Agent"
      - "Referer"
```

#### JSON<a name="aws-properties-wafv2-webacl-headermatchpattern--examples--Set_a_header_match_pattern_with_included_paths_--json"></a>

```
"MatchPattern": {
  "IncludedHeaders": [
    "User-Agent",
    "Referer"
  ]
}
```
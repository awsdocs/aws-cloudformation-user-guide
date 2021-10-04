# AWS::WAFv2::WebACL JsonMatchPattern<a name="aws-properties-wafv2-webacl-jsonmatchpattern"></a>

The patterns to look for in the JSON body\. AWS WAF inspects the results of these pattern matches against the rule inspection criteria\. This is used with the `FieldToMatch` option `JsonBody`\. 

## Syntax<a name="aws-properties-wafv2-webacl-jsonmatchpattern-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-jsonmatchpattern-syntax.json"></a>

```
{
  "[All](#cfn-wafv2-webacl-jsonmatchpattern-all)" : Json,
  "[IncludedPaths](#cfn-wafv2-webacl-jsonmatchpattern-includedpaths)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-jsonmatchpattern-syntax.yaml"></a>

```
  [All](#cfn-wafv2-webacl-jsonmatchpattern-all): Json
  [IncludedPaths](#cfn-wafv2-webacl-jsonmatchpattern-includedpaths): 
    - String
```

## Properties<a name="aws-properties-wafv2-webacl-jsonmatchpattern-properties"></a>

`All`  <a name="cfn-wafv2-webacl-jsonmatchpattern-all"></a>
Match all of the elements\. See also `MatchScope` in `JsonBody`\.   
You must specify either this setting or the `IncludedPaths` setting, but not both\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludedPaths`  <a name="cfn-wafv2-webacl-jsonmatchpattern-includedpaths"></a>
Match only the specified include paths\. See also `MatchScope` in `JsonBody`\.   
Provide the include paths using JSON Pointer syntax\. For example, `"IncludedPaths": ["/dogs/0/name", "/dogs/1/name"]`\. For information about this syntax, see the Internet Engineering Task Force \(IETF\) documentation [JavaScript Object Notation \(JSON\) Pointer](https://tools.ietf.org/html/rfc6901)\.   
You must specify either this setting or the `All` setting, but not both\.  
Don't use this option to include all paths\. Instead, use the `All` setting\. 
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-jsonmatchpattern--examples"></a>



### Set a JSON match pattern for all paths<a name="aws-properties-wafv2-webacl-jsonmatchpattern--examples--Set_a_JSON_match_pattern_for_all_paths_"></a>

The following shows an example JSON match pattern specification for all paths\. 

#### YAML<a name="aws-properties-wafv2-webacl-jsonmatchpattern--examples--Set_a_JSON_match_pattern_for_all_paths_--yaml"></a>

```
MatchPattern:
  All: {}
```

#### JSON<a name="aws-properties-wafv2-webacl-jsonmatchpattern--examples--Set_a_JSON_match_pattern_for_all_paths_--json"></a>

```
"MatchPattern": {
  "All": {}
}
```

### Set a JSON match pattern with included paths<a name="aws-properties-wafv2-webacl-jsonmatchpattern--examples--Set_a_JSON_match_pattern_with_included_paths_"></a>

The following shows an example JSON match pattern specification with included paths\. 

#### YAML<a name="aws-properties-wafv2-webacl-jsonmatchpattern--examples--Set_a_JSON_match_pattern_with_included_paths_--yaml"></a>

```
MatchPattern:
  IncludedPaths:
    - "/dogs/0/name"
    - "/cats/0/name"
```

#### JSON<a name="aws-properties-wafv2-webacl-jsonmatchpattern--examples--Set_a_JSON_match_pattern_with_included_paths_--json"></a>

```
"MatchPattern": {
  "IncludedPaths": [
    "/dogs/0/name",
    "/cats/0/name"
  ]
}
```
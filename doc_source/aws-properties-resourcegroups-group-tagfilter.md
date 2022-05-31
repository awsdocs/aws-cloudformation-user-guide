# AWS::ResourceGroups::Group TagFilter<a name="aws-properties-resourcegroups-group-tagfilter"></a>

Specifies a single tag key and optional values that you can use to specify membership in a tag\-based group\. An AWS resource that doesn't have a matching tag key and value is rejected as a member of the group\.

A `TagFilter` object includes two properties: `Key` \(a string\) and `Values` \(a list of strings\)\. Only resources in the account that are tagged with a matching key\-value pair are members of the group\. The `Values` property of `TagFilter` is optional, but specifying it narrows the query results\.

As an example, suppose the `TagFilters` string is `[{"Key": "Stage", "Values": ["Test", "Beta"]}, {"Key": "Storage"}]`\. In this case, only resources with all of the following tags are members of the group:
+ `Stage` tag key with a value of either `Test` or `Beta`
+ `Storage` tag key with any value

## Syntax<a name="aws-properties-resourcegroups-group-tagfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resourcegroups-group-tagfilter-syntax.json"></a>

```
{
  "[Key](#cfn-resourcegroups-group-tagfilter-key)" : String,
  "[Values](#cfn-resourcegroups-group-tagfilter-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-resourcegroups-group-tagfilter-syntax.yaml"></a>

```
  [Key](#cfn-resourcegroups-group-tagfilter-key): String
  [Values](#cfn-resourcegroups-group-tagfilter-values): 
    - String
```

## Properties<a name="aws-properties-resourcegroups-group-tagfilter-properties"></a>

`Key`  <a name="cfn-resourcegroups-group-tagfilter-key"></a>
A string that defines a tag key\. Only resources in the account that are tagged with a specified tag key are members of the tag\-based resource group\.  
This field is required when the `ResourceQuery` structure's `Type` property is `TAG_FILTERS_1_0`\. You must specify at least one tag key\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-resourcegroups-group-tagfilter-values"></a>
A list of tag values that can be included in the tag\-based resource group\. This is optional\. If you don't specify a value or values for a key, then an AWS resource with any value for that key is a member\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
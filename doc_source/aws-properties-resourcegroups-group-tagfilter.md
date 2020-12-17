# AWS::ResourceGroups::Group TagFilter<a name="aws-properties-resourcegroups-group-tagfilter"></a>

The `TagFilter` object used to define tag\-based group membership\. 

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
A string that defines a tag key\. Only resources in the account that are tagged with a specified tag key are members of the tag\-based resource group\. This field is required when the `ResourceQuery.Type` property is `TAG_FILTERS_1_0`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-resourcegroups-group-tagfilter-values"></a>
A list of tag values that can be included in the tag\-based resource group\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
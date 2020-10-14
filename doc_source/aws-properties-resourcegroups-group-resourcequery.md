# AWS::ResourceGroups::Group ResourceQuery<a name="aws-properties-resourcegroups-group-resourcequery"></a>

The query used to define a group\.

## Syntax<a name="aws-properties-resourcegroups-group-resourcequery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resourcegroups-group-resourcequery-syntax.json"></a>

```
{
  "[Query](#cfn-resourcegroups-group-resourcequery-query)" : Query,
  "[Type](#cfn-resourcegroups-group-resourcequery-type)" : String
}
```

### YAML<a name="aws-properties-resourcegroups-group-resourcequery-syntax.yaml"></a>

```
  [Query](#cfn-resourcegroups-group-resourcequery-query): 
    Query
  [Type](#cfn-resourcegroups-group-resourcequery-type): String
```

## Properties<a name="aws-properties-resourcegroups-group-resourcequery-properties"></a>

`Query`  <a name="cfn-resourcegroups-group-resourcequery-query"></a>
The query that defines a group\. This field is required when the type is `TAG_FILTERS_1_0`\.  
*Required*: Conditional  
*Type*: [Query](aws-properties-resourcegroups-group-query.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-resourcegroups-group-resourcequery-type"></a>
The valid types are `TAG_FILTERS_1_0` and `CLOUDFORMATION_STACK_1_0.` Each type requires specific attributes for the `Query` object:  
+ `TAG_FILTERS_1_0` indicates that the group is a tag\-based group\. Group membership is defined by the query's `TagFilters` property\. Specify the tag filters to use in the query\.
+ `CLOUDFORMATION_STACK_1_0`, the default, indicates that the group is a CloudFormation stack\-based group\. Group membership is based on the CloudFormation stack\. Specify the `StackIdentifier` property in the query to define which stack to associate the group with, or leave it empty to default to the stack where the group is defined\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
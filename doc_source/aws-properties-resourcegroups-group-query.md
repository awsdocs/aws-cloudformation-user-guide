# AWS::ResourceGroups::Group Query<a name="aws-properties-resourcegroups-group-query"></a>

A mapping of a query attached to a resource group that determines the AWS resources that are members of the group\.

## Syntax<a name="aws-properties-resourcegroups-group-query-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resourcegroups-group-query-syntax.json"></a>

```
{
  "[ResourceTypeFilters](#cfn-resourcegroups-group-query-resourcetypefilters)" : [ String, ... ],
  "[StackIdentifier](#cfn-resourcegroups-group-query-stackidentifier)" : String,
  "[TagFilters](#cfn-resourcegroups-group-query-tagfilters)" : [ TagFilter, ... ]
}
```

### YAML<a name="aws-properties-resourcegroups-group-query-syntax.yaml"></a>

```
  [ResourceTypeFilters](#cfn-resourcegroups-group-query-resourcetypefilters): 
    - String
  [StackIdentifier](#cfn-resourcegroups-group-query-stackidentifier): String
  [TagFilters](#cfn-resourcegroups-group-query-tagfilters): 
    - TagFilter
```

## Properties<a name="aws-properties-resourcegroups-group-query-properties"></a>

`ResourceTypeFilters`  <a name="cfn-resourcegroups-group-query-resourcetypefilters"></a>
The resource types that can be part of the resource group\. For example, if `ResourceTypeFilters` is `["AWS::EC2::Instance", "AWS::DynamoDB::Table"]`, only EC2 Instance resources or DynamoDB Table resources can be members of this resource group\. The default value is `["AWS::AllSupported"]`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackIdentifier`  <a name="cfn-resourcegroups-group-query-stackidentifier"></a>
The CFN Stack ARN\. When specified, all supported resources of the CFN stack are members of the resource group\. The default value is an identifier of the current stack, which means that all the resources of the current stack are grouped\.  
Only specify a value for `StackIdentifier` when the `ResourceQuery.Type` property is `CLOUDFORMATION_STACK_1_0.`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilters`  <a name="cfn-resourcegroups-group-query-tagfilters"></a>
A list of key\-value pair objects that limit which resources are members of a group\. This property is required when the `ResourceQuery.Type` property is `TAG_FILTERS_1_0`\.  
`TagFilter` objects include two properties: `Key` \(a string\) and `Values` \(a list of strings\)\. Only resources in the account that are tagged with an allowed key\-value pair are members of the group\. The `Values` property of `TagFilter` is optional, but specifying it narrows the query results\. For example, suppose `TagFilters` is `[{"Key": "Stage", "Values": ["Test", "Beta"]}, {"Key": "Storage"}]`\. In this case, only resources with all of the following tags are members of the group:  
+ `Stage` tag key with a value of either `Test` or `Beta`
+ `Storage` tag key with any value
*Required*: Conditional  
*Type*: List of [TagFilter](aws-properties-resourcegroups-group-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
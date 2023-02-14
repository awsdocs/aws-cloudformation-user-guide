# AWS::ResourceGroups::Group Query<a name="aws-properties-resourcegroups-group-query"></a>

Specifies details within a `ResourceQuery` structure that determines the membership of the resource group\. The contents required in the `Query` structure are determined by the `Type` property of the containing `ResourceQuery` structure\.

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
Specifies limits to the types of resources that can be included in the resource group\. For example, if `ResourceTypeFilters` is `["AWS::EC2::Instance", "AWS::DynamoDB::Table"]`, only EC2 instances or DynamoDB tables can be members of this resource group\. The default value is `["AWS::AllSupported"]`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackIdentifier`  <a name="cfn-resourcegroups-group-query-stackidentifier"></a>
Specifies the ARN of a CloudFormation stack\. All supported resources of the CloudFormation stack are members of the resource group\. If you don't specify an ARN, this parameter defaults to the current stack that you are defining, which means that all the resources of the current stack are grouped\.  
You can specify a value for `StackIdentifier` only when the `ResourceQuery.Type` property is `CLOUDFORMATION_STACK_1_0.`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilters`  <a name="cfn-resourcegroups-group-query-tagfilters"></a>
A list of key\-value pair objects that limit which resources can be members of the resource group\. This property is required when the `ResourceQuery.Type` property is `TAG_FILTERS_1_0`\.  
A resource must have a tag that matches every filter that is provided in the `TagFilters` list\.  
*Required*: Conditional  
*Type*: List of [TagFilter](aws-properties-resourcegroups-group-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::ResourceGroups::Group<a name="aws-resource-resourcegroups-group"></a>

Creates a resource group with the specified name and description\. You can optionally include a resource query, or a service configuration\. For more information about constructing a resource query, see [Create a tag\-based group in Resource Groups](https://docs.aws.amazon.com/ARG/latest/userguide/gettingstarted-query.html#gettingstarted-query-cli-tag)\. For more information about service configurations, see [Service configurations for resource groups](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html)\.

 **Minimum permissions** 

To run this command, you must have the following permissions:
+  `resource-groups:CreateGroup` 

## Syntax<a name="aws-resource-resourcegroups-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-resourcegroups-group-syntax.json"></a>

```
{
  "Type" : "AWS::ResourceGroups::Group",
  "Properties" : {
      "[Description](#cfn-resourcegroups-group-description)" : String,
      "[Name](#cfn-resourcegroups-group-name)" : String,
      "[ResourceQuery](#cfn-resourcegroups-group-resourcequery)" : ResourceQuery,
      "[Tags](#cfn-resourcegroups-group-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-resourcegroups-group-syntax.yaml"></a>

```
Type: AWS::ResourceGroups::Group
Properties: 
  [Description](#cfn-resourcegroups-group-description): String
  [Name](#cfn-resourcegroups-group-name): String
  [ResourceQuery](#cfn-resourcegroups-group-resourcequery): 
    ResourceQuery
  [Tags](#cfn-resourcegroups-group-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-resourcegroups-group-properties"></a>

`Description`  <a name="cfn-resourcegroups-group-description"></a>
The description of the resource group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-resourcegroups-group-name"></a>
The name of a resource group\. Specify a name that is unique in the Region\. To create multiple resource groups based on the same CloudFormation stack, use unique names for each\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceQuery`  <a name="cfn-resourcegroups-group-resourcequery"></a>
The resource query that determines which AWS resources are members of the associated resource group\.  
*Required*: No  
*Type*: [ResourceQuery](aws-properties-resourcegroups-group-resourcequery.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-resourcegroups-group-tags"></a>
The tags associated with the specified resource group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-resourcegroups-group-return-values"></a>

### Ref<a name="aws-resource-resourcegroups-group-return-values-ref"></a>

The name of a resource group\.

### Fn::GetAtt<a name="aws-resource-resourcegroups-group-return-values-fn--getatt"></a>

#### <a name="aws-resource-resourcegroups-group-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of a resource group\.

## Examples<a name="aws-resource-resourcegroups-group--examples"></a>



### Creating a CloudFormation Stack\-Based Group Using Defaults<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_Using_Defaults"></a>

This example creates a CloudFormation stack\-based group using defaults\. It includes all supported resource types and uses the same `StackIdentifier` as the CloudFormation stack that defines the group\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_Using_Defaults--json"></a>

```
{
    "ResourceGroup": { 
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyResourceGroup" 
        }
    } 
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_Using_Defaults--yaml"></a>

```
ResourceGroup:
  Type: "AWS::ResourceGroups::Group" 
  Properties:
    Name: "MyMinimalResourceGroup"
```

### Creating a CloudFormation Stack\-Based Group That Includes Specific Resources<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_That_Includes_Specific_Resources"></a>

This example creates a CloudFormation stack\-based group that's similar to the group shown in the previous example\. The difference is that it includes only specific resource types: EC2 instances and DynamoDB tables\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_That_Includes_Specific_Resources--json"></a>

```
{
    "CloudFormationStackGroupForSelectedResourceTypes": {
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyCloudFormationResourceGroup-Filters",
            "ResourceQuery": {
                "Query": {
                    "ResourceTypeFilters": [
                        "AWS::EC2::Instance",
                        "AWS::DynamoDB::Table" 
                    ] 
                } 
            }
        }
    }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_That_Includes_Specific_Resources--yaml"></a>

```
CloudFormationStackGroupForSelectedResourceTypes:
  Type: "AWS::ResourceGroups::Group" 
  Properties: 
    Name: "MyCloudFormationResourceGroup-Filters" 
    ResourceQuery: 
      Query: 
        ResourceTypeFilters: 
          - "AWS::EC2::Instance" 
          - "AWS::DynamoDB::Table"
```

### Creating a CloudFormation Stack\-Based Group Based on Another Stack<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_Based_on_Another_Stack"></a>

This example creates a group that's built from another stack\. The `StackIdentifier` value specifies that resources in the `arn:aws:cloudformation:us-east-1:0123456789:stack/stack-name/9b6f8604-4a39-490c-870b-44b0ebdd38b9` stack are included in the group\. The group is tagged with `TagKey=TagValue.`

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_Based_on_Another_Stack--json"></a>

```
{
    "CloudFormationStackGroupForAnotherStack": {
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyCloudFormationResourceGroupForAnotherStack",
            "Description": "A group that is created via CFN",
            "ResourceQuery": { 
                "Type": "CLOUDFORMATION_STACK_1_0",
                "Query": {
                    "ResourceTypeFilters": [
                        "AWS::AllSupported" 
                    ],
                    "StackIdentifier": "arn:aws:cloudformation:us-east-1:0123456789:stack/stack-name/9b6f8604-4a39-490c-870b-44b0ebdd38b9"
                }
            },
            "Tags": [
                {
                    "Key": "TagKey",
                    "Value": "TagValue" 
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_Stack-Based_Group_Based_on_Another_Stack--yaml"></a>

```
CloudFormationStackGroupForAnotherStack:
  Type: "AWS::ResourceGroups::Group" 
  Properties: 
    Name: "MyCloudFormationResourceGroupForAnotherStack" 
    Description: "A group that is created via CFN" 
    ResourceQuery: 
      Type: "CLOUDFORMATION_STACK_1_0" 
      Query: 
        ResourceTypeFilters:
          - "AWS::AllSupported" 
        StackIdentifier: "arn:aws:cloudformation:us-east-1:0123456789:stack/stack-name/9b6f8604-4a39-490c-870b-44b0ebdd38b9"
    Tags: 
      -
        Key: "TagKey" 
        Value: "TagValue"
```

### Creating a Tag\-Based Group<a name="aws-resource-resourcegroups-group--examples--Creating_a_Tag-Based_Group"></a>

This example shows how to create a group based on tags\. All resources that are tagged with the `Usage` key with a value of `Integration Tests` will be members of this group\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_Tag-Based_Group--json"></a>

```
{
    "TagBasedGroup": {
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyTagBasedResourceGroup",
            "Description": "A group that is created via CFN",
            "ResourceQuery": {
                "Type": "TAG_FILTERS_1_0",
                "Query": {
                    "ResourceTypeFilters": [
                        "AWS::AllSupported" 
                    ],
                    "TagFilters": [
                        {
                            "Key": "Usage",
                            "Values": [
                                "Integration Tests" 
                            ]
                        }
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_Tag-Based_Group--yaml"></a>

```
TagBasedGroup:
  Type: "AWS::ResourceGroups::Group"
  Properties:
    Name: "MyTagBasedResourceGroup"
    Description: "A group that is created via CFN"
    ResourceQuery:
      Type:
        "TAG_FILTERS_1_0" 
      Query:
        ResourceTypeFilters: 
          - "AWS::AllSupported" 
        TagFilters:
          - 
            Key: "Usage" 
            Values: 
              - "Integration Tests"
```
# AWS::ResourceGroups::Group<a name="aws-resource-resourcegroups-group"></a>

Creates a resource group with the specified name and description\. You can optionally include either a resource query or a service configuration\. For more information about constructing a resource query, see [Build queries and groups in AWS Resource Groups](https://docs.aws.amazon.com/ARG/latest/userguide/getting_started-query.html) in the * AWS Resource Groups User Guide*\. For more information about service\-linked groups and service configurations, see [Service configurations for Resource Groups](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html)\.

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
      "[Configuration](#cfn-resourcegroups-group-configuration)" : [ ConfigurationItem, ... ],
      "[Description](#cfn-resourcegroups-group-description)" : String,
      "[Name](#cfn-resourcegroups-group-name)" : String,
      "[ResourceQuery](#cfn-resourcegroups-group-resourcequery)" : ResourceQuery,
      "[Resources](#cfn-resourcegroups-group-resources)" : [ String, ... ],
      "[Tags](#cfn-resourcegroups-group-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-resourcegroups-group-syntax.yaml"></a>

```
Type: AWS::ResourceGroups::Group
Properties: 
  [Configuration](#cfn-resourcegroups-group-configuration): 
    - ConfigurationItem
  [Description](#cfn-resourcegroups-group-description): String
  [Name](#cfn-resourcegroups-group-name): String
  [ResourceQuery](#cfn-resourcegroups-group-resourcequery): 
    ResourceQuery
  [Resources](#cfn-resourcegroups-group-resources): 
    - String
  [Tags](#cfn-resourcegroups-group-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-resourcegroups-group-properties"></a>

`Configuration`  <a name="cfn-resourcegroups-group-configuration"></a>
The service configuration currently associated with the resource group and in effect for the members of the resource group\. A `Configuration` consists of one or more `ConfigurationItem` entries\. For information about service configurations for resource groups and how to construct them, see [Service configurations for resource groups](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html) in the *AWS Resource Groups User Guide*\.  
You can include either a `Configuration` or a `ResourceQuery`, but not both\.
*Required*: Conditional  
*Type*: List of [ConfigurationItem](aws-properties-resourcegroups-group-configurationitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-resourcegroups-group-description"></a>
The description of the resource group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-resourcegroups-group-name"></a>
The name of a resource group\. The name must be unique within the AWS Region in which you create the resource\. To create multiple resource groups based on the same CloudFormation stack, you must generate unique names for each\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceQuery`  <a name="cfn-resourcegroups-group-resourcequery"></a>
The resource query structure that is used to dynamically determine which AWS resources are members of the associated resource group\. For more information about queries and how to construct them, see [Build queries and groups in AWS Resource Groups](https://docs.aws.amazon.com/ARG/latest/userguide/gettingstarted-query.html) in the *AWS Resource Groups User Guide*  
+ You can include either a `ResourceQuery` or a `Configuration`, but not both\.
+ You can specify the group's membership either by using a `ResourceQuery` or by using a list of `Resources`, but not both\.
*Required*: Conditional  
*Type*: [ResourceQuery](aws-properties-resourcegroups-group-resourcequery.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resources`  <a name="cfn-resourcegroups-group-resources"></a>
A list of the Amazon Resource Names \(ARNs\) of AWS resources that you want to add to the specified group\.  
+ You can specify the group membership either by using a list of `Resources` or by using a `ResourceQuery`, but not both\.
+ You can include a `Resources` property only if you also specify a `Configuration` property\.
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-resourcegroups-group-tags"></a>
The tag key and value pairs that are attached to the resource group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-resourcegroups-group-return-values"></a>

### Ref<a name="aws-resource-resourcegroups-group-return-values-ref"></a>

The name of the new resource group\.

### Fn::GetAtt<a name="aws-resource-resourcegroups-group-return-values-fn--getatt"></a>

#### <a name="aws-resource-resourcegroups-group-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the new resource group\.

## Examples<a name="aws-resource-resourcegroups-group--examples"></a>

The following examples show both the JSON and YAML templates that you can use to create resource groups with the specified characteristics\.

### Creating a CloudFormation stack\-based resource group using defaults<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_using_defaults"></a>

This example creates a CloudFormation stack\-based resource group using defaults\. It includes all supported resource types and uses the same `StackIdentifier` as the CloudFormation stack that defines the group\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_using_defaults--json"></a>

```
{
    "ResourceGroup": { 
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyResourceGroup",
            "Description": "A basic, empty resource group that is created by CFN",
        }
    } 
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_using_defaults--yaml"></a>

```
ResourceGroup:
  Type: "AWS::ResourceGroups::Group" 
  Properties:
    Name: "MyMinimalResourceGroup"
    Description: "A basic, empty resource group that is created by CFN"
```

### Creating a CloudFormation stack\-based resource group with specific resources<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_with_specific_resources"></a>

This example creates a CloudFormation stack\-based resource group that's similar to the group shown in the previous example\. The difference is that it can include only resources of the specified types: EC2 instances and DynamoDB tables\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_with_specific_resources--json"></a>

```
{
    "CloudFormationStackGroupForSelectedResourceTypes": {
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyCloudFormationResourceGroup-Filters",
            "Description": "A basic resource group that can hold only EC2 instances or DynamoDB tables", 
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

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_with_specific_resources--yaml"></a>

```
CloudFormationStackGroupForSelectedResourceTypes:
  Type: "AWS::ResourceGroups::Group" 
  Properties: 
    Name: "MyCloudFormationResourceGroup-Filters"
    Description: "A basic resource group that can hold only EC2 instances or DynamoDB tables"
    ResourceQuery: 
      Query: 
        ResourceTypeFilters: 
          - "AWS::EC2::Instance" 
          - "AWS::DynamoDB::Table"
```

### Creating a CloudFormation stack\-based resource group based on another stack<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_based_on_another_stack"></a>

This example creates a resource group that's built from another stack\. The `StackIdentifier` value specifies that resources in the stack with the ARN `arn:aws:cloudformation:us-east-1:123456789012:stack/stack-name/9b6f8604-4a39-490c-870b-44b0ebdd38b9` are included in the group\. The group itself \(not its individual member resources\) is tagged with `Env=Prod`\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_based_on_another_stack--json"></a>

```
{
    "CloudFormationStackGroupForAnotherStack": {
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyCloudFormationResourceGroupForAnotherStack",
            "Description": "A resource group that is based on another CFN stack",
            "ResourceQuery": { 
                "Type": "CLOUDFORMATION_STACK_1_0",
                "Query": {
                    "ResourceTypeFilters": [
                        "AWS::AllSupported" 
                    ],
                    "StackIdentifier": "arn:aws:cloudformation:us-east-1:123456789012:stack/stack-name/9b6f8604-4a39-490c-870b-44b0ebdd38b9"
                }
            },
            "Tags": [
                {
                    "Key": "Env",
                    "Value": "Prod" 
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_CloudFormation_stack-based_resource_group_based_on_another_stack--yaml"></a>

```
CloudFormationStackGroupForAnotherStack:
  Type: "AWS::ResourceGroups::Group" 
  Properties: 
    Name: "MyCloudFormationResourceGroupForAnotherStack" 
    Description: "A group that is based on CFN another stack" 
    ResourceQuery: 
      Type: "CLOUDFORMATION_STACK_1_0" 
      Query: 
        ResourceTypeFilters:
          - "AWS::AllSupported" 
        StackIdentifier: "arn:aws:cloudformation:us-east-1:123456789012:stack/stack-name/9b6f8604-4a39-490c-870b-44b0ebdd38b9"
    Tags: 
      -
        Key: "Env" 
        Value: "Prod"
```

### Creating a tag\-based resource group<a name="aws-resource-resourcegroups-group--examples--Creating_a_tag-based_resource_group"></a>

This example shows how to create a resource group whose membership is based on a tag query\. Any resources that have tags that match the query, in this case the key `Usage` and the value `Integration Tests`, are members of this group\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_tag-based_resource_group--json"></a>

```
{
    "TagBasedGroup": {
        "Type": "AWS::ResourceGroups::Group",
        "Properties": {
            "Name": "MyTagBasedResourceGroup",
            "Description": "A group that is based on a tag query",
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

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_tag-based_resource_group--yaml"></a>

```
TagBasedGroup:
  Type: "AWS::ResourceGroups::Group"
  Properties:
    Name: "MyTagBasedResourceGroup"
    Description: "A group that is based on a tag query"
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

### Creating a resource group for EC2 capacity reservations<a name="aws-resource-resourcegroups-group--examples--Creating_a_resource_group_for_EC2_capacity_reservations"></a>

This example creates a capacity reservations resource group by specifying a configuration and limiting the allowed resource types\. This group initially has no members\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_resource_group_for_EC2_capacity_reservations--json"></a>

```
{
   "CapacityReservationsGroupWithoutResources": {
      "Type": "AWS::ResourceGroups::Group",
      "Properties": {
         "Name": "MyCapacityReservationsGroup",
         "Description": "A resource group for EC2 capacity reservations",
         "Configuration": [
            {
               "Type": "AWS::EC2::CapacityReservationPool",
               "Parameters": []
            },
            {
               "Type": "AWS::ResourceGroups::Generic",
               "Parameters": [
                  {
                     "Name": "allowed-resource-types",
                     "Values": [
                        "AWS::EC2::CapacityReservation"
                     ]
                  }
               ]
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_resource_group_for_EC2_capacity_reservations--yaml"></a>

```
CapacityReservationsGroupWithoutResources:
  Type: "AWS::ResourceGroups::Group"
  Properties:
    Name: "MyCapacityReservationsGroup"
    Description: "A resource group for EC2 capacity reservations"
    Configuration:
    - Type: "AWS::EC2::CapacityReservationPool"
      Parameters: []
    - Type: "AWS::ResourceGroups::Generic"
      Parameters:
      - Name: "allowed-resource-types"
        Values:
          - "AWS::EC2::CapacityReservation"
```

### Creating a resource group for EC2 capacity reservations with initial members<a name="aws-resource-resourcegroups-group--examples--Creating_a_resource_group_for_EC2_capacity_reservations_with_initial_members"></a>

This example creates a capacity reservations resource group identical to the previous example, except this one includes two initial capacity reservations as specified in the `Resources` property\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_a_resource_group_for_EC2_capacity_reservations_with_initial_members--json"></a>

```
{
   "CapacityReservationsGroupWithResources": {
      "Type": "AWS::ResourceGroups::Group",
      "Properties": {
         "Name": "MyCapacityReservationsGroup",
         "Description": "A resource group for EC2 capacity reservations",
         "Configuration": [
            {
               "Type": "AWS::EC2::CapacityReservationPool",
               "Parameters": []
            },
            {
               "Type": "AWS::ResourceGroups::Generic",
               "Parameters": [
                  {
                     "Name": "allowed-resource-types",
                     "Values": [
                        "AWS::EC2::CapacityReservation"
                     ]
                  }
               ]
            }
         ],
         "Resources": [
            "arn:aws:ec2:us-east-1:123456789012:capacity-reservation/cr-0d4953834cd1a96a3",
            "arn:aws:ec2:us-east-1:123456789012:capacity-reservation/cr-0069a2275c16b7333"
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_a_resource_group_for_EC2_capacity_reservations_with_initial_members--yaml"></a>

```
CapacityReservationsGroupWithResources:
  Type: "AWS::ResourceGroups::Group"
  Properties:
    Name: "MyCapacityReservationsGroup"
    Description: "A resource group for EC2 capacity reservations"
    Configuration:
    - Type: "AWS::EC2::CapacityReservationPool"
      Parameters: []
    - Type: "AWS::ResourceGroups::Generic"
      Parameters:
      - Name: "allowed-resource-types"
        Values:
          - "AWS::EC2::CapacityReservation"
    Resources:
      - "arn:aws:ec2:us-east-1:123456789012:capacity-reservation/cr-0d4953834cd1a96a3"
      - "arn:aws:ec2:us-east-1:123456789012:capacity-reservation/cr-0069a2275c16b7333"
```

### Creating an EC2 hosts resource group<a name="aws-resource-resourcegroups-group--examples--Creating_an_EC2_hosts_resource_group"></a>

This example creates a host resource group\. Instances in the group are automatically configured to accept any host based license configuration, to allow only the `c5` host family, to not auto\-release hosts, and to be delete protected\. The group initially has no members\.

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_an_EC2_hosts_resource_group--json"></a>

```
{
  "HostResourceGroup": {
    "Type": "AWS::ResourceGroups::Group",
    "Properties": {
      "Name": "MyHostResourceGroup",
      "Description": "A resource group for EC2 dedicated hosts",
      "Configuration": [
        {
          "Type": "AWS::EC2::HostManagement",
          "Parameters": [
            {
              "Name": "any-host-based-license-configuration",
              "Values": [
                "true"
              ]
            },
            {
              "Name": "allowed-host-families",
              "Values": [
                "c5"
              ]
            },
            {
              "Name": "auto-release-host",
              "Values": [
                "false"
              ]
            }
          ]
        },
        {
          "Type": "AWS::ResourceGroups::Generic",
          "Parameters": [
            {
              "Name": "allowed-resource-types",
              "Values": [
                "AWS::EC2::Host"
              ]
            },
            {
              "Name": "deletion-protection",
              "Values": [
                "UNLESS_EMPTY"
              ]
            }
          ]
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_an_EC2_hosts_resource_group--yaml"></a>

```
HostResourceGroup:
  Type: "AWS::ResourceGroups::Group"
  Properties:
    Name: "MyHostResourceGroup"
    Description: "A resource group for EC2 dedicated hosts"
    Configuration:
      - Type: "AWS::EC2::HostManagement"
        Parameters:
          - Name: "any-host-based-license-configuration"
            Values:
              - "true"
          - Name: "allowed-host-families"
            Values:
              - "c5"
          - Name: "auto-release-host"
            Values:
              - "false"
      - Type: "AWS::ResourceGroups::Generic"
        Parameters:
          - Name: "allowed-resource-types"
            Values:
              - "AWS::EC2::Host"
          - Name: "deletion-protection"
            Values:
              - "UNLESS_EMPTY"
```

### Creating an EC2 hosts resource group with some initial members<a name="aws-resource-resourcegroups-group--examples--Creating_an_EC2_hosts_resource_group_with_some_initial_members"></a>

This example creates an EC2 host resource group that is configured to work with a specific license configuration\. The group initially contains the two hosts specified by the `Resources` property

#### JSON<a name="aws-resource-resourcegroups-group--examples--Creating_an_EC2_hosts_resource_group_with_some_initial_members--json"></a>

```
{
  "HostResourceGroupWithResources": {
    "Type": "AWS::ResourceGroups::Group",
    "Properties": {
      "Name": "MyHostResourceGroup",
      "Description": "A resource group for EC2 dedicated hosts",
      "Configuration": [
        {
          "Type": "AWS::EC2::HostManagement",
          "Parameters": [
            {
              "Name": "allowed-resource-types",
              "Values": [
                "AWS::EC2::Host"
              ]
            },
            {
              "Name": "deletion-protection",
              "Values": [
                "UNLESS_EMPTY"
              ]
            }
          ]
        }
      ],
      "Resources": [
        "arn:aws:ec2:us-east-1:123456789012:dedicated-host/h-0375ef7462b26b11f",
        "arn:aws:ec2:us-east-1:123456789012:dedicated-host/h-0501ab6812c719123"
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-resourcegroups-group--examples--Creating_an_EC2_hosts_resource_group_with_some_initial_members--yaml"></a>

```
HostResourceGroupWithResources:
  Type: "AWS::ResourceGroups::Group"
  Properties:
    Name: "MyHostResourceGroup"
    Description: "A resource group for EC2 dedicated hosts"
    Configuration:
      - Type: "AWS::EC2::HostManagement"
        Parameters:
          - Name: "allowed-host-based-license-configurations"
            Values:
              - "arn:aws:license-manager:us-east-1:123456789012:license-configuration:lic-42bc5628e8edcee52ed797d5bebf0879"
        Parameters:
          - Name: "allowed-resource-types"
            Values:
              - "AWS::EC2::Host"
          - Name: "deletion-protection"
            Values:
              - "UNLESS_EMPTY"
    Resources:
      - "arn:aws:ec2:us-east-1:123456789012:dedicated-host/h-0375ef7462b26b11f"
      - "arn:aws:ec2:us-east-1:123456789012:dedicated-host/h-0501ab6812c719123"
```
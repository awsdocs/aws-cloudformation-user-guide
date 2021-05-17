# AWS::ResourceGroups::Group ConfigurationItem<a name="aws-properties-resourcegroups-group-configurationitem"></a>

One of the items in the service configuration assigned to a resource group\. A service configuration can consist of one or more items\. For details service configurations and how to construct them, see [Service configurations for resource groups](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html) in the *AWS Resource Groups User Guide*\.

## Syntax<a name="aws-properties-resourcegroups-group-configurationitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resourcegroups-group-configurationitem-syntax.json"></a>

```
{
  "[Parameters](#cfn-resourcegroups-group-configurationitem-parameters)" : [ ConfigurationParameter, ... ],
  "[Type](#cfn-resourcegroups-group-configurationitem-type)" : String
}
```

### YAML<a name="aws-properties-resourcegroups-group-configurationitem-syntax.yaml"></a>

```
  [Parameters](#cfn-resourcegroups-group-configurationitem-parameters): 
    - ConfigurationParameter
  [Type](#cfn-resourcegroups-group-configurationitem-type): String
```

## Properties<a name="aws-properties-resourcegroups-group-configurationitem-properties"></a>

`Parameters`  <a name="cfn-resourcegroups-group-configurationitem-parameters"></a>
A collection of parameters for this configuration item\. For the list of parameters that you can use with each configuration item `Type`, see [Supported resource types and parameters](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html#about-slg-types) in the *AWS Resource Groups User Guide*\.  
*Required*: No  
*Type*: List of [ConfigurationParameter](aws-properties-resourcegroups-group-configurationparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-resourcegroups-group-configurationitem-type"></a>
Specifies the type of configuration item\. Each item must have a unique value for type\. For the list of the types that you can specify for a configuration item, see [Supported resource types and parameters](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html#about-slg-types) in the *AWS Resource Groups User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
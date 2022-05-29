# AWS::ResourceGroups::Group ConfigurationParameter<a name="aws-properties-resourcegroups-group-configurationparameter"></a>

One parameter for a group configuration item\. For details about service configurations and how to construct them, see [Service configurations for resource groups](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html) in the *AWS Resource Groups User Guide*\.

## Syntax<a name="aws-properties-resourcegroups-group-configurationparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-resourcegroups-group-configurationparameter-syntax.json"></a>

```
{
  "[Name](#cfn-resourcegroups-group-configurationparameter-name)" : String,
  "[Values](#cfn-resourcegroups-group-configurationparameter-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-resourcegroups-group-configurationparameter-syntax.yaml"></a>

```
  [Name](#cfn-resourcegroups-group-configurationparameter-name): String
  [Values](#cfn-resourcegroups-group-configurationparameter-values): 
    - String
```

## Properties<a name="aws-properties-resourcegroups-group-configurationparameter-properties"></a>

`Name`  <a name="cfn-resourcegroups-group-configurationparameter-name"></a>
The name of the group configuration parameter\. For the list of parameters that you can use with each configuration item type, see [Supported resource types and parameters](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html#about-slg-types) in the *AWS Resource Groups User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-resourcegroups-group-configurationparameter-values"></a>
The value or values to be used for the specified parameter\. For the list of values you can use with each parameter, see [Supported resource types and parameters](https://docs.aws.amazon.com/ARG/latest/APIReference/about-slg.html#about-slg-types)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
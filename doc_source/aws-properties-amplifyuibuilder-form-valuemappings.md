# AWS::AmplifyUIBuilder::Form ValueMappings<a name="aws-properties-amplifyuibuilder-form-valuemappings"></a>

Represents the data binding configuration for a value map\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-valuemappings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-valuemappings-syntax.json"></a>

```
{
  "[Values](#cfn-amplifyuibuilder-form-valuemappings-values)" : [ ValueMapping, ... ]
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-valuemappings-syntax.yaml"></a>

```
  [Values](#cfn-amplifyuibuilder-form-valuemappings-values): 
    - ValueMapping
```

## Properties<a name="aws-properties-amplifyuibuilder-form-valuemappings-properties"></a>

`Values`  <a name="cfn-amplifyuibuilder-form-valuemappings-values"></a>
The value and display value pairs\.  
*Required*: Yes  
*Type*: List of [ValueMapping](aws-properties-amplifyuibuilder-form-valuemapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
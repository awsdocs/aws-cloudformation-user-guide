# AWS::AmplifyUIBuilder::Component ComponentBindingPropertiesValue<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalue"></a>

The `ComponentBindingPropertiesValue` property specifies the data binding configuration for a component at runtime\. You can use `ComponentBindingPropertiesValue` to add exposed properties to a component to allow different values to be entered when a component is reused in different places in an app\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalue-syntax.json"></a>

```
{
  "[BindingProperties](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-bindingproperties)" : ComponentBindingPropertiesValueProperties,
  "[DefaultValue](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-defaultvalue)" : String,
  "[Type](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-type)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalue-syntax.yaml"></a>

```
  [BindingProperties](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-bindingproperties): 
    ComponentBindingPropertiesValueProperties
  [DefaultValue](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-defaultvalue): String
  [Type](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-type): String
```

## Properties<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalue-properties"></a>

`BindingProperties`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-bindingproperties"></a>
Describes the properties to customize with data at runtime\.  
*Required*: No  
*Type*: [ComponentBindingPropertiesValueProperties](aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalueproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultValue`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-defaultvalue"></a>
The default value of the property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalue-type"></a>
The property type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
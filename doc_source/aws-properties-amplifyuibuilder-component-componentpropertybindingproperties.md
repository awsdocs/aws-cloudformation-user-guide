# AWS::AmplifyUIBuilder::Component ComponentPropertyBindingProperties<a name="aws-properties-amplifyuibuilder-component-componentpropertybindingproperties"></a>

The `ComponentPropertyBindingProperties` property specifies a component property to associate with a binding property\. This enables exposed properties on the top level component to propagate data to the component's property values\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-componentpropertybindingproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-componentpropertybindingproperties-syntax.json"></a>

```
{
  "[Field](#cfn-amplifyuibuilder-component-componentpropertybindingproperties-field)" : String,
  "[Property](#cfn-amplifyuibuilder-component-componentpropertybindingproperties-property)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-componentpropertybindingproperties-syntax.yaml"></a>

```
  [Field](#cfn-amplifyuibuilder-component-componentpropertybindingproperties-field): String
  [Property](#cfn-amplifyuibuilder-component-componentpropertybindingproperties-property): String
```

## Properties<a name="aws-properties-amplifyuibuilder-component-componentpropertybindingproperties-properties"></a>

`Field`  <a name="cfn-amplifyuibuilder-component-componentpropertybindingproperties-field"></a>
The data field to bind the property to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Property`  <a name="cfn-amplifyuibuilder-component-componentpropertybindingproperties-property"></a>
The component property to bind to the data field\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
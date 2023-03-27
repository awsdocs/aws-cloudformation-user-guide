# AWS::AmplifyUIBuilder::Component ActionParameters<a name="aws-properties-amplifyuibuilder-component-actionparameters"></a>

The `ActionParameters` property specifies the event action configuration for an element of a `Component` or `ComponentChild`\. Use for the workflow feature in Amplify Studio that allows you to bind events and actions to components\. `ActionParameters` defines the action that is performed when an event occurs on the component\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-actionparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-actionparameters-syntax.json"></a>

```
{
  "[Anchor](#cfn-amplifyuibuilder-component-actionparameters-anchor)" : ComponentProperty,
  "[Fields](#cfn-amplifyuibuilder-component-actionparameters-fields)" : {Key : Value, ...},
  "[Global](#cfn-amplifyuibuilder-component-actionparameters-global)" : ComponentProperty,
  "[Id](#cfn-amplifyuibuilder-component-actionparameters-id)" : ComponentProperty,
  "[Model](#cfn-amplifyuibuilder-component-actionparameters-model)" : String,
  "[State](#cfn-amplifyuibuilder-component-actionparameters-state)" : MutationActionSetStateParameter,
  "[Target](#cfn-amplifyuibuilder-component-actionparameters-target)" : ComponentProperty,
  "[Type](#cfn-amplifyuibuilder-component-actionparameters-type)" : ComponentProperty,
  "[Url](#cfn-amplifyuibuilder-component-actionparameters-url)" : ComponentProperty
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-actionparameters-syntax.yaml"></a>

```
  [Anchor](#cfn-amplifyuibuilder-component-actionparameters-anchor): 
    ComponentProperty
  [Fields](#cfn-amplifyuibuilder-component-actionparameters-fields): 
    Key : Value
  [Global](#cfn-amplifyuibuilder-component-actionparameters-global): 
    ComponentProperty
  [Id](#cfn-amplifyuibuilder-component-actionparameters-id): 
    ComponentProperty
  [Model](#cfn-amplifyuibuilder-component-actionparameters-model): String
  [State](#cfn-amplifyuibuilder-component-actionparameters-state): 
    MutationActionSetStateParameter
  [Target](#cfn-amplifyuibuilder-component-actionparameters-target): 
    ComponentProperty
  [Type](#cfn-amplifyuibuilder-component-actionparameters-type): 
    ComponentProperty
  [Url](#cfn-amplifyuibuilder-component-actionparameters-url): 
    ComponentProperty
```

## Properties<a name="aws-properties-amplifyuibuilder-component-actionparameters-properties"></a>

`Anchor`  <a name="cfn-amplifyuibuilder-component-actionparameters-anchor"></a>
The HTML anchor link to the location to open\. Specify this value for a navigation action\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Fields`  <a name="cfn-amplifyuibuilder-component-actionparameters-fields"></a>
A dictionary of key\-value pairs mapping Amplify Studio properties to fields in a data model\. Use when the action performs an operation on an Amplify DataStore model\.  
*Required*: No  
*Type*: Map of [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Global`  <a name="cfn-amplifyuibuilder-component-actionparameters-global"></a>
Specifies whether the user should be signed out globally\. Specify this value for an auth sign out action\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-amplifyuibuilder-component-actionparameters-id"></a>
The unique ID of the component that the `ActionParameters` apply to\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Model`  <a name="cfn-amplifyuibuilder-component-actionparameters-model"></a>
The name of the data model\. Use when the action performs an operation on an Amplify DataStore model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-amplifyuibuilder-component-actionparameters-state"></a>
A key\-value pair that specifies the state property name and its initial value\.  
*Required*: No  
*Type*: [MutationActionSetStateParameter](aws-properties-amplifyuibuilder-component-mutationactionsetstateparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-amplifyuibuilder-component-actionparameters-target"></a>
The element within the same component to modify when the action occurs\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-amplifyuibuilder-component-actionparameters-type"></a>
The type of navigation action\. Valid values are `url` and `anchor`\. This value is required for a navigation action\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-amplifyuibuilder-component-actionparameters-url"></a>
The URL to the location to open\. Specify this value for a navigation action\.  
*Required*: No  
*Type*: [ComponentProperty](aws-properties-amplifyuibuilder-component-componentproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
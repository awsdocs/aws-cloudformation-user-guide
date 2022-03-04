# AWS::AmplifyUIBuilder::Component ComponentEvent<a name="aws-properties-amplifyuibuilder-component-componentevent"></a>

The `ComponentEvent` property specifies the configuration of an event\. You can bind an event and a corresponding action to a `Component` or a `ComponentChild`\. A button click is an example of an event\. 

## Syntax<a name="aws-properties-amplifyuibuilder-component-componentevent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-componentevent-syntax.json"></a>

```
{
  "[Action](#cfn-amplifyuibuilder-component-componentevent-action)" : String,
  "[Parameters](#cfn-amplifyuibuilder-component-componentevent-parameters)" : ActionParameters
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-componentevent-syntax.yaml"></a>

```
  [Action](#cfn-amplifyuibuilder-component-componentevent-action): String
  [Parameters](#cfn-amplifyuibuilder-component-componentevent-parameters): 
    ActionParameters
```

## Properties<a name="aws-properties-amplifyuibuilder-component-componentevent-properties"></a>

`Action`  <a name="cfn-amplifyuibuilder-component-componentevent-action"></a>
The action to perform when a specific event is raised\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-amplifyuibuilder-component-componentevent-parameters"></a>
Describes information about the action\.  
*Required*: No  
*Type*: [ActionParameters](aws-properties-amplifyuibuilder-component-actionparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
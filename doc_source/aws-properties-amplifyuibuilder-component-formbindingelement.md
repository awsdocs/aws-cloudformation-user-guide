# AWS::AmplifyUIBuilder::Component FormBindingElement<a name="aws-properties-amplifyuibuilder-component-formbindingelement"></a>

Describes how to bind a component property to form data\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-formbindingelement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-formbindingelement-syntax.json"></a>

```
{
  "[Element](#cfn-amplifyuibuilder-component-formbindingelement-element)" : String,
  "[Property](#cfn-amplifyuibuilder-component-formbindingelement-property)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-formbindingelement-syntax.yaml"></a>

```
  [Element](#cfn-amplifyuibuilder-component-formbindingelement-element): String
  [Property](#cfn-amplifyuibuilder-component-formbindingelement-property): String
```

## Properties<a name="aws-properties-amplifyuibuilder-component-formbindingelement-properties"></a>

`Element`  <a name="cfn-amplifyuibuilder-component-formbindingelement-element"></a>
The name of the component to retrieve a value from\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Property`  <a name="cfn-amplifyuibuilder-component-formbindingelement-property"></a>
The property to retrieve a value from\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
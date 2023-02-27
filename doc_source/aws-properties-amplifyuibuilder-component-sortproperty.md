# AWS::AmplifyUIBuilder::Component SortProperty<a name="aws-properties-amplifyuibuilder-component-sortproperty"></a>

The `SortProperty` property specifies how to sort the data that you bind to a component\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-sortproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-sortproperty-syntax.json"></a>

```
{
  "[Direction](#cfn-amplifyuibuilder-component-sortproperty-direction)" : String,
  "[Field](#cfn-amplifyuibuilder-component-sortproperty-field)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-sortproperty-syntax.yaml"></a>

```
  [Direction](#cfn-amplifyuibuilder-component-sortproperty-direction): String
  [Field](#cfn-amplifyuibuilder-component-sortproperty-field): String
```

## Properties<a name="aws-properties-amplifyuibuilder-component-sortproperty-properties"></a>

`Direction`  <a name="cfn-amplifyuibuilder-component-sortproperty-direction"></a>
The direction of the sort, either ascending or descending\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Field`  <a name="cfn-amplifyuibuilder-component-sortproperty-field"></a>
The field to perform the sort on\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
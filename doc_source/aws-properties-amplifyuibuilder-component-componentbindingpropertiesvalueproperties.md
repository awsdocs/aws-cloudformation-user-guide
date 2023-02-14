# AWS::AmplifyUIBuilder::Component ComponentBindingPropertiesValueProperties<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalueproperties"></a>

The `ComponentBindingPropertiesValueProperties` property specifies the data binding configuration for a specific property using data stored in AWS\. For AWS connected properties, you can bind a property to data stored in an Amazon S3 bucket, an Amplify DataStore model or an authenticated user attribute\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-syntax.json"></a>

```
{
  "[Bucket](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-bucket)" : String,
  "[DefaultValue](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-defaultvalue)" : String,
  "[Field](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-field)" : String,
  "[Key](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-key)" : String,
  "[Model](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-model)" : String,
  "[Predicates](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-predicates)" : [ Predicate, ... ],
  "[UserAttribute](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-userattribute)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-syntax.yaml"></a>

```
  [Bucket](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-bucket): String
  [DefaultValue](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-defaultvalue): String
  [Field](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-field): String
  [Key](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-key): String
  [Model](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-model): String
  [Predicates](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-predicates): 
    - Predicate
  [UserAttribute](#cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-userattribute): String
```

## Properties<a name="aws-properties-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-properties"></a>

`Bucket`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-bucket"></a>
An Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultValue`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-defaultvalue"></a>
The default value to assign to the property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Field`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-field"></a>
The field to bind the data to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-key"></a>
The storage key for an Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Model`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-model"></a>
An Amplify DataStore model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Predicates`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-predicates"></a>
A list of predicates for binding a component's properties to data\.  
*Required*: No  
*Type*: List of [Predicate](aws-properties-amplifyuibuilder-component-predicate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserAttribute`  <a name="cfn-amplifyuibuilder-component-componentbindingpropertiesvalueproperties-userattribute"></a>
An authenticated user attribute\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
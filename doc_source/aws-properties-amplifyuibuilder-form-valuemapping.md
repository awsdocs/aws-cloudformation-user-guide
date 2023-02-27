# AWS::AmplifyUIBuilder::Form ValueMapping<a name="aws-properties-amplifyuibuilder-form-valuemapping"></a>

Associates a complex object with a display value\. Use `ValueMapping` to store how to represent complex objects when they are displayed\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-valuemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-valuemapping-syntax.json"></a>

```
{
  "[DisplayValue](#cfn-amplifyuibuilder-form-valuemapping-displayvalue)" : FormInputValueProperty,
  "[Value](#cfn-amplifyuibuilder-form-valuemapping-value)" : FormInputValueProperty
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-valuemapping-syntax.yaml"></a>

```
  [DisplayValue](#cfn-amplifyuibuilder-form-valuemapping-displayvalue): 
    FormInputValueProperty
  [Value](#cfn-amplifyuibuilder-form-valuemapping-value): 
    FormInputValueProperty
```

## Properties<a name="aws-properties-amplifyuibuilder-form-valuemapping-properties"></a>

`DisplayValue`  <a name="cfn-amplifyuibuilder-form-valuemapping-displayvalue"></a>
The value to display for the complex object\.  
*Required*: No  
*Type*: [FormInputValueProperty](aws-properties-amplifyuibuilder-form-forminputvalueproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-amplifyuibuilder-form-valuemapping-value"></a>
The complex object\.  
*Required*: Yes  
*Type*: [FormInputValueProperty](aws-properties-amplifyuibuilder-form-forminputvalueproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::AmplifyUIBuilder::Component ComponentVariant<a name="aws-properties-amplifyuibuilder-component-componentvariant"></a>

The `ComponentVariant` property specifies the style configuration of a unique variation of a main component\.

## Syntax<a name="aws-properties-amplifyuibuilder-component-componentvariant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-component-componentvariant-syntax.json"></a>

```
{
  "[Overrides](#cfn-amplifyuibuilder-component-componentvariant-overrides)" : Json,
  "[VariantValues](#cfn-amplifyuibuilder-component-componentvariant-variantvalues)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-amplifyuibuilder-component-componentvariant-syntax.yaml"></a>

```
  [Overrides](#cfn-amplifyuibuilder-component-componentvariant-overrides): Json
  [VariantValues](#cfn-amplifyuibuilder-component-componentvariant-variantvalues): 
    Key : Value
```

## Properties<a name="aws-properties-amplifyuibuilder-component-componentvariant-properties"></a>

`Overrides`  <a name="cfn-amplifyuibuilder-component-componentvariant-overrides"></a>
The properties of the component variant that can be overriden when customizing an instance of the component\. You can't specify `tags` as a valid property for `overrides`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VariantValues`  <a name="cfn-amplifyuibuilder-component-componentvariant-variantvalues"></a>
The combination of variants that comprise this variant\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
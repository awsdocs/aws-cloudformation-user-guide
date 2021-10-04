# AWS::CustomerProfiles::ObjectType FieldMap<a name="aws-properties-customerprofiles-objecttype-fieldmap"></a>

A map of the name and ObjectType field\.

## Syntax<a name="aws-properties-customerprofiles-objecttype-fieldmap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-objecttype-fieldmap-syntax.json"></a>

```
{
  "[Name](#cfn-customerprofiles-objecttype-fieldmap-name)" : String,
  "[ObjectTypeField](#cfn-customerprofiles-objecttype-fieldmap-objecttypefield)" : ObjectTypeField
}
```

### YAML<a name="aws-properties-customerprofiles-objecttype-fieldmap-syntax.yaml"></a>

```
  [Name](#cfn-customerprofiles-objecttype-fieldmap-name): String
  [ObjectTypeField](#cfn-customerprofiles-objecttype-fieldmap-objecttypefield): 
    ObjectTypeField
```

## Properties<a name="aws-properties-customerprofiles-objecttype-fieldmap-properties"></a>

`Name`  <a name="cfn-customerprofiles-objecttype-fieldmap-name"></a>
Name of the field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectTypeField`  <a name="cfn-customerprofiles-objecttype-fieldmap-objecttypefield"></a>
Represents a field in a ProfileObjectType\.  
*Required*: No  
*Type*: [ObjectTypeField](aws-properties-customerprofiles-objecttype-objecttypefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
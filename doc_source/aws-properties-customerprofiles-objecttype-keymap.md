# AWS::CustomerProfiles::ObjectType KeyMap<a name="aws-properties-customerprofiles-objecttype-keymap"></a>

A unique key map that can be used to map data to the profile\.

## Syntax<a name="aws-properties-customerprofiles-objecttype-keymap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-objecttype-keymap-syntax.json"></a>

```
{
  "[Name](#cfn-customerprofiles-objecttype-keymap-name)" : String,
  "[ObjectTypeKeyList](#cfn-customerprofiles-objecttype-keymap-objecttypekeylist)" : [ ObjectTypeKey, ... ]
}
```

### YAML<a name="aws-properties-customerprofiles-objecttype-keymap-syntax.yaml"></a>

```
  [Name](#cfn-customerprofiles-objecttype-keymap-name): String
  [ObjectTypeKeyList](#cfn-customerprofiles-objecttype-keymap-objecttypekeylist): 
    - ObjectTypeKey
```

## Properties<a name="aws-properties-customerprofiles-objecttype-keymap-properties"></a>

`Name`  <a name="cfn-customerprofiles-objecttype-keymap-name"></a>
Name of the key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectTypeKeyList`  <a name="cfn-customerprofiles-objecttype-keymap-objecttypekeylist"></a>
 A list of ObjectTypeKey\.  
*Required*: No  
*Type*: List of [ObjectTypeKey](aws-properties-customerprofiles-objecttype-objecttypekey.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
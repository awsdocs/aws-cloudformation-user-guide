# AWS::CustomerProfiles::ObjectType ObjectTypeField<a name="aws-properties-customerprofiles-objecttype-objecttypefield"></a>

Represents a field in a ProfileObjectType\.

## Syntax<a name="aws-properties-customerprofiles-objecttype-objecttypefield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-objecttype-objecttypefield-syntax.json"></a>

```
{
  "[ContentType](#cfn-customerprofiles-objecttype-objecttypefield-contenttype)" : String,
  "[Source](#cfn-customerprofiles-objecttype-objecttypefield-source)" : String,
  "[Target](#cfn-customerprofiles-objecttype-objecttypefield-target)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-objecttype-objecttypefield-syntax.yaml"></a>

```
  [ContentType](#cfn-customerprofiles-objecttype-objecttypefield-contenttype): String
  [Source](#cfn-customerprofiles-objecttype-objecttypefield-source): String
  [Target](#cfn-customerprofiles-objecttype-objecttypefield-target): String
```

## Properties<a name="aws-properties-customerprofiles-objecttype-objecttypefield-properties"></a>

`ContentType`  <a name="cfn-customerprofiles-objecttype-objecttypefield-contenttype"></a>
The content type of the field\. Used for determining equality when searching\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-customerprofiles-objecttype-objecttypefield-source"></a>
A field of a ProfileObject\. For example: \_source\.FirstName, where “\_source” is a ProfileObjectType of a Zendesk user and “FirstName” is a field in that ObjectType\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-customerprofiles-objecttype-objecttypefield-target"></a>
The location of the data in the standard ProfileObject model\. For example: \_profile\.Address\.PostalCode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
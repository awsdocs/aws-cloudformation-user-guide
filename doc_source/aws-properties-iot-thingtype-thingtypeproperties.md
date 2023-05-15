# AWS::IoT::ThingType ThingTypeProperties<a name="aws-properties-iot-thingtype-thingtypeproperties"></a>

The ThingTypeProperties contains information about the thing type including: a thing type description, and a list of searchable thing attribute names\.

## Syntax<a name="aws-properties-iot-thingtype-thingtypeproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-thingtype-thingtypeproperties-syntax.json"></a>

```
{
  "[SearchableAttributes](#cfn-iot-thingtype-thingtypeproperties-searchableattributes)" : [ String, ... ],
  "[ThingTypeDescription](#cfn-iot-thingtype-thingtypeproperties-thingtypedescription)" : String
}
```

### YAML<a name="aws-properties-iot-thingtype-thingtypeproperties-syntax.yaml"></a>

```
  [SearchableAttributes](#cfn-iot-thingtype-thingtypeproperties-searchableattributes): 
    - String
  [ThingTypeDescription](#cfn-iot-thingtype-thingtypeproperties-thingtypedescription): String
```

## Properties<a name="aws-properties-iot-thingtype-thingtypeproperties-properties"></a>

`SearchableAttributes`  <a name="cfn-iot-thingtype-thingtypeproperties-searchableattributes"></a>
A list of searchable thing attribute names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ThingTypeDescription`  <a name="cfn-iot-thingtype-thingtypeproperties-thingtypedescription"></a>
The description of the thing type\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
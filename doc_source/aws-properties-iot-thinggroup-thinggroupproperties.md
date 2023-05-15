# AWS::IoT::ThingGroup ThingGroupProperties<a name="aws-properties-iot-thinggroup-thinggroupproperties"></a>

Thing group properties\.

## Syntax<a name="aws-properties-iot-thinggroup-thinggroupproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-thinggroup-thinggroupproperties-syntax.json"></a>

```
{
  "[AttributePayload](#cfn-iot-thinggroup-thinggroupproperties-attributepayload)" : AttributePayload,
  "[ThingGroupDescription](#cfn-iot-thinggroup-thinggroupproperties-thinggroupdescription)" : String
}
```

### YAML<a name="aws-properties-iot-thinggroup-thinggroupproperties-syntax.yaml"></a>

```
  [AttributePayload](#cfn-iot-thinggroup-thinggroupproperties-attributepayload): 
    AttributePayload
  [ThingGroupDescription](#cfn-iot-thinggroup-thinggroupproperties-thinggroupdescription): String
```

## Properties<a name="aws-properties-iot-thinggroup-thinggroupproperties-properties"></a>

`AttributePayload`  <a name="cfn-iot-thinggroup-thinggroupproperties-attributepayload"></a>
The thing group attributes in JSON format\.  
*Required*: No  
*Type*: [AttributePayload](aws-properties-iot-thinggroup-attributepayload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThingGroupDescription`  <a name="cfn-iot-thinggroup-thinggroupproperties-thinggroupdescription"></a>
The thing group description\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
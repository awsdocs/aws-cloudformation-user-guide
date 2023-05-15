# AWS::IoT::ThingGroup AttributePayload<a name="aws-properties-iot-thinggroup-attributepayload"></a>

The attribute payload\.

## Syntax<a name="aws-properties-iot-thinggroup-attributepayload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-thinggroup-attributepayload-syntax.json"></a>

```
{
  "[Attributes](#cfn-iot-thinggroup-attributepayload-attributes)" : {Key: Value, ...}
}
```

### YAML<a name="aws-properties-iot-thinggroup-attributepayload-syntax.yaml"></a>

```
  [Attributes](#cfn-iot-thinggroup-attributepayload-attributes): 
    Key: Value
```

## Properties<a name="aws-properties-iot-thinggroup-attributepayload-properties"></a>

`Attributes`  <a name="cfn-iot-thinggroup-attributepayload-attributes"></a>
A JSON string containing up to three key\-value pair in JSON format\. For example:  
 `{\"attributes\":{\"string1\":\"string2\"}}`   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
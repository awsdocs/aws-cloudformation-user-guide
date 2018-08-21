# AWS IoT Thing AttributePayload<a name="aws-properties-iot-thing-attributepayload"></a>

The `AttributePayload` property specifies up to three attributes for an AWS IoT as key–value pairs\. `AttributePayload` is a property of the [AWS::IoT::Thing](aws-resource-iot-thing.md) resource\.

## Syntax<a name="aws-properties-iot-thing-attributepayload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-thing-attributepayload-syntax.json"></a>

```
{
  "[Attributes](#cfn-iot-thing-attributepayload-attributes)" : { String:String, ... }
}
```

### YAML<a name="aws-properties-iot-thing-attributepayload-syntax.yaml"></a>

```
[Attributes](#cfn-iot-thing-attributepayload-attributes):
  String: String
```

## Properties<a name="aws-properties-iot-thing-attributepayload-properties"></a>

`Attributes`  <a name="cfn-iot-thing-attributepayload-attributes"></a>
A string that contains up to three key–value pairs\. Maximum length of 800\. Duplicates not allowed\.  
*Required*: No  
*Type*: String to string map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Example<a name="aws-properties-iot-thing-attributepayload-example"></a>

The following example declares an attribute payload with three attributes\.

### JSON<a name="aws-properties-iot-thing-attributepayload-example.json"></a>

```
"AttributePayload": {
    "Attributes": {
        "myAttributeA": {
            "Ref": "MyAttributeValueA"
        },
        "myAttributeB": {
            "Ref": "MyAttributeValueB"
        },
        "myAttributeC": {
            "Ref": "MyAttributeValueC"
        }
    }
}
```

### YAML<a name="aws-properties-iot-thing-attributepayload-example.yaml"></a>

```
AttributePayload: 
  Attributes: 
    myAttributeA: 
      Ref: "MyAttributeValueA"
    myAttributeB: 
      Ref: "MyAttributeValueB"
    myAttributeC: 
      Ref: "MyAttributeValueC"
```
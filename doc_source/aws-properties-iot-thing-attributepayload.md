# AWS::IoT::Thing AttributePayload<a name="aws-properties-iot-thing-attributepayload"></a>

The AttributePayload property specifies up to three attributes for an AWS IoT as key value pairs\. AttributePayload is a property of the [AWS::IoT::Thing](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-thing.html) resource\.

## Syntax<a name="aws-properties-iot-thing-attributepayload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-thing-attributepayload-syntax.json"></a>

```
{
  "[Attributes](#cfn-iot-thing-attributepayload-attributes)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-iot-thing-attributepayload-syntax.yaml"></a>

```
  [Attributes](#cfn-iot-thing-attributepayload-attributes): 
    Key : Value
```

## Properties<a name="aws-properties-iot-thing-attributepayload-properties"></a>

`Attributes`  <a name="cfn-iot-thing-attributepayload-attributes"></a>
A JSON string containing up to three key\-value pair in JSON format\. For example:  
 `{\"attributes\":{\"string1\":\"string2\"}}`   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-iot-thing-attributepayload--examples"></a>

### <a name="aws-properties-iot-thing-attributepayload--examples--"></a>

The following example declares an attribute payload with three attributes\.

#### JSON<a name="aws-properties-iot-thing-attributepayload--examples----json"></a>

```
            {
   "AttributePayload":{
      "Attributes":{
         "myAttributeA":{
            "Ref":"MyAttributeValueA"
         },
         "myAttributeB":{
            "Ref":"MyAttributeValueB"
         },
         "myAttributeC":{
            "Ref":"MyAttributeValueC"
         }
      }
   }
}
```

#### YAML<a name="aws-properties-iot-thing-attributepayload--examples----yaml"></a>

```
AttributePayload:
  Attributes:
    myAttributeA:
      Ref: MyAttributeValueA
    myAttributeB:
      Ref: MyAttributeValueB
    myAttributeC:
      Ref: MyAttributeValueC
```
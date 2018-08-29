# AWS::IoT::Thing<a name="aws-resource-iot-thing"></a>

Use the `AWS::IoT::Thing` resource to declare an AWS IoT thing\.

For information about working with things, see [How AWS IoT Works](http://docs.aws.amazon.com/iot/latest/developerguide/aws-iot-how-it-works.html) and [Device Registry for AWS IoT](http://docs.aws.amazon.com/iot/latest/developerguide/thing-registry.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="w3ab2c21c10d805b7"></a>

### JSON<a name="aws-resource-iot-thing-syntax.json"></a>

```
{
   "Type": "AWS::IoT::Thing",
   "Properties": {
      "[AttributePayload](#cfn-iot-thing-attributepayload)": [*AttributePayload*](aws-properties-iot-thing-attributepayload.md)
      "[ThingName](#cfn-iot-thing-thingname)": String
    }
}
```

### YAML<a name="aws-resource-iot-thing-syntax.yaml"></a>

```
Type: "AWS::IoT::Thing"
Properties:
  [AttributePayload](#cfn-iot-thing-attributepayload):
    [*AttributePayload*](aws-properties-iot-thing-attributepayload.md)
  [ThingName](#cfn-iot-thing-thingname): String
```

## Properties<a name="w3ab2c21c10d805b9"></a>

`AttributePayload`  <a name="cfn-iot-thing-attributepayload"></a>
The attribute payload\.  
*Required*: No  
*Type*: [AWS IoT Thing AttributePayload](aws-properties-iot-thing-attributepayload.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ThingName`  <a name="cfn-iot-thing-thingname"></a>
The name \(the physical ID\) of the AWS IoT thing\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d805c11"></a>

### Ref<a name="w3ab2c21c10d805c11b2"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the thing name\. For example:

```
{ "Ref": "MyThing" }
```

For a stack named `MyStack`, a value similar to the following is returned:

```
MyStack-MyThing-AB1CDEFGHIJK
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d805c13"></a>

The following example declares a thing and the values of its attributes\.

### JSON<a name="aws-resource-iot-thing-example.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyThing": {
         "Type": "AWS::IoT::Thing",
         "Properties": {
            "ThingName": {
               "Ref": "NameParameter"
            },
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
         }
      }
   },
   "Parameters": {
      "NameParameter": {
         "Type": "String"
      },
      "MyAttributeValueA": {
         "Type": "String",
         "Default": "myStringA123"
      },
      "MyAttributeValueB": {
         "Type": "String",
         "Default": "myStringB123"
      },
      "MyAttributeValueC": {
         "Type": "String",
         "Default": "myStringC123"
      }
   }
}
```

### YAML<a name="aws-resource-iot-thing-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MyThing: 
    Type: "AWS::IoT::Thing"
    Properties: 
      ThingName: 
        Ref: "NameParameter"
      AttributePayload: 
        Attributes: 
          myAttributeA: 
            Ref: "MyAttributeValueA"
          myAttributeB: 
            Ref: "MyAttributeValueB"
          myAttributeC: 
            Ref: "MyAttributeValueC"
Parameters: 
  NameParameter: 
    Type: "String"
  MyAttributeValueA: 
    Type: "String"
    Default: "myStringA123"
  MyAttributeValueB: 
    Type: "String"
    Default: "myStringB123"
  MyAttributeValueC: 
    Type: "String"
    Default: "myStringC123"
```
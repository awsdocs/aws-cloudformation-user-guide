# AWS::IoT::Thing<a name="aws-resource-iot-thing"></a>

Use the `AWS::IoT::Thing` resource to declare an AWS IoT thing\.

For information about working with things, see [How AWS IoT Works](https://docs.aws.amazon.com/iot/latest/developerguide/aws-iot-how-it-works.html) and [Device Registry for AWS IoT](https://docs.aws.amazon.com/iot/latest/developerguide/thing-registry.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="aws-resource-iot-thing-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-thing-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::Thing",
  "Properties" : {
      "[AttributePayload](#cfn-iot-thing-attributepayload)" : AttributePayload,
      "[ThingName](#cfn-iot-thing-thingname)" : String
    }
}
```

### YAML<a name="aws-resource-iot-thing-syntax.yaml"></a>

```
Type: AWS::IoT::Thing
Properties: 
  [AttributePayload](#cfn-iot-thing-attributepayload): 
    AttributePayload
  [ThingName](#cfn-iot-thing-thingname): String
```

## Properties<a name="aws-resource-iot-thing-properties"></a>

`AttributePayload`  <a name="cfn-iot-thing-attributepayload"></a>
A string that contains up to three key value pairs\. Maximum length of 800\. Duplicates not allowed\.  
*Required*: No  
*Type*: [AttributePayload](aws-properties-iot-thing-attributepayload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThingName`  <a name="cfn-iot-thing-thingname"></a>
The name of the thing to update\.  
You can't change a thing's name\. To change a thing's name, you must create a new thing, give it the new name, and then delete the old thing\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-thing-return-values"></a>

### Ref<a name="aws-resource-iot-thing-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the thing name\. For example:

 `{ "Ref": "MyThing" }` 

For a stack named MyStack, a value similar to the following is returned:

 `MyStack-MyThing-AB1CDEFGHIJK` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-iot-thing--examples"></a>

### <a name="aws-resource-iot-thing--examples--"></a>

The following example declares a thing and the values of its attributes\.

#### JSON<a name="aws-resource-iot-thing--examples----json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Resources":{
      "MyThing":{
         "Type":"AWS::IoT::Thing",
         "Properties":{
            "ThingName":{
               "Ref":"NameParameter"
            },
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
      }
   },
   "Parameters":{
      "NameParameter":{
         "Type":"String"
      },
      "MyAttributeValueA":{
         "Type":"String",
         "Default":"myStringA123"
      },
      "MyAttributeValueB":{
         "Type":"String",
         "Default":"myStringB123"
      },
      "MyAttributeValueC":{
         "Type":"String",
         "Default":"myStringC123"
      }
   }
}
```

#### YAML<a name="aws-resource-iot-thing--examples----yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyThing:
    Type: AWS::IoT::Thing
    Properties:
      ThingName:
        Ref: NameParameter
      AttributePayload:
        Attributes:
          myAttributeA:
            Ref: MyAttributeValueA
          myAttributeB:
            Ref: MyAttributeValueB
          myAttributeC:
            Ref: MyAttributeValueC
Parameters:
  NameParameter:
    Type: String
  MyAttributeValueA:
    Type: String
    Default: myStringA123
  MyAttributeValueB:
    Type: String
    Default: myStringB123
  MyAttributeValueC:
    Type: String
    Default: myStringC123
```
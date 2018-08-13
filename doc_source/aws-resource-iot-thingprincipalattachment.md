# AWS::IoT::ThingPrincipalAttachment<a name="aws-resource-iot-thingprincipalattachment"></a>

Use the `AWS::IoT::ThingPrincipalAttachment` resource to attach a principal \(an X\.509 certificate or another credential\) to a thing\.

For information about working with AWS IoT things and principals, see [Authorization](http://docs.aws.amazon.com/iot/latest/developerguide/authorization.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="w3ab2c21c10d810b7"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-thingprincipalattachment-syntax.json"></a>

```
{
   "Type": "AWS::IoT::ThingPrincipalAttachment",
   "Properties": {
      "[Principal](#cfn-iot-thingprincipalattachment-principal)": String,
      "[ThingName](#cfn-iot-thingprincipalattachment-thingname)": String
    }
}
```

### YAML<a name="aws-resource-iot-thingprincipalattachment-syntax.yaml"></a>

```
Type: "AWS::IoT::ThingPrincipalAttachment"
Properties:
  [Principal](#cfn-iot-thingprincipalattachment-principal): String
  [ThingName](#cfn-iot-thingprincipalattachment-thingname): String
```

## Properties<a name="w3ab2c21c10d810b9"></a>

`Principal`  <a name="cfn-iot-thingprincipalattachment-principal"></a>
The principal, which can be a certificate ARN \(as returned from the `CreateCertificate` operation\) or an Amazon Cognito ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ThingName`  <a name="cfn-iot-thingprincipalattachment-thingname"></a>
The name of the AWS IoT thing\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Example<a name="w3ab2c21c10d810c11"></a>

The following example attaches a principal to a thing\.

### JSON<a name="aws-resource-iot-thingprincipalattachment-example.json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyThingPrincipalAttachment": {
         "Type": "AWS::IoT::ThingPrincipalAttachment",
         "Properties": {
            "ThingName": {
               "Ref": "NameParameter"
            },
            "Principal": "arn:aws:iot:ap-southeast-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2"
         }
      }
   },
   "Parameters": {
      "NameParameter": {
         "Type": "String"
      }
   }
}
```

### YAML<a name="aws-resource-iot-thingprincipalattachment-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MyThingPrincipalAttachment: 
    Type: "AWS::IoT::ThingPrincipalAttachment"
    Properties: 
      ThingName: 
        Ref: "NameParameter"
      Principal: "arn:aws:iot:ap-southeast-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2"
Parameters: 
  NameParameter: 
    Type: "String"
```
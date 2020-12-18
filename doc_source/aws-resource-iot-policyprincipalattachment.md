# AWS::IoT::PolicyPrincipalAttachment<a name="aws-resource-iot-policyprincipalattachment"></a>

Use the `AWS::IoT::PolicyPrincipalAttachment` resource to attach an AWS IoT policy to a principal \(an X\.509 certificate or other credential\)\.

For information about working with AWS IoT policies and principals, see [Authorization](https://docs.aws.amazon.com/iot/latest/developerguide/authorization.html) in the *AWS IoT Developer Guide*\.

## Syntax<a name="aws-resource-iot-policyprincipalattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-policyprincipalattachment-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::PolicyPrincipalAttachment",
  "Properties" : {
      "[PolicyName](#cfn-iot-policyprincipalattachment-policyname)" : String,
      "[Principal](#cfn-iot-policyprincipalattachment-principal)" : String
    }
}
```

### YAML<a name="aws-resource-iot-policyprincipalattachment-syntax.yaml"></a>

```
Type: AWS::IoT::PolicyPrincipalAttachment
Properties: 
  [PolicyName](#cfn-iot-policyprincipalattachment-policyname): String
  [Principal](#cfn-iot-policyprincipalattachment-principal): String
```

## Properties<a name="aws-resource-iot-policyprincipalattachment-properties"></a>

`PolicyName`  <a name="cfn-iot-policyprincipalattachment-policyname"></a>
The name of the AWS IoT policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Principal`  <a name="cfn-iot-policyprincipalattachment-principal"></a>
The principal, which can be a certificate ARN \(as returned from the `CreateCertificate` operation\) or an Amazon Cognito ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-iot-policyprincipalattachment--examples"></a>



### <a name="aws-resource-iot-policyprincipalattachment--examples--"></a>

The following example attaches a policy to a principal\.

#### JSON<a name="aws-resource-iot-policyprincipalattachment--examples----json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Resources":{
      "MyPolicyPrincipalAttachment":{
         "Type":"AWS::IoT::PolicyPrincipalAttachment",
         "Properties":{
            "PolicyName":{
               "Ref":"NameParameter"
            },
            "Principal":"arn:aws:iot:ap-southeast-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2"
         }
      }
   },
   "Parameters":{
      "NameParameter":{
         "Type":"String"
      }
   }
}
```

#### YAML<a name="aws-resource-iot-policyprincipalattachment--examples----yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyPolicyPrincipalAttachment:
    Type: AWS::IoT::PolicyPrincipalAttachment
    Properties:
      PolicyName:
        Ref: NameParameter
      Principal: arn:aws:iot:ap-southeast-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2
Parameters:
  NameParameter:
    Type: String
```
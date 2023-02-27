# AWS::Connect::SecurityKey<a name="aws-resource-connect-securitykey"></a>

The security key for the instance\.

**Note**  
Only two security keys are allowed per Amazon Connect instance\.

## Syntax<a name="aws-resource-connect-securitykey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-securitykey-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::SecurityKey",
  "Properties" : {
      "[InstanceId](#cfn-connect-securitykey-instanceid)" : String,
      "[Key](#cfn-connect-securitykey-key)" : String
    }
}
```

### YAML<a name="aws-resource-connect-securitykey-syntax.yaml"></a>

```
Type: AWS::Connect::SecurityKey
Properties: 
  [InstanceId](#cfn-connect-securitykey-instanceid): String
  [Key](#cfn-connect-securitykey-key): String
```

## Properties<a name="aws-resource-connect-securitykey-properties"></a>

`InstanceId`  <a name="cfn-connect-securitykey-instanceid"></a>
The Amazon Resource Name \(ARN\) of the instance\.  
*Minimum*: `1`  
*Maximum*: `100`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Key`  <a name="cfn-connect-securitykey-key"></a>
A valid security key in PEM format\.  
*Minimum*: `1`  
*Maximum*: `1024`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-connect-securitykey-return-values"></a>

### Ref<a name="aws-resource-connect-securitykey-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-connect-securitykey-return-values-fn--getatt"></a>

#### <a name="aws-resource-connect-securitykey-return-values-fn--getatt-fn--getatt"></a>

`AssociationId`  <a name="AssociationId-fn::getatt"></a>
An `AssociationId` is automatically generated when a storage config is associated with an instance\.

## Examples<a name="aws-resource-connect-securitykey--examples"></a>



### Specify a security key for an Amazon Connect instance<a name="aws-resource-connect-securitykey--examples--Specify_a_security_key_for_an_Amazon_Connect_instance"></a>

The following example specifies a security key for an Amazon Connect instance\.

#### YAML<a name="aws-resource-connect-securitykey--examples--Specify_a_security_key_for_an_Amazon_Connect_instance--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a security key for an Amazon Connect instance
Resources:
  SecurityKey:
    Type: AWS::Connect::SecurityKey
    Properties:
      InstanceId: arn:aws:connect:region-name:aws-account-id:instance/instance-arn
      Key: "valid-pem-key"
```
# AWS::VerifiedPermissions::PolicyStore<a name="aws-resource-verifiedpermissions-policystore"></a>

Creates a policy store\. A policy store is a container for policy resources\. You can create a separate policy store for each of your applications\.

## Syntax<a name="aws-resource-verifiedpermissions-policystore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-verifiedpermissions-policystore-syntax.json"></a>

```
{
  "Type" : "AWS::VerifiedPermissions::PolicyStore",
  "Properties" : {
      "[Schema](#cfn-verifiedpermissions-policystore-schema)" : SchemaDefinition,
      "[ValidationSettings](#cfn-verifiedpermissions-policystore-validationsettings)" : ValidationSettings
    }
}
```

### YAML<a name="aws-resource-verifiedpermissions-policystore-syntax.yaml"></a>

```
Type: AWS::VerifiedPermissions::PolicyStore
Properties: 
  [Schema](#cfn-verifiedpermissions-policystore-schema): 
    SchemaDefinition
  [ValidationSettings](#cfn-verifiedpermissions-policystore-validationsettings): 
    ValidationSettings
```

## Properties<a name="aws-resource-verifiedpermissions-policystore-properties"></a>

`Schema`  <a name="cfn-verifiedpermissions-policystore-schema"></a>
Creates or updates the policy schema in a policy store\. Cedar can use the schema to validate any Cedar policies and policy templates submitted to the policy store\. Any changes to the schema validate only policies and templates submitted after the schema change\. Existing policies and templates are not re\-evaluated against the changed schema\. If you later update a policy, then it is evaluated against the new schema at that time\.  
*Required*: No  
*Type*: [SchemaDefinition](aws-properties-verifiedpermissions-policystore-schemadefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidationSettings`  <a name="cfn-verifiedpermissions-policystore-validationsettings"></a>
Specifies the validation setting for this policy store\.  
Currently, the only valid and required value is `Mode`\.  
We recommend that you turn on `STRICT` mode only after you define a schema\. If a schema doesn't exist, then `STRICT` mode causes any policy to fail validation, and Verified Permissions rejects the policy\. You can turn off validation by using the [UpdatePolicyStore](https://docs.aws.amazon.com/verifiedpermissions/latest/apireference/API_UpdatePolicyStore)\. Then, when you have a schema defined, use [UpdatePolicyStore](https://docs.aws.amazon.com/verifiedpermissions/latest/apireference/API_UpdatePolicyStore) again to turn validation back on\.
*Required*: Yes  
*Type*: [ValidationSettings](aws-properties-verifiedpermissions-policystore-validationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-verifiedpermissions-policystore-return-values"></a>

### Ref<a name="aws-resource-verifiedpermissions-policystore-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the unique id of the new or updated policy store\. For example:

`{ "Ref": "PSEXAMPLEabcdefg111111" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-verifiedpermissions-policystore-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-verifiedpermissions-policystore-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The [Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the new or updated policy store\.

`PolicyStoreId`  <a name="PolicyStoreId-fn::getatt"></a>
The unique ID of the new or updated policy store\.

## Examples<a name="aws-resource-verifiedpermissions-policystore--examples"></a>



### Creating a policy store with a schema and verification enabled<a name="aws-resource-verifiedpermissions-policystore--examples--Creating_a_policy_store_with_a_schema_and_verification_enabled"></a>

The following example creates a policy store that is configured with a schema and policy validation against that schema turned on\.

#### JSON<a name="aws-resource-verifiedpermissions-policystore--examples--Creating_a_policy_store_with_a_schema_and_verification_enabled--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation sample template for creating a policy store for Verified Permissions.",
    "Resources": {
        "MyPolicyStore": {
            "Type": "AWS::VerifiedPermissions::PolicyStore",
            "Properties": {
                "Schema": {
                    "CedarJson": "{\"PhotoApp\":{\"commonTypes\":{\"PersonType\":{\"type\":\"Record\",\"attributes\":{\"age\":{\"type\":\"Long\"},\"name\":{\"type\":\"String\"}}},\"ContextType\":{\"type\":\"Record\",\"attributes\":{\"ip\":{\"type\":\"Extension\",\"name\":\"ipaddr\",\"required\":false},\"authenticated\":{\"type\":\"Boolean\",\"required\":true}}}},\"entityTypes\":{\"User\":{\"shape\":{\"type\":\"Record\",\"attributes\":{\"userId\":{\"type\":\"String\"},\"personInformation\":{\"type\":\"PersonType\"}}},\"memberOfTypes\":[\"UserGroup\"]},\"UserGroup\":{\"shape\":{\"type\":\"Record\",\"attributes\":{}}},\"Photo\":{\"shape\":{\"type\":\"Record\",\"attributes\":{\"account\":{\"type\":\"Entity\",\"name\":\"Account\",\"required\":true},\"private\":{\"type\":\"Boolean\",\"required\":true}}},\"memberOfTypes\":[\"Album\",\"Account\"]},\"Album\":{\"shape\":{\"type\":\"Record\",\"attributes\":{}}},\"Account\":{\"shape\":{\"type\":\"Record\",\"attributes\":{}}}},\"actions\":{\"viewPhoto\":{\"appliesTo\":{\"principalTypes\":[\"User\",\"UserGroup\"],\"resourceTypes\":[\"Photo\"],\"context\":{\"type\":\"ContextType\"}}},\"createPhoto\":{\"appliesTo\":{\"principalTypes\":[\"User\",\"UserGroup\"],\"resourceTypes\":[\"Photo\"],\"context\":{\"type\":\"ContextType\"}}},\"listPhotos\":{\"appliesTo\":{\"principalTypes\":[\"User\",\"UserGroup\"],\"resourceTypes\":[\"Photo\"],\"context\":{\"type\":\"ContextType\"}}}}}}"
                },
                "ValidationSettings": {
                    "Mode": "STRICT"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-verifiedpermissions-policystore--examples--Creating_a_policy_store_with_a_schema_and_verification_enabled--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  Description": "AWS CloudFormation sample template for creating a policy store for Verified Permissions." 
Resources:
  MyPolicyStore:
    Type: AWS::VerifiedPermissions::PolicyStore
    Properties:
      Schema:
        CedarJson: '{"PhotoApp":{"commonTypes":{"PersonType":{"type":"Record","attributes":{"age":{"type":"Long"},"name":{"type":"String"}}},"ContextType":{"type":"Record","attributes":{"ip":{"type":"Extension","name":"ipaddr","required":false},"authenticated":{"type":"Boolean","required":true}}}},"entityTypes":{"User":{"shape":{"type":"Record","attributes":{"userId":{"type":"String"},"personInformation":{"type":"PersonType"}}},"memberOfTypes":["UserGroup"]},"UserGroup":{"shape":{"type":"Record","attributes":{}}},"Photo":{"shape":{"type":"Record","attributes":{"account":{"type":"Entity","name":"Account","required":true},"private":{"type":"Boolean","required":true}}},"memberOfTypes":["Album","Account"]},"Album":{"shape":{"type":"Record","attributes":{}}},"Account":{"shape":{"type":"Record","attributes":{}}}},"actions":{"viewPhoto":{"appliesTo":{"principalTypes":["User","UserGroup"],"resourceTypes":["Photo"],"context":{"type":"ContextType"}}},"createPhoto":{"appliesTo":{"principalTypes":["User","UserGroup"],"resourceTypes":["Photo"],"context":{"type":"ContextType"}}},"listPhotos":{"appliesTo":{"principalTypes":["User","UserGroup"],"resourceTypes":["Photo"],"context":{"type":"ContextType"}}}}}}'
      ValidationSettings:
        Mode: STRICT
```
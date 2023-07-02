# AWS::VerifiedPermissions::PolicyStore SchemaDefinition<a name="aws-properties-verifiedpermissions-policystore-schemadefinition"></a>

Contains a list of principal types, resource types, and actions that can be specified in policies stored in the same policy store\. If the validation mode for the policy store is set to `STRICT`, then policies that can't be validated by this schema are rejected by Verified Permissions and can't be stored in the policy store\.

## Syntax<a name="aws-properties-verifiedpermissions-policystore-schemadefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-policystore-schemadefinition-syntax.json"></a>

```
{
  "[CedarJson](#cfn-verifiedpermissions-policystore-schemadefinition-cedarjson)" : String
}
```

### YAML<a name="aws-properties-verifiedpermissions-policystore-schemadefinition-syntax.yaml"></a>

```
  [CedarJson](#cfn-verifiedpermissions-policystore-schemadefinition-cedarjson): String
```

## Properties<a name="aws-properties-verifiedpermissions-policystore-schemadefinition-properties"></a>

`CedarJson`  <a name="cfn-verifiedpermissions-policystore-schemadefinition-cedarjson"></a>
A JSON string representation of the schema supported by applications that use this policy store\. For more information, see [Policy store schema](https://docs.aws.amazon.com/verifiedpermissions/latest/userguide/schema.html) in the *Amazon Verified Permissions User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
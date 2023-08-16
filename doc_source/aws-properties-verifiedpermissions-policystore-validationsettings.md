# AWS::VerifiedPermissions::PolicyStore ValidationSettings<a name="aws-properties-verifiedpermissions-policystore-validationsettings"></a>

A structure that contains Cedar policy validation settings for the policy store\. The validation mode determines which validation failures that Cedar considers serious enough to block acceptance of a new or edited static policy or policy template\. 

## Syntax<a name="aws-properties-verifiedpermissions-policystore-validationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-policystore-validationsettings-syntax.json"></a>

```
{
  "[Mode](#cfn-verifiedpermissions-policystore-validationsettings-mode)" : String
}
```

### YAML<a name="aws-properties-verifiedpermissions-policystore-validationsettings-syntax.yaml"></a>

```
  [Mode](#cfn-verifiedpermissions-policystore-validationsettings-mode): String
```

## Properties<a name="aws-properties-verifiedpermissions-policystore-validationsettings-properties"></a>

`Mode`  <a name="cfn-verifiedpermissions-policystore-validationsettings-mode"></a>
The validation mode currently configured for this policy store\. The valid values are:  
+ **OFF** – Neither Verified Permissions nor Cedar perform any validation on policies\. No validation errors are reported by either service\.
+ **STRICT** – Requires a schema to be present in the policy store\. Cedar performs validation on all submitted new or updated static policies and policy templates\. Any that fail validation are rejected and Cedar doesn't store them in the policy store\.
If `Mode=STRICT` and the policy store doesn't contain a schema, Verified Permissions rejects all static policies and policy templates because there is no schema to validate against\.   
To submit a static policy or policy template without a schema, you must turn off validation\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::Cognito::IdentityPoolRoleAttachment<a name="aws-resource-cognito-identitypoolroleattachment"></a>

The `AWS::Cognito::IdentityPoolRoleAttachment` resource manages the role configuration for an Amazon Cognito identity pool\.

**Topics**
+ [Syntax](#aws-resource-cognito-identitypoolroleattachment-syntax)
+ [Properties](#w3ab2c21c10d275b9)
+ [Return Value](#w3ab2c21c10d275c11)

## Syntax<a name="aws-resource-cognito-identitypoolroleattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-identitypoolroleattachment-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::IdentityPoolRoleAttachment",
  "Properties" : {
    "[IdentityPoolId](#cfn-cognito-identitypoolroleattachment-identitypoolid)" : String,
    "[RoleMappings](#cfn-cognito-identitypoolroleattachment-rolemappings)" : String to RoleMapping object map,
    "[Roles](#cfn-cognito-identitypoolroleattachment-roles)" : { String:String, ... }
  }
}
```

### YAML<a name="aws-resource-cognito-identitypoolroleattachment-syntax.yaml"></a>

```
Type: "AWS::Cognito::IdentityPoolRoleAttachment"
Properties:
  [IdentityPoolId](#cfn-cognito-identitypoolroleattachment-identitypoolid): String
  [RoleMappings](#cfn-cognito-identitypoolroleattachment-rolemappings): 
    String to RoleMapping object map
  [Roles](#cfn-cognito-identitypoolroleattachment-roles): 
    String:String
```

## Properties<a name="w3ab2c21c10d275b9"></a>

`IdentityPoolId`  <a name="cfn-cognito-identitypoolroleattachment-identitypoolid"></a>
An identity pool ID in the format `REGION:GUID`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RoleMappings`  <a name="cfn-cognito-identitypoolroleattachment-rolemappings"></a>
How users for a specific identity provider are to mapped to roles\. This is a string to RoleMapping object map\. The string identifies the identity provider, for example, "graph\.facebook\.com" or "cognito\-idp\-east\-1\.amazonaws\.com/us\-east\-1\_abcdefghi:app\_client\_id"  
*Required*: No  
*Type*: String to [Amazon Cognito IdentityPoolRoleAttachment RoleMapping](aws-properties-cognito-identitypoolroleattachment-rolemapping.md) object map\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Roles`  <a name="cfn-cognito-identitypoolroleattachment-roles"></a>
The map of roles associated with this pool\. For a given role, the key will be either "authenticated" or "unauthenticated" and the value will be the Role ARN\.  
*Required*: No  
*Type:* String to string map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d275c11"></a>

### Ref<a name="w3ab2c21c10d275c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns a generated ID, such as `IdentityPoolRoleAttachment-EXAMPLEwnOR3n`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.
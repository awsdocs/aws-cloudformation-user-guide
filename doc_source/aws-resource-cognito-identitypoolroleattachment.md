# AWS::Cognito::IdentityPoolRoleAttachment<a name="aws-resource-cognito-identitypoolroleattachment"></a>

The `AWS::Cognito::IdentityPoolRoleAttachment` resource manages the role configuration for an Amazon Cognito identity pool\.

## Syntax<a name="aws-resource-cognito-identitypoolroleattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-identitypoolroleattachment-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::IdentityPoolRoleAttachment",
  "Properties" : {
      "[IdentityPoolId](#cfn-cognito-identitypoolroleattachment-identitypoolid)" : String,
      "[RoleMappings](#cfn-cognito-identitypoolroleattachment-rolemappings)" : Json,
      "[Roles](#cfn-cognito-identitypoolroleattachment-roles)" : Json
    }
}
```

### YAML<a name="aws-resource-cognito-identitypoolroleattachment-syntax.yaml"></a>

```
Type: AWS::Cognito::IdentityPoolRoleAttachment
Properties : 
﻿  [IdentityPoolId](#cfn-cognito-identitypoolroleattachment-identitypoolid) : String
﻿  [RoleMappings](#cfn-cognito-identitypoolroleattachment-rolemappings) : Json
﻿  [Roles](#cfn-cognito-identitypoolroleattachment-roles) : Json
```

## Properties<a name="aws-resource-cognito-identitypoolroleattachment-properties"></a>

`IdentityPoolId`  <a name="cfn-cognito-identitypoolroleattachment-identitypoolid"></a>
An identity pool ID in the format `REGION:GUID`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleMappings`  <a name="cfn-cognito-identitypoolroleattachment-rolemappings"></a>
How users for a specific identity provider are mapped to roles\. This is a string to RoleMapping object map\. The string identifies the identity provider, for example, "graph\.facebook\.com" or "cognito\-idp\-east\-1\.amazonaws\.com/us\-east\-1\_abcdefghi:app\_client\_id"  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Roles`  <a name="cfn-cognito-identitypoolroleattachment-roles"></a>
The map of roles associated with this pool\. For a given role, the key will be either "authenticated" or "unauthenticated" and the value will be the Role ARN\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-cognito-identitypoolroleattachment-return-values"></a>

### Ref<a name="aws-resource-cognito-identitypoolroleattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a generated ID, such as `IdentityPoolRoleAttachment-EXAMPLEwnOR3n`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.
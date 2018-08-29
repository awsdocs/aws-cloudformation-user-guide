# Amazon Cognito IdentityPoolRoleAttachment RoleMapping<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping"></a>

`RoleMapping` is a property of the [AWS::Cognito::IdentityPoolRoleAttachment](aws-resource-cognito-identitypoolroleattachment.md) resource that defines the role mapping attributes of an Amazon Cognito identity pool\.

## Syntax<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-syntax.json"></a>

```
{
  "[AmbiguousRoleResolution](#cfn-cognito-identitypoolroleattachment-rolemapping-ambiguousroleresolution)" : String,
  "[RulesConfiguration](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration)" : RulesConfiguration,
  "[Type](#cfn-cognito-identitypoolroleattachment-rolemapping-type)" : String
}
```

### YAML<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-syntax.yaml"></a>

```
[AmbiguousRoleResolution](#cfn-cognito-identitypoolroleattachment-rolemapping-ambiguousroleresolution): String,
[RulesConfiguration](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration): RulesConfiguration,
[Type](#cfn-cognito-identitypoolroleattachment-rolemapping-type): String
```

## Properties<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-properties"></a>

`AmbiguousRoleResolution`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-ambiguousroleresolution"></a>
Specifies the action to be taken if either no rules match the claim value for the Rules type, or there is no `cognito:preferred_role` claim and there are multiple `cognito:roles` matches for the Token type\. If you specify Token or Rules as the Type, AmbiguousRoleResolution is required\.  
Valid values are `AuthenticatedRole` or `Deny`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RulesConfiguration`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration"></a>
The rules to be used for mapping users to roles\. If you specify Rules as the role mapping type, RulesConfiguration is required\.  
*Required*: No  
*Type*: [Amazon Cognito IdentityPoolRoleAttachment RoleMapping RulesConfiguration](aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Type`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-type"></a>
The role mapping type\. `Token` will use `cognito:roles` and `cognito:preferred_role` claims from the Amazon Cognito identity provider token to map groups to roles\. `Rules` will attempt to match claims from the token to map to a role\.   
Valid values are `Token` or `Rules`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
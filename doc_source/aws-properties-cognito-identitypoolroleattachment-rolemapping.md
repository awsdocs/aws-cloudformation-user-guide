# AWS::Cognito::IdentityPoolRoleAttachment RoleMapping<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping"></a>

`RoleMapping` is a property of the [AWS::Cognito::IdentityPoolRoleAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-identitypoolroleattachment.html) resource that defines the role\-mapping attributes of an Amazon Cognito identity pool\.

## Syntax<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-syntax.json"></a>

```
{
  "[AmbiguousRoleResolution](#cfn-cognito-identitypoolroleattachment-rolemapping-ambiguousroleresolution)" : String,
  "[IdentityProvider](#cfn-cognito-identitypoolroleattachment-rolemapping-identityprovider)" : String,
  "[RulesConfiguration](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration)" : RulesConfigurationType,
  "[Type](#cfn-cognito-identitypoolroleattachment-rolemapping-type)" : String
}
```

### YAML<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-syntax.yaml"></a>

```
  [AmbiguousRoleResolution](#cfn-cognito-identitypoolroleattachment-rolemapping-ambiguousroleresolution): String
  [IdentityProvider](#cfn-cognito-identitypoolroleattachment-rolemapping-identityprovider): String
  [RulesConfiguration](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration): 
    RulesConfigurationType
  [Type](#cfn-cognito-identitypoolroleattachment-rolemapping-type): String
```

## Properties<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-properties"></a>

`AmbiguousRoleResolution`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-ambiguousroleresolution"></a>
Specifies the action to be taken if either no rules match the claim value for the Rules type, or there is no `cognito:preferred_role` claim and there are multiple `cognito:roles` matches for the Token type\. If you specify Token or Rules as the Type, AmbiguousRoleResolution is required\.  
Valid values are `AuthenticatedRole` or `Deny`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProvider`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-identityprovider"></a>
Identifier for the identity provider for which the role is mapped\. For example: "graph\.facebook\.com" or "cognito\-idp\.us\-east\-1\.amazonaws\.com/us\-east\-1\_abcdefghi:app\_client\_id \(http://cognito\-idp\.us\-east\-1\.amazonaws\.com/us\-east\-1\_abcdefghi:app\_client\_id\)"\. This is the identity provider that is used by the user for authentication\.  
If the identity provider property isn't provided, the key of the entry in the `RoleMappings` map is used as the identity provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RulesConfiguration`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration"></a>
The rules to be used for mapping users to roles\. If you specify "Rules" as the role\-mapping type, RulesConfiguration is required\.  
*Required*: No  
*Type*: [RulesConfigurationType](aws-properties-cognito-identitypoolroleattachment-rulesconfigurationtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-type"></a>
The role\-mapping type\. `Token` uses `cognito:roles` and `cognito:preferred_role` claims from the Amazon Cognito identity provider token to map groups to roles\. `Rules` attempts to match claims from the token to map to a role\.  
Valid values are `Token` or `Rules`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
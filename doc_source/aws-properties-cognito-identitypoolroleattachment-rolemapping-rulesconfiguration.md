# Amazon Cognito IdentityPoolRoleAttachment RoleMapping RulesConfiguration<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration"></a>

`RulesConfiguration` is a subproperty of the [AWS::Cognito::IdentityPoolRoleAttachment](aws-resource-cognito-identitypoolroleattachment.md) property that defines the rules to be used for mapping users to roles\.

## Syntax<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-rules)" : [ MappingRule, .. ]
}
```

### YAML<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-rules): 
  - MappingRule
```

## Properties<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-properties"></a>

`Rules`  
A list of rules\. You can specify up to 25 rules per identity provider\.  
*Required: *Yes  
*Type*: List of [[ERROR] BAD/MISSING LINK TEXT](aws-properties-cognito-identitypoolroleattachment-mappingrule.md)
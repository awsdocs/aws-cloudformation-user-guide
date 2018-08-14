# Amazon Cognito IdentityPoolRoleAttachment RoleMapping RulesConfiguration<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration"></a>

`RulesConfiguration` is a subproperty of the [AWS::Cognito::IdentityPoolRoleAttachment](aws-resource-cognito-identitypoolroleattachment.md) property that defines the rules to be used for mapping users to roles\.

## Syntax<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-syntax.json"></a>

```
{
  "[Rules](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-rules)" : [ [*MappingRule*](aws-properties-cognito-identitypoolroleattachment-mappingrule.md), .. ]
}
```

### YAML<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-syntax.yaml"></a>

```
[Rules](#cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-rules): 
  - [*MappingRule*](aws-properties-cognito-identitypoolroleattachment-mappingrule.md)
```

## Properties<a name="aws-properties-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-properties"></a>

`Rules`  <a name="cfn-cognito-identitypoolroleattachment-rolemapping-rulesconfiguration-rules"></a>
A list of rules\. You can specify up to 25 rules per identity provider\.  
*Required*: Yes  
*Type*: List of [Amazon Cognito IdentityPoolRoleAttachment MappingRule](aws-properties-cognito-identitypoolroleattachment-mappingrule.md)
# Amazon Cognito IdentityPoolRoleAttachment MappingRule<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule"></a>

`MappingRule` is a subproperty of the [Amazon Cognito IdentityPoolRoleAttachment RoleMapping](aws-properties-cognito-identitypoolroleattachment-rolemapping.md) property that defines how to map a claim to a role arn\.

## Syntax<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-syntax.json"></a>

```
{
  "[Claim](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-claim)" : String,
  "[MatchType](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-matchtype)" : String,
  "[RoleARN](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-rolearn)" : String,
  "[Value](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-value)" : String
}
```

### YAML<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-syntax.yaml"></a>

```
[Claim](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-claim): String,
[MatchType](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-matchtype): String,
[RoleARN](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-rolearn): String,
[Value](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-value): String
```

## Properties<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-properties"></a>

`Claim`  <a name="cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-claim"></a>
The claim name that must be present in the token, for example, "isAdmin" or "paid\."  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MatchType`  <a name="cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-matchtype"></a>
The match condition that specifies how closely the claim value in the IdP token must match `Value`\.  
Valid values are: `Equals`, `Contains`, `StartsWith`, and `NotEqual`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RoleARN`  <a name="cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Value`  <a name="cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-value"></a>
A brief string that the claim must match, for example, "paid" or "yes\."  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
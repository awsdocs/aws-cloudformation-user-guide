# Amazon Cognito IdentityPoolRoleAttachment MappingRule<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule"></a>

`MappingRule` is a subproperty of the [Amazon Cognito IdentityPoolRoleAttachment RoleMapping](aws-properties-cognito-identitypoolroleattachment-rolemapping.md) property that defines how to map a claim to a role arn\.

## Syntax<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-claim)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-matchtype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-rolearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-value)" : String
}
```

### YAML<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-claim): String,
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-matchtype): String,
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-rolearn): String,
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-mappingrule-value): String
```

## Properties<a name="aws-properties-cognito-identitypoolroleattachment-mappingrule-properties"></a>

`Claim`  
The claim name that must be present in the token, for example, "isAdmin" or "paid\."  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`MatchType`  
The match condition that specifies how closely the claim value in the IdP token must match `Value`\.  
Valid values are: `Equals`, `Contains`, `StartsWith`, and `NotEqual`\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`RoleARN`  
The Amazon Resource Name \(ARN\) of the role\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Value`  
A brief string that the claim must match, for example, "paid" or "yes\."  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption
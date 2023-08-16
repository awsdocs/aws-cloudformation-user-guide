# AWS::EKS::IdentityProviderConfig OidcIdentityProviderConfig<a name="aws-properties-eks-identityproviderconfig-oidcidentityproviderconfig"></a>

An object representing the configuration for an OpenID Connect \(OIDC\) identity provider\. 

## Syntax<a name="aws-properties-eks-identityproviderconfig-oidcidentityproviderconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-identityproviderconfig-oidcidentityproviderconfig-syntax.json"></a>

```
{
  "[ClientId](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-clientid)" : String,
  "[GroupsClaim](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-groupsclaim)" : String,
  "[GroupsPrefix](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-groupsprefix)" : String,
  "[IssuerUrl](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-issuerurl)" : String,
  "[RequiredClaims](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-requiredclaims)" : [ RequiredClaim, ... ],
  "[UsernameClaim](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-usernameclaim)" : String,
  "[UsernamePrefix](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-usernameprefix)" : String
}
```

### YAML<a name="aws-properties-eks-identityproviderconfig-oidcidentityproviderconfig-syntax.yaml"></a>

```
  [ClientId](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-clientid): String
  [GroupsClaim](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-groupsclaim): String
  [GroupsPrefix](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-groupsprefix): String
  [IssuerUrl](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-issuerurl): String
  [RequiredClaims](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-requiredclaims): 
    - RequiredClaim
  [UsernameClaim](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-usernameclaim): String
  [UsernamePrefix](#cfn-eks-identityproviderconfig-oidcidentityproviderconfig-usernameprefix): String
```

## Properties<a name="aws-properties-eks-identityproviderconfig-oidcidentityproviderconfig-properties"></a>

`ClientId`  <a name="cfn-eks-identityproviderconfig-oidcidentityproviderconfig-clientid"></a>
This is also known as *audience*\. The ID of the client application that makes authentication requests to the OIDC identity provider\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupsClaim`  <a name="cfn-eks-identityproviderconfig-oidcidentityproviderconfig-groupsclaim"></a>
The JSON web token \(JWT\) claim that the provider uses to return your groups\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupsPrefix`  <a name="cfn-eks-identityproviderconfig-oidcidentityproviderconfig-groupsprefix"></a>
The prefix that is prepended to group claims to prevent clashes with existing names \(such as `system:` groups\)\. For example, the value` oidc:` creates group names like `oidc:engineering` and `oidc:infra`\. The prefix can't contain `system:`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IssuerUrl`  <a name="cfn-eks-identityproviderconfig-oidcidentityproviderconfig-issuerurl"></a>
The URL of the OIDC identity provider that allows the API server to discover public signing keys for verifying tokens\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RequiredClaims`  <a name="cfn-eks-identityproviderconfig-oidcidentityproviderconfig-requiredclaims"></a>
The key\-value pairs that describe required claims in the identity token\. If set, each claim is verified to be present in the token with a matching value\.  
*Required*: No  
*Type*: List of [RequiredClaim](aws-properties-eks-identityproviderconfig-requiredclaim.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UsernameClaim`  <a name="cfn-eks-identityproviderconfig-oidcidentityproviderconfig-usernameclaim"></a>
The JSON Web token \(JWT\) claim that is used as the username\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UsernamePrefix`  <a name="cfn-eks-identityproviderconfig-oidcidentityproviderconfig-usernameprefix"></a>
The prefix that is prepended to username claims to prevent clashes with existing names\. The prefix can't contain `system:`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
# AWS::WorkSpacesWeb::IdentityProvider<a name="aws-resource-workspacesweb-identityprovider"></a>

This resource specifies an identity provider that is then associated with a web portal\. This resource is not required if your portal's `AuthenticationType` is IAM Identity Center\.

## Syntax<a name="aws-resource-workspacesweb-identityprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspacesweb-identityprovider-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpacesWeb::IdentityProvider",
  "Properties" : {
      "[IdentityProviderDetails](#cfn-workspacesweb-identityprovider-identityproviderdetails)" : {Key: Value, ...},
      "[IdentityProviderName](#cfn-workspacesweb-identityprovider-identityprovidername)" : String,
      "[IdentityProviderType](#cfn-workspacesweb-identityprovider-identityprovidertype)" : String,
      "[PortalArn](#cfn-workspacesweb-identityprovider-portalarn)" : String
    }
}
```

### YAML<a name="aws-resource-workspacesweb-identityprovider-syntax.yaml"></a>

```
Type: AWS::WorkSpacesWeb::IdentityProvider
Properties: 
  [IdentityProviderDetails](#cfn-workspacesweb-identityprovider-identityproviderdetails): 
    Key: Value
  [IdentityProviderName](#cfn-workspacesweb-identityprovider-identityprovidername): String
  [IdentityProviderType](#cfn-workspacesweb-identityprovider-identityprovidertype): String
  [PortalArn](#cfn-workspacesweb-identityprovider-portalarn): String
```

## Properties<a name="aws-resource-workspacesweb-identityprovider-properties"></a>

`IdentityProviderDetails`  <a name="cfn-workspacesweb-identityprovider-identityproviderdetails"></a>
The identity provider details\. The following list describes the provider detail keys for each identity provider type\.   
+ For Google and Login with Amazon:
  + `client_id`
  + `client_secret`
  + `authorize_scopes`
+ For Facebook:
  + `client_id`
  + `client_secret`
  + `authorize_scopes`
  + `api_version`
+ For Sign in with Apple:
  + `client_id`
  + `team_id`
  + `key_id`
  + `private_key`
  + `authorize_scopes`
+ For OIDC providers:
  + `client_id`
  + `client_secret`
  + `attributes_request_method`
  + `oidc_issuer`
  + `authorize_scopes`
  + `authorize_url` *if not available from discovery URL specified by oidc\_issuer key*
  + `token_url` *if not available from discovery URL specified by oidc\_issuer key*
  + `attributes_url` *if not available from discovery URL specified by oidc\_issuer key*
  + `jwks_uri` *if not available from discovery URL specified by oidc\_issuer key*
+ For SAML providers:
  +  `MetadataFile` OR `MetadataURL` 
  +  `IDPSignout` *optional* 
*Required*: Yes  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderName`  <a name="cfn-workspacesweb-identityprovider-identityprovidername"></a>
The identity provider name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[^_][\p{L}\p{M}\p{S}\p{N}\p{P}][^_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderType`  <a name="cfn-workspacesweb-identityprovider-identityprovidertype"></a>
The identity provider type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Facebook | Google | LoginWithAmazon | OIDC | SAML | SignInWithApple`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortalArn`  <a name="cfn-workspacesweb-identityprovider-portalarn"></a>
The ARN of the identity provider\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=\/,.@-]+:[a-zA-Z0-9\-]+:[a-zA-Z0-9\-]*:[a-zA-Z0-9]{1,12}:[a-zA-Z]+(\/[a-fA-F0-9\-]{36}){2,}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-workspacesweb-identityprovider-return-values"></a>

### Ref<a name="aws-resource-workspacesweb-identityprovider-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource's Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-workspacesweb-identityprovider-return-values-fn--getatt"></a>

#### <a name="aws-resource-workspacesweb-identityprovider-return-values-fn--getatt-fn--getatt"></a>

`IdentityProviderArn`  <a name="IdentityProviderArn-fn::getatt"></a>
The ARN of the identity provider\.
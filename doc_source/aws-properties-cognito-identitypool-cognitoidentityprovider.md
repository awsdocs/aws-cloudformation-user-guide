# Amazon Cognito IdentityPool CognitoIdentityProvider<a name="aws-properties-cognito-identitypool-cognitoidentityprovider"></a>

`CognitoIdentityProvider` is a property of the [AWS::Cognito::IdentityPool](aws-resource-cognito-identitypool.md) resource that represents an Amazon Cognito user pool and its client ID\.

## Syntax<a name="aws-properties-cognito-identitypool-cognitoidentityprovider-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypool-cognitoidentityprovider-syntax.json"></a>

```
{
  "[ClientId](#cfn-cognito-identitypool-cognitoidentityprovider-clientid)" : String,
  "[ProviderName](#cfn-cognito-identitypool-cognitoidentityprovider-providername)" : String,
  "[ServerSideTokenCheck](#cfn-cognito-identitypool-cognitoidentityprovider-serversidetokencheck)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-identitypool-cognitoidentityprovider-syntax.yaml"></a>

```
[ClientId](#cfn-cognito-identitypool-cognitoidentityprovider-clientid): String
[ProviderName](#cfn-cognito-identitypool-cognitoidentityprovider-providername): String
[ServerSideTokenCheck](#cfn-cognito-identitypool-cognitoidentityprovider-serversidetokencheck): Boolean
```

## Properties<a name="aws-properties-cognito-identitypool-cognitoidentityprovider-properties"></a>

`ClientId`  <a name="cfn-cognito-identitypool-cognitoidentityprovider-clientid"></a>
The client ID for the Amazon Cognito user pool\.  
*Type*: String  
*Required*: No

`ProviderName`  <a name="cfn-cognito-identitypool-cognitoidentityprovider-providername"></a>
The provider name for an Amazon Cognito user pool\. For example, `cognito-idp.us-east-2.amazonaws.com/us-east-2_123456789`\.  
*Type*: String  
*Required*: No

`ServerSideTokenCheck`  <a name="cfn-cognito-identitypool-cognitoidentityprovider-serversidetokencheck"></a>
TRUE if server\-side token validation is enabled for the identity provider’s token\.  
Once you set `ServerSideTokenCheck` to TRUE for an identity pool, that identity pool will check with the integrated user pools to make sure that the user has not been globally signed out or deleted before the identity pool provides an OIDC token or AWS credentials for the user\.  
If the user is signed out or deleted, the identity pool will return a 400 Not Authorized error\.  
*Type*: Boolean  
*Required*: No
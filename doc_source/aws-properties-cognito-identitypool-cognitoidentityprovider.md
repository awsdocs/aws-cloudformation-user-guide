# AWS::Cognito::IdentityPool CognitoIdentityProvider<a name="aws-properties-cognito-identitypool-cognitoidentityprovider"></a>

`CognitoIdentityProvider` is a property of the [AWS::Cognito::IdentityPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-identitypool.html) resource that represents an Amazon Cognito user pool and its client ID\.

## Syntax<a name="aws-properties-cognito-identitypool-cognitoidentityprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProviderName`  <a name="cfn-cognito-identitypool-cognitoidentityprovider-providername"></a>
The provider name for an Amazon Cognito user pool\. For example: `cognito-idp.us-east-2.amazonaws.com/us-east-2_123456789`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerSideTokenCheck`  <a name="cfn-cognito-identitypool-cognitoidentityprovider-serversidetokencheck"></a>
TRUE if server\-side token validation is enabled for the identity provider’s token\.  
After you set the `ServerSideTokenCheck` to TRUE for an identity pool, that identity pool checks with the integrated user pools to make sure the user has not been globally signed out or deleted before the identity pool provides an OIDC token or AWS credentials for the user\.  
If the user is signed out or deleted, the identity pool returns a 400 Not Authorized error\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
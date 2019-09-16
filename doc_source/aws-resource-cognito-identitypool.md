# AWS::Cognito::IdentityPool<a name="aws-resource-cognito-identitypool"></a>

The `AWS::Cognito::IdentityPool` resource creates an Amazon Cognito identity pool\.

## Syntax<a name="aws-resource-cognito-identitypool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-identitypool-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::IdentityPool",
  "Properties" : {
      "[AllowUnauthenticatedIdentities](#cfn-cognito-identitypool-allowunauthenticatedidentities)" : Boolean,
      "[CognitoEvents](#cfn-cognito-identitypool-cognitoevents)" : Json,
      "[CognitoIdentityProviders](#cfn-cognito-identitypool-cognitoidentityproviders)" : [ [CognitoIdentityProvider](aws-properties-cognito-identitypool-cognitoidentityprovider.md), ... ],
      "[CognitoStreams](#cfn-cognito-identitypool-cognitostreams)" : [CognitoStreams](aws-properties-cognito-identitypool-cognitostreams.md),
      "[DeveloperProviderName](#cfn-cognito-identitypool-developerprovidername)" : String,
      "[IdentityPoolName](#cfn-cognito-identitypool-identitypoolname)" : String,
      "[OpenIdConnectProviderARNs](#cfn-cognito-identitypool-openidconnectproviderarns)" : [ String, ... ],
      "[PushSync](#cfn-cognito-identitypool-pushsync)" : [PushSync](aws-properties-cognito-identitypool-pushsync.md),
      "[SamlProviderARNs](#cfn-cognito-identitypool-samlproviderarns)" : [ String, ... ],
      "[SupportedLoginProviders](#cfn-cognito-identitypool-supportedloginproviders)" : Json
    }
}
```

### YAML<a name="aws-resource-cognito-identitypool-syntax.yaml"></a>

```
Type: AWS::Cognito::IdentityPool
Properties: 
  [AllowUnauthenticatedIdentities](#cfn-cognito-identitypool-allowunauthenticatedidentities): Boolean
  [CognitoEvents](#cfn-cognito-identitypool-cognitoevents): Json
  [CognitoIdentityProviders](#cfn-cognito-identitypool-cognitoidentityproviders): 
    - [CognitoIdentityProvider](aws-properties-cognito-identitypool-cognitoidentityprovider.md)
  [CognitoStreams](#cfn-cognito-identitypool-cognitostreams): 
    [CognitoStreams](aws-properties-cognito-identitypool-cognitostreams.md)
  [DeveloperProviderName](#cfn-cognito-identitypool-developerprovidername): String
  [IdentityPoolName](#cfn-cognito-identitypool-identitypoolname): String
  [OpenIdConnectProviderARNs](#cfn-cognito-identitypool-openidconnectproviderarns): 
    - String
  [PushSync](#cfn-cognito-identitypool-pushsync): 
    [PushSync](aws-properties-cognito-identitypool-pushsync.md)
  [SamlProviderARNs](#cfn-cognito-identitypool-samlproviderarns): 
    - String
  [SupportedLoginProviders](#cfn-cognito-identitypool-supportedloginproviders): Json
```

## Properties<a name="aws-resource-cognito-identitypool-properties"></a>

`AllowUnauthenticatedIdentities`  <a name="cfn-cognito-identitypool-allowunauthenticatedidentities"></a>
Specifies whether the identity pool supports unauthenticated logins\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CognitoEvents`  <a name="cfn-cognito-identitypool-cognitoevents"></a>
The events to configure\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CognitoIdentityProviders`  <a name="cfn-cognito-identitypool-cognitoidentityproviders"></a>
An array of Amazon Cognito user pools and their client IDs\.  
*Required*: No  
*Type*: List of [CognitoIdentityProvider](aws-properties-cognito-identitypool-cognitoidentityprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CognitoStreams`  <a name="cfn-cognito-identitypool-cognitostreams"></a>
Configuration options for configuring Amazon Cognito streams\.  
*Required*: No  
*Type*: [CognitoStreams](aws-properties-cognito-identitypool-cognitostreams.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeveloperProviderName`  <a name="cfn-cognito-identitypool-developerprovidername"></a>
The "domain" by which Amazon Cognito will refer to your users\. This name acts as a placeholder that allows your backend and the Amazon Cognito service to communicate about the developer provider\. For the `DeveloperProviderName`, you can use letters and periods \(\.\), underscores \(\_\), and dashes \(\-\)\.  
*Minimum length*: 1  
*Maximum length*: 100  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityPoolName`  <a name="cfn-cognito-identitypool-identitypoolname"></a>
The name of your Amazon Cognito identity pool\.  
*Minimum length*: 1  
*Maximum length*: 128  
*Pattern*: `[\w ]+`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenIdConnectProviderARNs`  <a name="cfn-cognito-identitypool-openidconnectproviderarns"></a>
A list of ARNs for the OpendID Connect provider\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PushSync`  <a name="cfn-cognito-identitypool-pushsync"></a>
Configuration options to be applied to the identity pool\.  
*Required*: No  
*Type*: [PushSync](aws-properties-cognito-identitypool-pushsync.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamlProviderARNs`  <a name="cfn-cognito-identitypool-samlproviderarns"></a>
A list of Amazon Resource Names \(ARNs\) of Security Assertion Markup Language \(SAML\) providers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportedLoginProviders`  <a name="cfn-cognito-identitypool-supportedloginproviders"></a>
Key\-value pairs that map provider names to provider app IDs\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-cognito-identitypool-return-values"></a>

### Ref<a name="aws-resource-cognito-identitypool-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `IdentityPoolId`, such as `us-east-2:0d01f4d7-1305-4408-b437-12345EXAMPLE`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cognito-identitypool-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cognito-identitypool-return-values-fn--getatt-fn--getatt"></a>

`Name`  <a name="Name-fn::getatt"></a>
The name of the Amazon Cognito identity pool, returned as a string\.
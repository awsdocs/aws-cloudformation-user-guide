# AWS::Cognito::IdentityPool<a name="aws-resource-cognito-identitypool"></a>

The `AWS::Cognito::IdentityPool` resource creates an Amazon Cognito identity pool\.

**Topics**
+ [Syntax](#aws-resource-cognito-identitypool-syntax)
+ [Properties](#w3ab2c21c10d271b9)
+ [Return Value](#w3ab2c21c10d271c11)

## Syntax<a name="aws-resource-cognito-identitypool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-identitypool-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::IdentityPool",
  "Properties" : {
    "[IdentityPoolName](#cfn-cognito-identitypool-identitypoolname)" : String,
    "[AllowUnauthenticatedIdentities](#cfn-cognito-identitypool-allowunauthenticatedidentities)" : Boolean, 
    "[DeveloperProviderName](#cfn-cognito-identitypool-developerprovidername)" : String,
    "[SupportedLoginProviders](#cfn-cognito-identitypool-supportedloginproviders)" : { String:String, ... },
    "[CognitoIdentityProviders](#cfn-cognito-identitypool-cognitoidentityproviders)" : [ [*CognitoIdentityProvider*](aws-properties-cognito-identitypool-cognitoidentityprovider.md), ... ], 
    "[SamlProviderARNs](#cfn-cognito-identitypool-samlproviderarns)" : [ String, ... ],
    "[OpenIdConnectProviderARNs](#cfn-cognito-identitypool-openidconnectproviderarns)" : [ String, ... ],
    "[CognitoStreams](#cfn-cognito-identitypool-cognitostreams)" : CognitoStreams, 
    "[PushSync](#cfn-cognito-identitypool-pushsync)" : PushSync,
    "[CognitoEvents](#cfn-cognito-identitypool-cognitoevents)" : { String:String, ... }
  }
}
```

### YAML<a name="aws-resource-cognito-identitypool-syntax.yaml"></a>

```
Type: "AWS::Cognito::IdentityPool"
Properties:
  [IdentityPoolName](#cfn-cognito-identitypool-identitypoolname): String
  [AllowUnauthenticatedIdentities](#cfn-cognito-identitypool-allowunauthenticatedidentities): Boolean
  [DeveloperProviderName](#cfn-cognito-identitypool-developerprovidername): String
  [SupportedLoginProviders](#cfn-cognito-identitypool-supportedloginproviders): 
    String: String
  [CognitoIdentityProviders](#cfn-cognito-identitypool-cognitoidentityproviders): 
    - [*CognitoIdentityProvider*](aws-properties-cognito-identitypool-cognitoidentityprovider.md)
  [SamlProviderARNs](#cfn-cognito-identitypool-samlproviderarns): 
    - String
  [OpenIdConnectProviderARNs](#cfn-cognito-identitypool-openidconnectproviderarns): 
    - String
  [CognitoStreams](#cfn-cognito-identitypool-cognitostreams): 
    - CognitoStreams
  [PushSync](#cfn-cognito-identitypool-pushsync): 
    - PushSync
  [CognitoEvents](#cfn-cognito-identitypool-cognitoevents): 
    String: String
```

## Properties<a name="w3ab2c21c10d271b9"></a>

`IdentityPoolName`  <a name="cfn-cognito-identitypool-identitypoolname"></a>
The name of your Amazon Cognito identity pool\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
MinLength: 1  
MaxLength: 128

`AllowUnauthenticatedIdentities`  <a name="cfn-cognito-identitypool-allowunauthenticatedidentities"></a>
Specifies whether the identity pool supports unauthenticated logins\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DeveloperProviderName`  <a name="cfn-cognito-identitypool-developerprovidername"></a>
The "domain" by which Amazon Cognito will refer to your users\. This name acts as a placeholder that allows your backend and the Amazon Cognito service to communicate about the developer provider\. For the `DeveloperProviderName`, you can use letters and periods \(`.`\), underscores \(`_`\), and dashes \(`-`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
MinLength: 1  
MaxLength: 100

`SupportedLoginProviders`  <a name="cfn-cognito-identitypool-supportedloginproviders"></a>
Key\-value pairs that map provider names to provider app IDs\.  
*Required*: No  
*Type*: String to String map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CognitoIdentityProviders`  <a name="cfn-cognito-identitypool-cognitoidentityproviders"></a>
An array of Amazon Cognito user pools and their client IDs\.  
*Required*: No  
*Type*: An array of [Amazon Cognito IdentityPool CognitoIdentityProvider](aws-properties-cognito-identitypool-cognitoidentityprovider.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SamlProviderARNs`  <a name="cfn-cognito-identitypool-samlproviderarns"></a>
A list of Amazon Resource Names \(ARNs\) of Security Assertion Markup Language \(SAML\) providers\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OpenIdConnectProviderARNs`  <a name="cfn-cognito-identitypool-openidconnectproviderarns"></a>
A list of ARNs for the OpendID Connect provider\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CognitoStreams`  <a name="cfn-cognito-identitypool-cognitostreams"></a>
Configuration options for configuring Amazon Cognito streams\.  
*Required*: No  
*Type*: [Amazon Cognito IdentityPool CognitoStreams](aws-properties-cognito-identitypool-cognitostreams.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PushSync`  <a name="cfn-cognito-identitypool-pushsync"></a>
Configuration options to be applied to the identity pool\.  
*Required*: No  
*Type*: [Amazon Cognito IdentityPool PushSync](aws-properties-cognito-identitypool-pushsync.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CognitoEvents`  <a name="cfn-cognito-identitypool-cognitoevents"></a>
The events to configure\.  
*Required*: No  
*Type:* String to String map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d271c11"></a>

### Ref<a name="w3ab2c21c10d271c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the `IdentityPoolId`, such as `us-east-2:0d01f4d7-1305-4408-b437-12345EXAMPLE`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d271c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Name`  
The name of the Amazon Cognito identity pool, returned as a string\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.
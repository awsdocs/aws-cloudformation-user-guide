# AWS::Cognito::IdentityPool<a name="aws-resource-cognito-identitypool"></a>

The `AWS::Cognito::IdentityPool` resource creates an Amazon Cognito identity pool\.


+ [Syntax](#aws-resource-cognito-identitypool-syntax)
+ [Properties](#w3ab2c21c10d242b9)
+ [Return Value](#w3ab2c21c10d242c11)

## Syntax<a name="aws-resource-cognito-identitypool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-identitypool-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::IdentityPool",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-identitypoolname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-allowunauthenticatedidentities)" : Boolean, 
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-developerprovidername)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-supportedloginproviders)" : { String:String, ... },
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-cognitoidentityproviders)" : [ CognitoIdentityProvider, ... ], 
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-samlproviderarns)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-openidconnectproviderarns)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-cognitostreams)" : CognitoStreams, 
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-pushsync)" : PushSync,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-cognitoevents)" : { String:String, ... }
  }
}
```

### YAML<a name="aws-resource-cognito-identitypool-syntax.yaml"></a>

```
Type: "AWS::Cognito::IdentityPool"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-identitypoolname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-allowunauthenticatedidentities): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-developerprovidername): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-supportedloginproviders): 
    String: String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-cognitoidentityproviders): 
    - CognitoIdentityProvider
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-samlproviderarns): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-openidconnectproviderarns): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-cognitostreams): 
    - CognitoStreams
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-pushsync): 
    - PushSync
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-identitypool-cognitoevents): 
    String: String
```

## Properties<a name="w3ab2c21c10d242b9"></a>

`IdentityPoolName`  
The name of your Amazon Cognito identity pool\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption  
MinLength: 1  
MaxLength: 128

`AllowUnauthenticatedIdentities`  
Specifies whether the identity pool supports unauthenticated logins\.  
*Required: *Yes  
*Type*: Boolean  
*Update requires*: No interruption

`DeveloperProviderName`  
The "domain" by which Amazon Cognito will refer to your users\. This name acts as a placeholder that allows your backend and the Amazon Cognito service to communicate about the developer provider\. For the `DeveloperProviderName`, you can use letters and periods \(`.`\), underscores \(`_`\), and dashes \(`-`\)\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption  
MinLength: 1  
MaxLength: 100

`SupportedLoginProviders`  
Key\-value pairs that map provider names to provider app IDs\.  
*Required: *No  
*Type*: String to String map  
*Update requires*: No interruption

`CognitoIdentityProviders`  
An array of Amazon Cognito user pools and their client IDs\.  
*Required: *No  
*Type*: An array of [[ERROR] BAD/MISSING LINK TEXT](aws-properties-cognito-identitypool-cognitoidentityprovider.md)\.  
*Update requires*: No interruption

`SamlProviderARNs`  
A list of Amazon Resource Names \(ARNs\) of Security Assertion Markup Language \(SAML\) providers\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`OpenIdConnectProviderARNs`  
A list of ARNs for the OpendID Connect provider\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`CognitoStreams`  
Configuration options for configuring Amazon Cognito streams\.  
*Required: *No  
*Type*: [Amazon Cognito IdentityPool CognitoStreams](aws-properties-cognito-identitypool-cognitostreams.md)  
*Update requires*: No interruption

`PushSync`  
Configuration options to be applied to the identity pool\.  
*Required: *No  
*Type*: [Amazon Cognito IdentityPool PushSync](aws-properties-cognito-identitypool-pushsync.md)  
*Update requires*: No interruption

`CognitoEvents`  
The events to configure\.  
*Required: *No  
*Type:* String to String map  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10d242c11"></a>

### Ref<a name="w3ab2c21c10d242c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the `IdentityPoolId`, such as `us-east-2:0d01f4d7-1305-4408-b437-12345EXAMPLE`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d242c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Name`  
The name of the Amazon Cognito identity pool, returned as a string\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.
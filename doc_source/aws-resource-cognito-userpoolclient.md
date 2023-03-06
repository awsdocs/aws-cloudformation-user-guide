# AWS::Cognito::UserPoolClient<a name="aws-resource-cognito-userpoolclient"></a>

The `AWS::Cognito::UserPoolClient` resource specifies an Amazon Cognito user pool client\.

**Note**  
If you don't specify a value for a parameter, Amazon Cognito sets it to a default value\.

## Syntax<a name="aws-resource-cognito-userpoolclient-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolclient-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolClient",
  "Properties" : {
      "[AccessTokenValidity](#cfn-cognito-userpoolclient-accesstokenvalidity)" : Integer,
      "[AllowedOAuthFlows](#cfn-cognito-userpoolclient-allowedoauthflows)" : [ String, ... ],
      "[AllowedOAuthFlowsUserPoolClient](#cfn-cognito-userpoolclient-allowedoauthflowsuserpoolclient)" : Boolean,
      "[AllowedOAuthScopes](#cfn-cognito-userpoolclient-allowedoauthscopes)" : [ String, ... ],
      "[AnalyticsConfiguration](#cfn-cognito-userpoolclient-analyticsconfiguration)" : AnalyticsConfiguration,
      "[AuthSessionValidity](#cfn-cognito-userpoolclient-authsessionvalidity)" : Integer,
      "[CallbackURLs](#cfn-cognito-userpoolclient-callbackurls)" : [ String, ... ],
      "[ClientName](#cfn-cognito-userpoolclient-clientname)" : String,
      "[DefaultRedirectURI](#cfn-cognito-userpoolclient-defaultredirecturi)" : String,
      "[EnablePropagateAdditionalUserContextData](#cfn-cognito-userpoolclient-enablepropagateadditionalusercontextdata)" : Boolean,
      "[EnableTokenRevocation](#cfn-cognito-userpoolclient-enabletokenrevocation)" : Boolean,
      "[ExplicitAuthFlows](#cfn-cognito-userpoolclient-explicitauthflows)" : [ String, ... ],
      "[GenerateSecret](#cfn-cognito-userpoolclient-generatesecret)" : Boolean,
      "[IdTokenValidity](#cfn-cognito-userpoolclient-idtokenvalidity)" : Integer,
      "[LogoutURLs](#cfn-cognito-userpoolclient-logouturls)" : [ String, ... ],
      "[PreventUserExistenceErrors](#cfn-cognito-userpoolclient-preventuserexistenceerrors)" : String,
      "[ReadAttributes](#cfn-cognito-userpoolclient-readattributes)" : [ String, ... ],
      "[RefreshTokenValidity](#cfn-cognito-userpoolclient-refreshtokenvalidity)" : Integer,
      "[SupportedIdentityProviders](#cfn-cognito-userpoolclient-supportedidentityproviders)" : [ String, ... ],
      "[TokenValidityUnits](#cfn-cognito-userpoolclient-tokenvalidityunits)" : TokenValidityUnits,
      "[UserPoolId](#cfn-cognito-userpoolclient-userpoolid)" : String,
      "[WriteAttributes](#cfn-cognito-userpoolclient-writeattributes)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-cognito-userpoolclient-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolClient
Properties: 
  [AccessTokenValidity](#cfn-cognito-userpoolclient-accesstokenvalidity): Integer
  [AllowedOAuthFlows](#cfn-cognito-userpoolclient-allowedoauthflows): 
    - String
  [AllowedOAuthFlowsUserPoolClient](#cfn-cognito-userpoolclient-allowedoauthflowsuserpoolclient): Boolean
  [AllowedOAuthScopes](#cfn-cognito-userpoolclient-allowedoauthscopes): 
    - String
  [AnalyticsConfiguration](#cfn-cognito-userpoolclient-analyticsconfiguration): 
    AnalyticsConfiguration
  [AuthSessionValidity](#cfn-cognito-userpoolclient-authsessionvalidity): Integer
  [CallbackURLs](#cfn-cognito-userpoolclient-callbackurls): 
    - String
  [ClientName](#cfn-cognito-userpoolclient-clientname): String
  [DefaultRedirectURI](#cfn-cognito-userpoolclient-defaultredirecturi): String
  [EnablePropagateAdditionalUserContextData](#cfn-cognito-userpoolclient-enablepropagateadditionalusercontextdata): Boolean
  [EnableTokenRevocation](#cfn-cognito-userpoolclient-enabletokenrevocation): Boolean
  [ExplicitAuthFlows](#cfn-cognito-userpoolclient-explicitauthflows): 
    - String
  [GenerateSecret](#cfn-cognito-userpoolclient-generatesecret): Boolean
  [IdTokenValidity](#cfn-cognito-userpoolclient-idtokenvalidity): Integer
  [LogoutURLs](#cfn-cognito-userpoolclient-logouturls): 
    - String
  [PreventUserExistenceErrors](#cfn-cognito-userpoolclient-preventuserexistenceerrors): String
  [ReadAttributes](#cfn-cognito-userpoolclient-readattributes): 
    - String
  [RefreshTokenValidity](#cfn-cognito-userpoolclient-refreshtokenvalidity): Integer
  [SupportedIdentityProviders](#cfn-cognito-userpoolclient-supportedidentityproviders): 
    - String
  [TokenValidityUnits](#cfn-cognito-userpoolclient-tokenvalidityunits): 
    TokenValidityUnits
  [UserPoolId](#cfn-cognito-userpoolclient-userpoolid): String
  [WriteAttributes](#cfn-cognito-userpoolclient-writeattributes): 
    - String
```

## Properties<a name="aws-resource-cognito-userpoolclient-properties"></a>

`AccessTokenValidity`  <a name="cfn-cognito-userpoolclient-accesstokenvalidity"></a>
The access token time limit\. After this limit expires, your user can't use their access token\. To specify the time unit for `AccessTokenValidity` as `seconds`, `minutes`, `hours`, or `days`, set a `TokenValidityUnits` value in your API request\.  
For example, when you set `AccessTokenValidity` to `10` and `TokenValidityUnits` to `hours`, your user can authorize access with their access token for 10 hours\.  
The default time unit for `AccessTokenValidity` in an API request is hours\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedOAuthFlows`  <a name="cfn-cognito-userpoolclient-allowedoauthflows"></a>
The allowed OAuth flows\.    
code  
Use a code grant flow, which provides an authorization code as the response\. This code can be exchanged for access tokens with the `/oauth2/token` endpoint\.  
implicit  
Issue the access token \(and, optionally, ID token, based on scopes\) directly to your user\.  
client\_credentials  
Issue the access token from the `/oauth2/token` endpoint directly to a non\-person user using a combination of the client ID and client secret\.
*Required*: No  
*Type*: List of String  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedOAuthFlowsUserPoolClient`  <a name="cfn-cognito-userpoolclient-allowedoauthflowsuserpoolclient"></a>
Set to true if the client is allowed to follow the OAuth protocol when interacting with Amazon Cognito user pools\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedOAuthScopes`  <a name="cfn-cognito-userpoolclient-allowedoauthscopes"></a>
The allowed OAuth scopes\. Possible values provided by OAuth are `phone`, `email`, `openid`, and `profile`\. Possible values provided by AWS are `aws.cognito.signin.user.admin`\. Custom scopes created in Resource Servers are also supported\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AnalyticsConfiguration`  <a name="cfn-cognito-userpoolclient-analyticsconfiguration"></a>
The user pool analytics configuration for collecting metrics and sending them to your Amazon Pinpoint campaign\.  
In AWS Regions where Amazon Pinpoint isn't available, user pools only support sending events to Amazon Pinpoint projects in AWS Region us\-east\-1\. In Regions where Amazon Pinpoint is available, user pools support sending events to Amazon Pinpoint projects within that same Region\.
*Required*: No  
*Type*: [AnalyticsConfiguration](aws-properties-cognito-userpoolclient-analyticsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthSessionValidity`  <a name="cfn-cognito-userpoolclient-authsessionvalidity"></a>
Amazon Cognito creates a session token for each API request in an authentication flow\. `AuthSessionValidity` is the duration, in minutes, of that session token\. Your user pool native user must respond to each authentication challenge before the session expires\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `3`  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CallbackURLs`  <a name="cfn-cognito-userpoolclient-callbackurls"></a>
A list of allowed redirect \(callback\) URLs for the IdPs\.  
A redirect URI must:  
+ Be an absolute URI\.
+ Be registered with the authorization server\.
+ Not include a fragment component\.
See [OAuth 2\.0 \- Redirection Endpoint](https://tools.ietf.org/html/rfc6749#section-3.1.2)\.  
Amazon Cognito requires HTTPS over HTTP except for http://localhost for testing purposes only\.  
App callback URLs such as myapp://example are also supported\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientName`  <a name="cfn-cognito-userpoolclient-clientname"></a>
The client name for the user pool client you would like to create\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w\s+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultRedirectURI`  <a name="cfn-cognito-userpoolclient-defaultredirecturi"></a>
The default redirect URI\. Must be in the `CallbackURLs` list\.  
A redirect URI must:  
+ Be an absolute URI\.
+ Be registered with the authorization server\.
+ Not include a fragment component\.
See [OAuth 2\.0 \- Redirection Endpoint](https://tools.ietf.org/html/rfc6749#section-3.1.2)\.  
Amazon Cognito requires HTTPS over HTTP except for http://localhost for testing purposes only\.  
App callback URLs such as myapp://example are also supported\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnablePropagateAdditionalUserContextData`  <a name="cfn-cognito-userpoolclient-enablepropagateadditionalusercontextdata"></a>
Activates the propagation of additional user context data\. For more information about propagation of user context data, see [ Adding advanced security to a user pool](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pool-settings-advanced-security.html)\. If you don’t include this parameter, you can't send device fingerprint information, including source IP address, to Amazon Cognito advanced security\. You can only activate `EnablePropagateAdditionalUserContextData` in an app client that has a client secret\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableTokenRevocation`  <a name="cfn-cognito-userpoolclient-enabletokenrevocation"></a>
Activates or deactivates token revocation\. For more information about revoking tokens, see [RevokeToken](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_RevokeToken.html)\.  
If you don't include this parameter, token revocation is automatically activated for the new user pool client\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExplicitAuthFlows`  <a name="cfn-cognito-userpoolclient-explicitauthflows"></a>
The authentication flows that you want your user pool client to support\. For each app client in your user pool, you can sign in your users with any combination of one or more flows, including with a user name and Secure Remote Password \(SRP\), a user name and password, or a custom authentication process that you define with Lambda functions\.  
If you don't specify a value for `ExplicitAuthFlows`, your user client supports `ALLOW_REFRESH_TOKEN_AUTH`, `ALLOW_USER_SRP_AUTH`, and `ALLOW_CUSTOM_AUTH`\.
Valid values include:  
+  `ALLOW_ADMIN_USER_PASSWORD_AUTH`: Enable admin based user password authentication flow `ADMIN_USER_PASSWORD_AUTH`\. This setting replaces the `ADMIN_NO_SRP_AUTH` setting\. With this authentication flow, your app passes a user name and password to Amazon Cognito in the request, instead of using the Secure Remote Password \(SRP\) protocol to securely transmit the password\.
+  `ALLOW_CUSTOM_AUTH`: Enable Lambda trigger based authentication\.
+  `ALLOW_USER_PASSWORD_AUTH`: Enable user password\-based authentication\. In this flow, Amazon Cognito receives the password in the request instead of using the SRP protocol to verify passwords\.
+  `ALLOW_USER_SRP_AUTH`: Enable SRP\-based authentication\.
+  `ALLOW_REFRESH_TOKEN_AUTH`: Enable authflow to refresh tokens\.
In some environments, you will see the values `ADMIN_NO_SRP_AUTH`, `CUSTOM_AUTH_FLOW_ONLY`, or `USER_PASSWORD_AUTH`\. You can't assign these legacy `ExplicitAuthFlows` values to user pool clients at the same time as values that begin with `ALLOW_`, like `ALLOW_USER_SRP_AUTH`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GenerateSecret`  <a name="cfn-cognito-userpoolclient-generatesecret"></a>
Boolean to specify whether you want to generate a secret for the user pool client being created\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IdTokenValidity`  <a name="cfn-cognito-userpoolclient-idtokenvalidity"></a>
The ID token time limit\. After this limit expires, your user can't use their ID token\. To specify the time unit for `IdTokenValidity` as `seconds`, `minutes`, `hours`, or `days`, set a `TokenValidityUnits` value in your API request\.  
For example, when you set `IdTokenValidity` as `10` and `TokenValidityUnits` as `hours`, your user can authenticate their session with their ID token for 10 hours\.  
The default time unit for `IdTokenValidity` in an API request is hours\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogoutURLs`  <a name="cfn-cognito-userpoolclient-logouturls"></a>
A list of allowed logout URLs for the IdPs\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreventUserExistenceErrors`  <a name="cfn-cognito-userpoolclient-preventuserexistenceerrors"></a>
 Use this setting to choose which errors and responses are returned by Cognito APIs during authentication, account confirmation, and password recovery when the user does not exist in the user pool\. When set to `ENABLED` and the user does not exist, authentication returns an error indicating either the username or password was incorrect, and account confirmation and password recovery return a response indicating a code was sent to a simulated destination\. When set to `LEGACY`, those APIs will return a `UserNotFoundException` exception if the user does not exist in the user pool\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ENABLED | LEGACY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadAttributes`  <a name="cfn-cognito-userpoolclient-readattributes"></a>
The read attributes\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshTokenValidity`  <a name="cfn-cognito-userpoolclient-refreshtokenvalidity"></a>
The refresh token time limit\. After this limit expires, your user can't use their refresh token\. To specify the time unit for `RefreshTokenValidity` as `seconds`, `minutes`, `hours`, or `days`, set a `TokenValidityUnits` value in your API request\.  
For example, when you set `RefreshTokenValidity` as `10` and `TokenValidityUnits` as `days`, your user can refresh their session and retrieve new access and ID tokens for 10 days\.  
The default time unit for `RefreshTokenValidity` in an API request is days\. You can't set `RefreshTokenValidity` to 0\. If you do, Amazon Cognito overrides the value with the default value of 30 days\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportedIdentityProviders`  <a name="cfn-cognito-userpoolclient-supportedidentityproviders"></a>
A list of provider names for the identity providers \(IdPs\) that are supported on this client\. The following are supported: `COGNITO`, `Facebook`, `Google`, `SignInWithApple`, and `LoginWithAmazon`\. You can also specify the names that you configured for the SAML and OIDC IdPs in your user pool, for example `MySAMLIdP` or `MyOIDCIdP`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenValidityUnits`  <a name="cfn-cognito-userpoolclient-tokenvalidityunits"></a>
The units in which the validity times are represented\. The default unit for RefreshToken is days, and default for ID and access tokens are hours\.  
*Required*: No  
*Type*: [TokenValidityUnits](aws-properties-cognito-userpoolclient-tokenvalidityunits.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-cognito-userpoolclient-userpoolid"></a>
The user pool ID for the user pool where you want to create a user pool client\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WriteAttributes`  <a name="cfn-cognito-userpoolclient-writeattributes"></a>
The user pool attributes that the app client can write to\.  
If your app client allows users to sign in through an IdP, this array must include all attributes that you have mapped to IdP attributes\. Amazon Cognito updates mapped attributes when users sign in to your application through an IdP\. If your app client does not have write access to a mapped attribute, Amazon Cognito throws an error when it tries to update the attribute\. For more information, see [Specifying IdP Attribute Mappings for Your user pool](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools-specifying-attribute-mapping.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cognito-userpoolclient-return-values"></a>

### Ref<a name="aws-resource-cognito-userpoolclient-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Cognito user pool client ID, such as `1h57kf5cpq17m0eml12EXAMPLE`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.
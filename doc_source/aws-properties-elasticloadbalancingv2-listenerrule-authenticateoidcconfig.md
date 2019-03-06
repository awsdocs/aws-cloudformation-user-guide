# Elastic Load Balancing V2 AuthenticateOidcConfig<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig"></a>

<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-description"></a>The `AuthenticateOidcConfig` property type specifies request parameters when using an identity provider \(IdP\) that is compliant with OpenID Connect \(OIDC\) to authenticate users\.

<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-inheritance"></a> `AuthenticateOidcConfig` is a property of the [Elastic Load Balancing V2 Actions](aws-properties-elasticloadbalancingv2-listenerrule-actions.md) property type\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-syntax.json"></a>

```
{
  "[AuthenticationRequestExtraParams](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-authenticationrequestextraparams)" : { String:String, ... } ,
  "[AuthorizationEndpoint](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-authorizationendpoint)" : String,
  "[ClientId](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-clientid)" : String,
  "[ClientSecret](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-clientsecret)" : String,
  "[Issuer](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-issuer)" : String,
  "[OnUnauthenticatedRequest](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-onunauthenticatedrequest)" : String,
  "[Scope](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-scope)" : String,
  "[SessionCookieName](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-sessioncookiename)" : String,
  "[SessionTimeout](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-sessiontimeout)" : Number,
  "[TokenEndpoint](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-tokenendpoint)" : String,
  "[UserInfoEndpoint](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-userinfoendpoint)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-syntax.yaml"></a>

```
[AuthenticationRequestExtraParams](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-authenticationrequestextraparams): { String:String, ... }
[AuthorizationEndpoint](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-authorizationendpoint): String
[ClientId](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-clientid): String
[ClientSecret](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-clientsecret): String
[Issuer](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-issuer): String
[OnUnauthenticatedRequest](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-onunauthenticatedrequest): String
[Scope](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-scope): String
[SessionCookieName](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-sessioncookiename): String
[SessionTimeout](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-sessiontimeout): Number
[TokenEndpoint](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-tokenendpoint): String
[UserInfoEndpoint](#cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-userinfoendpoint): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-properties"></a>

`AuthenticationRequestExtraParams`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-authenticationrequestextraparams"></a>
The query parameters \(up to 10\) to include in the redirect request to the authorization endpoint\.  
 *Required*: No  
 *Type*: Map of string\-to\-string values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthorizationEndpoint`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-authorizationendpoint"></a>
The authorization endpoint of the IdP\. This must be a full URL, including the HTTPS protocol, the domain, and the path\.  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ClientId`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-clientid"></a>
The OAuth 2\.0 client identifier\.  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ClientSecret`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-clientsecret"></a>
The OAuth 2\.0 client secret\.  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Issuer`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-issuer"></a>
The OIDC issuer identifier of the IdP\. This must be a full URL, including the HTTPS protocol, the domain, and the path\.  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OnUnauthenticatedRequest`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-onunauthenticatedrequest"></a>
The behavior if the user is not authenticated\. The following are possible values:  
+ `deny`: Return an HTTP 401 Unauthorized error\.
+ `allow`: Allow the request to be forwarded to the target\.
+ authenticate``: Redirect the request to the IdP authorization endpoint\. This is the default value\.
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Scope`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-scope"></a>
The set of user claims to be requested from the IdP\. The default is `openid`\.   
To verify which scope values your IdP supports and how to separate multiple values, see the documentation for your IdP\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SessionCookieName`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-sessioncookiename"></a>
The name of the cookie used to maintain session information\. The default is `AWSELBAuthSessionCookie`\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SessionTimeout`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-sessiontimeout"></a>
The maximum duration of the authentication session, in seconds\. The default is 604800 seconds \(7 days\)\.  
 *Required*: Number  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TokenEndpoint`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-tokenendpoint"></a>
The maximum duration of the authentication session, in seconds\. The default is 604800 seconds \(7 days\)\.  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UserInfoEndpoint`  <a name="cfn-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-userinfoendpoint"></a>
The maximum duration of the authentication session, in seconds\. The default is 604800 seconds \(7 days\)\.  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig-seealso"></a>
+ [AuthenticateOidcActionConfig](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_AuthenticateOidcActionConfig.html) in the *Elastic Load Balancing API Reference version 2015\-12\-01*
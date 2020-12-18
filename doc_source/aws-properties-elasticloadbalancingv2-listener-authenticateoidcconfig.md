# AWS::ElasticLoadBalancingV2::Listener AuthenticateOidcConfig<a name="aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig"></a>

Specifies information required using an identity provide \(IdP\) that is compliant with OpenID Connect \(OIDC\) to authenticate users\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig-syntax.json"></a>

```
{
  "[AuthenticationRequestExtraParams](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-authenticationrequestextraparams)" : {Key : Value, ...},
  "[AuthorizationEndpoint](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-authorizationendpoint)" : String,
  "[ClientId](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-clientid)" : String,
  "[ClientSecret](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-clientsecret)" : String,
  "[Issuer](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-issuer)" : String,
  "[OnUnauthenticatedRequest](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-onunauthenticatedrequest)" : String,
  "[Scope](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-scope)" : String,
  "[SessionCookieName](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-sessioncookiename)" : String,
  "[SessionTimeout](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-sessiontimeout)" : String,
  "[TokenEndpoint](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-tokenendpoint)" : String,
  "[UserInfoEndpoint](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-userinfoendpoint)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig-syntax.yaml"></a>

```
  [AuthenticationRequestExtraParams](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-authenticationrequestextraparams): 
    Key : Value
  [AuthorizationEndpoint](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-authorizationendpoint): String
  [ClientId](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-clientid): String
  [ClientSecret](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-clientsecret): String
  [Issuer](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-issuer): String
  [OnUnauthenticatedRequest](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-onunauthenticatedrequest): String
  [Scope](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-scope): String
  [SessionCookieName](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-sessioncookiename): String
  [SessionTimeout](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-sessiontimeout): String
  [TokenEndpoint](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-tokenendpoint): String
  [UserInfoEndpoint](#cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-userinfoendpoint): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig-properties"></a>

`AuthenticationRequestExtraParams`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-authenticationrequestextraparams"></a>
The query parameters \(up to 10\) to include in the redirect request to the authorization endpoint\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizationEndpoint`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-authorizationendpoint"></a>
The authorization endpoint of the IdP\. This must be a full URL, including the HTTPS protocol, the domain, and the path\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientId`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-clientid"></a>
The OAuth 2\.0 client identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-clientsecret"></a>
The OAuth 2\.0 client secret\. This parameter is required if you are creating a rule\. If you are modifying a rule, you can omit this parameter if you set `UseExistingClientSecret` to true\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Issuer`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-issuer"></a>
The OIDC issuer identifier of the IdP\. This must be a full URL, including the HTTPS protocol, the domain, and the path\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnUnauthenticatedRequest`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-onunauthenticatedrequest"></a>
The behavior if the user is not authenticated\. The following are possible values:  
+ deny`` \- Return an HTTP 401 Unauthorized error\.
+ allow`` \- Allow the request to be forwarded to the target\.
+ authenticate`` \- Redirect the request to the IdP authorization endpoint\. This is the default value\.
*Required*: No  
*Type*: String  
*Allowed values*: `allow | authenticate | deny`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-scope"></a>
The set of user claims to be requested from the IdP\. The default is `openid`\.  
To verify which scope values your IdP supports and how to separate multiple values, see the documentation for your IdP\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionCookieName`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-sessioncookiename"></a>
The name of the cookie used to maintain session information\. The default is AWSELBAuthSessionCookie\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionTimeout`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-sessiontimeout"></a>
The maximum duration of the authentication session, in seconds\. The default is 604800 seconds \(7 days\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenEndpoint`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-tokenendpoint"></a>
The token endpoint of the IdP\. This must be a full URL, including the HTTPS protocol, the domain, and the path\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserInfoEndpoint`  <a name="cfn-elasticloadbalancingv2-listener-authenticateoidcconfig-userinfoendpoint"></a>
The user info endpoint of the IdP\. This must be a full URL, including the HTTPS protocol, the domain, and the path\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
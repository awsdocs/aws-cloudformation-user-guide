# Elastic Load Balancing V2 Actions<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions"></a>

`Actions` is a property of the [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md) resource that specifies the actions an Elastic Load Balancing listener takes when an incoming request meets a listener rule's condition\.

## Syntax<a name="w2922ab1c21c10d120c23c15b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions-syntax.json"></a>

```
{
  "[AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listenerrule-action-authenticatecognitoconfig)" : [*AuthenticateCognitoConfig*](aws-properties-elasticloadbalancingv2-listenerrule-authenticatecognitoconfig.md),
  "[AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listenerrule-action-authenticateoidcconfig)" : [*AuthenticateOidcConfig*](aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig.md),
  "[FixedResponseConfig](#cfn-elasticloadbalancingv2-listenerrule-action-fixedresponseconfig)" : [*FixedResponseConfig*](aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig.md),
  "[Order](#cfn-elasticloadbalancingv2-listenerrule-action-order)" : Integer,
  "[RedirectConfig](#cfn-elasticloadbalancingv2-listenerrule-action-redirectconfig)" : [*RedirectConfig*](aws-properties-elasticloadbalancingv2-listenerrule-redirectconfig.md),
  "[TargetGroupArn](#cfn-elasticloadbalancingv2-listenerrule-actions-targetgrouparn)" : String,
  "[Type](#cfn-elasticloadbalancingv2-listenerrule-actions-type)" : String  
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions-syntax.yaml"></a>

```
[AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listenerrule-action-authenticatecognitoconfig): [*AuthenticateCognitoConfig*](aws-properties-elasticloadbalancingv2-listenerrule-authenticatecognitoconfig.md)
[AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listenerrule-action-authenticateoidcconfig): [*AuthenticateOidcConfig*](aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig.md)
[FixedResponseConfig](#cfn-elasticloadbalancingv2-listenerrule-action-fixedresponseconfig): [*FixedResponseConfig*](aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig.md)
[Order](#cfn-elasticloadbalancingv2-listenerrule-action-order): Integer
[RedirectConfig](#cfn-elasticloadbalancingv2-listenerrule-action-redirectconfig): [*RedirectConfig*](aws-properties-elasticloadbalancingv2-listenerrule-redirectconfig.md)
[TargetGroupArn](#cfn-elasticloadbalancingv2-listenerrule-actions-targetgrouparn): String
[Type](#cfn-elasticloadbalancingv2-listenerrule-actions-type): String
```

## Properties<a name="w2922ab1c21c10d120c23c15b7"></a>

`AuthenticateCognitoConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-action-authenticatecognitoconfig"></a>
\[HTTPS listener\] Information for using Amazon Cognito to authenticate users\. Specify only when Type is `authenticate-cognito`\.  
*Required*: No  
*Type*: [AuthenticateCognitoConfig](aws-properties-elasticloadbalancingv2-listenerrule-authenticatecognitoconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthenticateOidcConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-action-authenticateoidcconfig"></a>
\[HTTPS listener\] Information about an identity provider that is compliant with OpenID Connect \(OIDC\)\. Specify only when Type is `authenticate-oidc`\.  
*Required*: No  
*Type*: [AuthenticateOidcConfig](aws-properties-elasticloadbalancingv2-listenerrule-authenticateoidcconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`FixedResponseConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-action-fixedresponseconfig"></a>
\[Application Load Balancer\] Information for creating an action that returns a custom HTTP response\. Specify only when Type is `fixed-response`\.  
*Required*: No  
*Type*: [FixedResponseConfig](aws-properties-elasticloadbalancingv2-listenerrule-fixedresponseconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Order`  <a name="cfn-elasticloadbalancingv2-listenerrule-action-order"></a>
The order for the action\. This value is required for rules with multiple actions\. The action with the lowest value for order is performed first\. The final action to be performed must be a `forward` or a `fixed-response` action\.  
Valid Range: Minimum value of 1\. Maximum value of 50000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RedirectConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-action-redirectconfig"></a>
\[Application Load Balancer\] Information for creating a redirect action\. Specify only when Type is `redirect`\.  
*Required*: No  
*Type*: [RedirectConfig](aws-properties-elasticloadbalancingv2-listenerrule-redirectconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetGroupArn`  <a name="cfn-elasticloadbalancingv2-listenerrule-actions-targetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the target group to which Elastic Load Balancing routes the traffic\. Specify only when `Type` is `forward`\.  
*Required*: No  
*Type*: String

`Type`  <a name="cfn-elasticloadbalancingv2-listenerrule-actions-type"></a>
The type of action\.  
*Valid values*: `forward` \| `authenticate-oidc` \| `authenticate-cognito` \| `redirect` \| `fixed-response`  
*Required*: Yes  
*Type*: String
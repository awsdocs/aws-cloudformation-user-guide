# Elastic Load Balancing V2 Action<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions"></a>

The `Action` property type specifies the default actions that the Elastic Load Balancing listener takes when handling incoming requests\.

The `DefaultActions` property of the [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md) resource contains a list of `Action` property types\.

## Syntax<a name="w13ab1c21c10d138c15c15b7"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-syntax.json"></a>

```
{
  "[AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig)" : [*AuthenticateCognitoConfig*](aws-properties-elasticloadbalancingv2-listener-authenticatecognitoconfig.md),
  "[AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig)" : [*AuthenticateOidcConfig*](aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig.md),
  "[FixedResponseConfig](#cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig)" : [*FixedResponseConfig*](aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig.md),
  "[Order](#cfn-elasticloadbalancingv2-listener-action-order)" : Integer,
  "[RedirectConfig](#cfn-elasticloadbalancingv2-listener-action-redirectconfig)" : [*RedirectConfig*](aws-properties-elasticloadbalancingv2-listener-redirectconfig.md),
  "[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn)" : String,
  "[Type](#cfn-elasticloadbalancingv2-listener-defaultactions-type)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-syntax.yaml"></a>

```
[AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig): [*AuthenticateCognitoConfig*](aws-properties-elasticloadbalancingv2-listener-authenticatecognitoconfig.md)
[AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig): [*AuthenticateOidcConfig*](aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig.md)
[FixedResponseConfig](#cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig): [*FixedResponseConfig*](aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig.md)
[Order](#cfn-elasticloadbalancingv2-listener-action-order): Integer
[RedirectConfig](#cfn-elasticloadbalancingv2-listener-action-redirectconfig): [*RedirectConfig*](aws-properties-elasticloadbalancingv2-listener-redirectconfig.md)
[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn): String
[Type](#cfn-elasticloadbalancingv2-listener-defaultactions-type): String
```

## Properties<a name="w13ab1c21c10d138c15c15b9"></a>

`AuthenticateCognitoConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig"></a>
\[HTTPS listener\] Information for using Amazon Cognito to authenticate users\. Specify only when `Type` is `authenticate-cognito`\.  
*Required*: No  
*Type*: [AuthenticateCognitoConfig](aws-properties-elasticloadbalancingv2-listener-authenticatecognitoconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthenticateOidcConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig"></a>
\[HTTPS listener\] Information about an identity provider that is compliant with OpenID Connect \(OIDC\)\. Specify only when `Type` is `authenticate-oidc`\.  
*Required*: No  
*Type*: [AuthenticateOidcConfig](aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`FixedResponseConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig"></a>
\[Application Load Balancer\] Information for creating an action that returns a custom HTTP response\. Specify only when `Type` is `fixed-response`\.  
*Required*: No  
*Type*: [FixedResponseConfig](aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Order`  <a name="cfn-elasticloadbalancingv2-listener-action-order"></a>
The order for the action\. This value is required for rules with multiple actions\. The action with the lowest value for order is performed first\. The final action to be performed must be a `forward` or a `fixed-response` action\.  
Valid Range: Minimum value of 1\. Maximum value of 50000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RedirectConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-redirectconfig"></a>
\[Application Load Balancer\] Information for creating a redirect action\. Specify only when `Type` is `redirect`\.  
*Required*: No  
*Type*: [RedirectConfig](aws-properties-elasticloadbalancingv2-listener-redirectconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetGroupArn`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the target group to which Elastic Load Balancing routes the traffic\. Specify only when `Type` is `forward`\.  
*Required*: No  
*Type*: String

`Type`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions-type"></a>
The type of action\. Each rule must include exactly one of the following types of actions: `forward`, `fixed-respons`e, or `redirect`\.  
*Valid values*: `forward` \| `authenticate-oidc` \| `authenticate-cognito` \| `redirect` \| `fixed-response`  
*Required*: Yes  
*Type*: String

## See Also<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-seealso"></a>
+ [Action](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_Action.html) in the *Elastic Load Balancing API Reference version 2015\-12\-01*
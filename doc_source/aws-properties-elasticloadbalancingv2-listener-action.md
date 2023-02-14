# AWS::ElasticLoadBalancingV2::Listener Action<a name="aws-properties-elasticloadbalancingv2-listener-action"></a>

Specifies an action for a listener rule\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-action-syntax.json"></a>

```
{
  "[AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig)" : AuthenticateCognitoConfig,
  "[AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig)" : AuthenticateOidcConfig,
  "[FixedResponseConfig](#cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig)" : FixedResponseConfig,
  "[ForwardConfig](#cfn-elasticloadbalancingv2-listener-action-forwardconfig)" : ForwardConfig,
  "[Order](#cfn-elasticloadbalancingv2-listener-action-order)" : Integer,
  "[RedirectConfig](#cfn-elasticloadbalancingv2-listener-action-redirectconfig)" : RedirectConfig,
  "[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-action-targetgrouparn)" : String,
  "[Type](#cfn-elasticloadbalancingv2-listener-action-type)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-action-syntax.yaml"></a>

```
  [AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig): 
    AuthenticateCognitoConfig
  [AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig): 
    AuthenticateOidcConfig
  [FixedResponseConfig](#cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig): 
    FixedResponseConfig
  [ForwardConfig](#cfn-elasticloadbalancingv2-listener-action-forwardconfig): 
    ForwardConfig
  [Order](#cfn-elasticloadbalancingv2-listener-action-order): Integer
  [RedirectConfig](#cfn-elasticloadbalancingv2-listener-action-redirectconfig): 
    RedirectConfig
  [TargetGroupArn](#cfn-elasticloadbalancingv2-listener-action-targetgrouparn): String
  [Type](#cfn-elasticloadbalancingv2-listener-action-type): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-action-properties"></a>

`AuthenticateCognitoConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig"></a>
\[HTTPS listeners\] Information for using Amazon Cognito to authenticate users\. Specify only when `Type` is `authenticate-cognito`\.  
*Required*: No  
*Type*: [AuthenticateCognitoConfig](aws-properties-elasticloadbalancingv2-listener-authenticatecognitoconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthenticateOidcConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig"></a>
\[HTTPS listeners\] Information about an identity provider that is compliant with OpenID Connect \(OIDC\)\. Specify only when `Type` is `authenticate-oidc`\.  
*Required*: No  
*Type*: [AuthenticateOidcConfig](aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FixedResponseConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig"></a>
\[Application Load Balancer\] Information for creating an action that returns a custom HTTP response\. Specify only when `Type` is `fixed-response`\.  
*Required*: No  
*Type*: [FixedResponseConfig](aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-forwardconfig"></a>
Information for creating an action that distributes requests among one or more target groups\. For Network Load Balancers, you can specify a single target group\. Specify only when `Type` is `forward`\. If you specify both `ForwardConfig` and `TargetGroupArn`, you can specify only one target group using `ForwardConfig` and it must be the same target group specified in `TargetGroupArn`\.  
*Required*: No  
*Type*: [ForwardConfig](aws-properties-elasticloadbalancingv2-listener-forwardconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Order`  <a name="cfn-elasticloadbalancingv2-listener-action-order"></a>
The order for the action\. This value is required for rules with multiple actions\. The action with the lowest value for order is performed first\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedirectConfig`  <a name="cfn-elasticloadbalancingv2-listener-action-redirectconfig"></a>
\[Application Load Balancer\] Information for creating a redirect action\. Specify only when `Type` is `redirect`\.  
*Required*: No  
*Type*: [RedirectConfig](aws-properties-elasticloadbalancingv2-listener-redirectconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupArn`  <a name="cfn-elasticloadbalancingv2-listener-action-targetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the target group\. Specify only when `Type` is `forward` and you want to route to a single target group\. To route to one or more target groups, use `ForwardConfig` instead\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-elasticloadbalancingv2-listener-action-type"></a>
The type of action\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `authenticate-cognito | authenticate-oidc | fixed-response | forward | redirect`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
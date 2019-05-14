# AWS::ElasticLoadBalancingV2::Listener Action<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions"></a>

Specifies an action for a listener rule\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-syntax.json"></a>

```
{
  "[AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig)" : [AuthenticateCognitoConfig](aws-properties-elasticloadbalancingv2-listener-authenticatecognitoconfig.md),
  "[AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig)" : [AuthenticateOidcConfig](aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig.md),
  "[FixedResponseConfig](#cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig)" : [FixedResponseConfig](aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig.md),
  "[Order](#cfn-elasticloadbalancingv2-listener-action-order)" : Integer,
  "[RedirectConfig](#cfn-elasticloadbalancingv2-listener-action-redirectconfig)" : [RedirectConfig](aws-properties-elasticloadbalancingv2-listener-redirectconfig.md),
  "[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn)" : String,
  "[Type](#cfn-elasticloadbalancingv2-listener-defaultactions-type)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-syntax.yaml"></a>

```
﻿  [AuthenticateCognitoConfig](#cfn-elasticloadbalancingv2-listener-action-authenticatecognitoconfig) : 
    [AuthenticateCognitoConfig](aws-properties-elasticloadbalancingv2-listener-authenticatecognitoconfig.md)
﻿  [AuthenticateOidcConfig](#cfn-elasticloadbalancingv2-listener-action-authenticateoidcconfig) : 
    [AuthenticateOidcConfig](aws-properties-elasticloadbalancingv2-listener-authenticateoidcconfig.md)
﻿  [FixedResponseConfig](#cfn-elasticloadbalancingv2-listener-action-fixedresponseconfig) : 
    [FixedResponseConfig](aws-properties-elasticloadbalancingv2-listener-fixedresponseconfig.md)
﻿  [Order](#cfn-elasticloadbalancingv2-listener-action-order) : Integer
﻿  [RedirectConfig](#cfn-elasticloadbalancingv2-listener-action-redirectconfig) : 
    [RedirectConfig](aws-properties-elasticloadbalancingv2-listener-redirectconfig.md)
﻿  [TargetGroupArn](#cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn) : String
﻿  [Type](#cfn-elasticloadbalancingv2-listener-defaultactions-type) : String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-properties"></a>

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

`Order`  <a name="cfn-elasticloadbalancingv2-listener-action-order"></a>
The order for the action\. This value is required for rules with multiple actions\. The action with the lowest value for order is performed first\. The final action to be performed must be a `forward` or a `fixed-response` action\.  
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

`TargetGroupArn`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the target group\. Specify only when `Type` is `forward`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions-type"></a>
The type of action\. Each rule must include exactly one of the following types of actions: `forward`, `fixed-response`, or `redirect`\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `authenticate-cognito | authenticate-oidc | fixed-response | forward | redirect`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
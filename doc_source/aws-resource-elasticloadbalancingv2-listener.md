# AWS::ElasticLoadBalancingV2::Listener<a name="aws-resource-elasticloadbalancingv2-listener"></a>

The `AWS::ElasticLoadBalancingV2::Listener` resource creates a listener for an Application Load Balancer or a Network Load Balancer\. The listener checks for connection requests and forwards them to one or more target groups\. For more information, see [Listeners for Your Application Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html) in the *User Guide for Application Load Balancers* or [Listeners for Your Network Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-listeners.html) in the *User Guide for Network Load Balancers*\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-listener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listener-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::Listener",
  "Properties" : {
    "[Certificates](#cfn-elasticloadbalancingv2-listener-certificates)" : [ [Certificate](aws-properties-elasticloadbalancingv2-listener-certificates.md) ],
    "[DefaultActions](#cfn-elasticloadbalancingv2-listener-defaultactions)" : [ [Action](aws-properties-elasticloadbalancingv2-listener-defaultactions.md), ... ],
    "[LoadBalancerArn](#cfn-elasticloadbalancingv2-listener-loadbalancerarn)" : String,
    "[Port](#cfn-elasticloadbalancingv2-listener-port)" : Integer,
    "[Protocol](#cfn-elasticloadbalancingv2-listener-protocol)" : String,
    "[SslPolicy](#cfn-elasticloadbalancingv2-listener-sslpolicy)" : String
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listener-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancingV2::Listener
Properties: 
  [Certificates](#cfn-elasticloadbalancingv2-listener-certificates):
    - [Certificate](aws-properties-elasticloadbalancingv2-listener-certificates.md)
  [DefaultActions](#cfn-elasticloadbalancingv2-listener-defaultactions):
    - [Action](aws-properties-elasticloadbalancingv2-listener-defaultactions.md)
  [LoadBalancerArn](#cfn-elasticloadbalancingv2-listener-loadbalancerarn): String
  [Port](#cfn-elasticloadbalancingv2-listener-port): Integer
  [Protocol](#cfn-elasticloadbalancingv2-listener-protocol): String
  [SslPolicy](#cfn-elasticloadbalancingv2-listener-sslpolicy): String
```

## Properties<a name="w13ab1c21c10d138c15b7"></a>

`Certificates`  <a name="cfn-elasticloadbalancingv2-listener-certificates"></a>
\[HTTPS and TLS listeners\] The default SSL server certificate for the listener\.  
*Required*: Conditional\. If you specify `HTTPS` or `TLS` for the `Protocol` property, you must specify exactly one certificate\.  
*Type*: List of [Elastic Load Balancing V2 Certificate](aws-properties-elasticloadbalancingv2-listener-certificates.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DefaultActions`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions"></a>
The actions for the default rule for the listener\.  
*Required*: Yes  
*Type*: List of [Elastic Load Balancing V2 Action](aws-properties-elasticloadbalancingv2-listener-defaultactions.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LoadBalancerArn`  <a name="cfn-elasticloadbalancingv2-listener-loadbalancerarn"></a>
The Amazon Resource Name \(ARN\) of the load balancer\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Port`  <a name="cfn-elasticloadbalancingv2-listener-port"></a>
The port on which the listener listens for requests\.  
For valid values, see the `Port` parameter for the [CreateListener](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateListener.html) action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Protocol`  <a name="cfn-elasticloadbalancingv2-listener-protocol"></a>
The protocol that clients must use to send requests to the listener\.  
For valid values, see the `Protocol` parameter for the [CreateListener](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateListener.html) action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SslPolicy`  <a name="cfn-elasticloadbalancingv2-listener-sslpolicy"></a>
\[HTTPS and TLS listeners\] The security policy that defines the ciphers and protocols that the listener supports\. The default is the current predefined security policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w13ab1c21c10d138c15b9"></a>

### Ref<a name="w13ab1c21c10d138c15b9b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the listener's ARN, such as `arn:aws:elasticloadbalancing:us-west-2:123456789012:listener/app/my-load-balancer/50dc6c495c0c9188/f2f7dc8efc522ab2`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w13ab1c21c10d138c15c11"></a>

The following example creates a listener for the `myLoadBalancer` resource\. The listener's default action is to forward requests to the `myTargetGroup` target group\.

### JSON<a name="aws-resource-elasticloadbalancingv2-listener-example.json"></a>

```
"Listener": {
  "Type": "AWS::ElasticLoadBalancingV2::Listener",
  "Properties": {
    "DefaultActions": [{
      "Type": "forward",
      "TargetGroupArn": { "Ref": "myTargetGroup" }
    }],
    "LoadBalancerArn": { "Ref": "myLoadBalancer" },
    "Port": "8000",
    "Protocol": "HTTP"
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listener-example.yaml"></a>

```
Listener:
  Type: AWS::ElasticLoadBalancingV2::Listener
  Properties:
    DefaultActions:
    - Type: forward
      TargetGroupArn:
        Ref: myTargetGroup
    LoadBalancerArn:
      Ref: myLoadBalancer
    Port: '8000'
    Protocol: HTTP
```
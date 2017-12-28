# AWS::ElasticLoadBalancingV2::Listener<a name="aws-resource-elasticloadbalancingv2-listener"></a>

The `AWS::ElasticLoadBalancingV2::Listener` resource creates a listener for an Elastic Load Balancing Application or Network load balancer\. The listener checks for connection requests and forwards them to one or more target groups\. For more information, see [Getting Started](http://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/load-balancer-getting-started.html) in the *Elastic Load Balancing User Guide*\.


+ [Syntax](#aws-resource-elasticloadbalancingv2-listener-syntax)
+ [Properties](#w3ab2c21c10d591b9)
+ [Return Value](#w3ab2c21c10d591c11)
+ [Example](#w3ab2c21c10d591c13)

## Syntax<a name="aws-resource-elasticloadbalancingv2-listener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listener-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::Listener",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-certificates)" : [ Certificate ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-defaultactions)" : [ Action, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-loadbalancerarn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-port)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-protocol)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-sslpolicy)" : String
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listener-syntax.yaml"></a>

```
Type: "AWS::ElasticLoadBalancingV2::Listener"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-certificates):
    - Certificate
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-defaultactions):
    - Action
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-loadbalancerarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-port): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-protocol): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-sslpolicy): String
```

## Properties<a name="w3ab2c21c10d591b9"></a>

`Certificates`  
The SSL server certificate for the listener\. With a certificate, you can encrypt traffic between the load balancer and the clients that initiate HTTPS sessions, and traffic between the load balancer and your targets\.  
This property represents the default certificate for the listener\. You can specify only one certificate for the `AWS::ElasticLoadBalancingV2::Listener` resource\.  
*Required: *Conditional\. If you specify `HTTPS` for the `Protocol` property, specify a certificate\.  
*Type*: List of [Elastic Load Balancing Listener Certificate](aws-properties-elasticloadbalancingv2-listener-certificates.md)  
*Update requires*: No interruption

`DefaultActions`  
The default actions that the listener takes when handling incoming requests\.  
*Required: *Yes  
*Type*: List of [Elastic Load Balancing Listener Action](aws-properties-elasticloadbalancingv2-listener-defaultactions.md)  
*Update requires*: No interruption

`LoadBalancerArn`  
The Amazon Resource Name \(ARN\) of the load balancer to associate with the listener\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Port`  
The port on which the listener listens for requests\.  
For valid values, see the `Port` parameter for the [CreateListener](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateListener.html) action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *Yes  
*Type*: Integer  
*Update requires*: No interruption

`Protocol`  
The protocol that clients must use to send requests to the listener\.  
For valid values, see the `Protocol` parameter for the [CreateListener](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateListener.html) action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`SslPolicy`  
The security policy that defines the ciphers and protocols that the load balancer supports\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10d591c11"></a>

### Ref<a name="w3ab2c21c10d591c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the listener's ARN, such as `arn:aws:elasticloadbalancing:us-west-2:123456789012:listener/app/my-load-balancer/50dc6c495c0c9188/f2f7dc8efc522ab2`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d591c13"></a>

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
# AWS::ElasticLoadBalancingV2::Listener<a name="aws-resource-elasticloadbalancingv2-listener"></a>

Specifies a listener for an Application Load Balancer or Network Load Balancer\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-listener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listener-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::Listener",
  "Properties" : {
      "[Certificates](#cfn-elasticloadbalancingv2-listener-certificates)" : [ [Certificate](aws-properties-elasticloadbalancingv2-listener-certificates-1.md), ... ],
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
    - [Certificate](aws-properties-elasticloadbalancingv2-listener-certificates-1.md)
  [DefaultActions](#cfn-elasticloadbalancingv2-listener-defaultactions): 
    - [Action](aws-properties-elasticloadbalancingv2-listener-defaultactions.md)
  [LoadBalancerArn](#cfn-elasticloadbalancingv2-listener-loadbalancerarn): String
  [Port](#cfn-elasticloadbalancingv2-listener-port): Integer
  [Protocol](#cfn-elasticloadbalancingv2-listener-protocol): String
  [SslPolicy](#cfn-elasticloadbalancingv2-listener-sslpolicy): String
```

## Properties<a name="aws-resource-elasticloadbalancingv2-listener-properties"></a>

`Certificates`  <a name="cfn-elasticloadbalancingv2-listener-certificates"></a>
The default SSL server certificate\. You must provide exactly one certificate if the listener protocol is HTTPS or TLS\.  
*Required*: Conditional  
*Type*: List of [Certificate](aws-properties-elasticloadbalancingv2-listener-certificates-1.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultActions`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions"></a>
The actions for the default rule\.  
*Required*: Yes  
*Type*: List of [Action](aws-properties-elasticloadbalancingv2-listener-defaultactions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerArn`  <a name="cfn-elasticloadbalancingv2-listener-loadbalancerarn"></a>
The Amazon Resource Name \(ARN\) of the load balancer\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-elasticloadbalancingv2-listener-port"></a>
The port on which the load balancer is listening\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-elasticloadbalancingv2-listener-protocol"></a>
The protocol for connections from clients to the load balancer\. For Application Load Balancers, the supported protocols are HTTP and HTTPS\. For Network Load Balancers, the supported protocols are TCP and TLS\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `HTTP | HTTPS | TCP | TLS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslPolicy`  <a name="cfn-elasticloadbalancingv2-listener-sslpolicy"></a>
\[HTTPS and TLS listeners\] The security policy that defines which ciphers and protocols are supported\. The default is the current predefined security policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-elasticloadbalancingv2-listener-return-values"></a>

### Ref<a name="aws-resource-elasticloadbalancingv2-listener-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the listener\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-elasticloadbalancingv2-listener--examples"></a>

The following example creates a listener with a default action that redirects HTTP requests on port 80 to HTTPS requests on port 443, retaining the original host name, path, and query string\.

### <a name="aws-resource-elasticloadbalancingv2-listener--examples--"></a>

#### YAML<a name="aws-resource-elasticloadbalancingv2-listener--examples----yaml"></a>

```
HTTPlistener:
   Type: "AWS::ElasticLoadBalancingV2::Listener"
   Properties:
     DefaultActions:
       - Type: "redirect"
         RedirectConfig:
           Protocol: "HTTPS"
           Port: "443"
           Host: "#{host}"
           Path: "/#{path}"
           Query: "#{query}"
           StatusCode: "HTTP_301"
     LoadBalancerArn: !Ref myLoadBalancer
     Port: 80
     Protocol: "HTTP"
```

#### JSON<a name="aws-resource-elasticloadbalancingv2-listener--examples----json"></a>

```
"HTTPlistener": {
    "Type": "AWS::ElasticLoadBalancingV2::Listener",
    "Properties": {
        "DefaultActions": [
            {
                "Type": "redirect",
                "RedirectConfig": {
                    "Protocol": "HTTPS",
                    "Port": "443",
                    "Host": "#{host}",
                    "Path": "/#{path}",
                    "Query": "#{query}",
                    "StatusCode": "HTTP_301"
                }
            }
        ],
        "LoadBalancerArn": {
            "Ref": "myLoadBalancer"
        },
        "Port": 80,
        "Protocol": "HTTP"
    }
}
```

## See Also<a name="aws-resource-elasticloadbalancingv2-listener--seealso"></a>
+  [CreateListener](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateListener.html) in the *Elastic Load Balancing API Reference \(version 2015\-12\-01\)* 
+  [Listeners](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html) in the *User Guide for Application Load Balancers* 
+  [Listeners](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-listeners.html) in the *User Guide for Network Load Balancers* 
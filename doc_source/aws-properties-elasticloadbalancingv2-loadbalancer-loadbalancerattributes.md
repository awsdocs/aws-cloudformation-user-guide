# Elastic Load Balancing LoadBalancer LoadBalancerAttributes<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes"></a>

`LoadBalancerAttributes` is a property of the [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md) resource that configures settings for an Elastic Load Balancing Application load balancer\. For more information, see [Load Balancer Attributes](http://docs.aws.amazon.com/elasticloadbalancing/latest/application/application-load-balancers.html#load-balancer-attributes) in the *Application Load Balancers Guide*\.

## Syntax<a name="w3ab2c21c14d833b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-key)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-value)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-key): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-value): String
```

## Properties<a name="w3ab2c21c14d833b7"></a>

`Key`  
The name of an attribute that you want to configure\. For the list of attributes that you can configure, see the `Key` contents for the [LoadBalancerAttribute](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_LoadBalancerAttribute.html) data type in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *No  
*Type*: String

`Value`  
A value for the attribute\.  
*Required: *No  
*Type*: String
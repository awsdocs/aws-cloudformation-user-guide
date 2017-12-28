# Elastic Load Balancing LoadBalancer SubnetMapping<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping"></a>

<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-description"></a>The `SubnetMapping` property type specifies the ID of a subnet to attach to an Elastic Load Balancing Application or Network Load Balancer\.

<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-inheritance"></a> `SubnetMappings` is a property of the [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md) resource\. 

## Syntax<a name="w3ab2c21c14d837b7"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-subnetid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-allocationid)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-subnetid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-allocationid): String
```

## Properties<a name="w3ab2c21c14d837b9"></a>

`SubnetId`  
The ID of the subnet\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`AllocationId`  
\[Network Load Balancer\] The ID that represents the allocation of the Elastic IP address\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption
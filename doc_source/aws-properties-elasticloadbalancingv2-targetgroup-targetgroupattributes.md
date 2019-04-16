# Elastic Load Balancing V2 TargetGroupAttributes<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattributes"></a>

`TargetGroupAttributes` is a property of the [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md) resource that configures settings for a target group\. For more information, see [Target Group Attributes](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html#target-group-attributes) in the *User Guide for Application Load Balancers* or [Target Group Attributes](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-target-groups.html#target-group-attributes) in the *User Guide for Network Load Balancers*\.

## Syntax<a name="w13ab1c21c10d138c31c23b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattributes-syntax.json"></a>

```
{
  "[Key](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-key)" : String,
  "[Value](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-value)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattributes-syntax.yaml"></a>

```
[Key](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-key): String
[Value](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-value): String
```

## Properties<a name="w13ab1c21c10d138c31c23b7"></a>

`Key`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-key"></a>
The name of the attribute to configure\. For the list of attributes, see the description of `Key` for the [TargetGroupAttribute](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_TargetGroupAttribute.html) data type in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-value"></a>
A value for the attribute\.  
*Required*: No  
*Type*: String
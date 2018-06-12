# Elastic Load Balancing TargetGroup TargetGroupAttributes<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattributes"></a>

`TargetGroupAttributes` is a property of the [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md) resource that configures settings for an Elastic Load Balancing target group\. For more information, see [Target Group Attributes](http://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html#target-group) in the *Application Load Balancers Guide*\.

## Syntax<a name="w3ab2c21c14e1036b5"></a>

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

## Properties<a name="w3ab2c21c14e1036b7"></a>

`Key`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-key"></a>
The name of the attribute that you want to configure\. For the list of attributes that you can configure, see the `Key` contents for the [TargetGroupAttribute](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_TargetGroupAttribute.html) data type in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes-value"></a>
A value for the attribute\.  
*Required*: No  
*Type*: String
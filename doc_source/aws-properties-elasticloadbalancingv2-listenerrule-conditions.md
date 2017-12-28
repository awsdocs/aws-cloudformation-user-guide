# Elastic Load Balancing ListenerRule Conditions<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions"></a>

`Conditions` is a property of the [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md) resource that specifies the conditions when an Elastic Load Balancing listener rule takes effect\.

## Syntax<a name="w3ab2c21c14d829b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listenerrule-conditions-field)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listenerrule-conditions-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listenerrule-conditions-field): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listenerrule-conditions-values):
  - String
```

## Properties<a name="w3ab2c21c14d829b7"></a>

`Field`  
The name of the condition that you want to define, such as `path-pattern` \(which forwards requests based on the URL of the request\)\.  
For valid values, see the `Field` contents for the [RuleCondition](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_RuleCondition.html) data type in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *No  
*Type*: String

`Values`  
The value for the field that you specified in the `Field` property\.  
*Required: *No  
*Type*: List of String values
# Elastic Load Balancing V2 Conditions<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions"></a>

`Conditions` is a property of the [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md) resource that specifies the conditions when an Elastic Load Balancing listener rule takes effect\.

For more information, see [RuleCondition](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_RuleCondition.html) in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.

## Syntax<a name="w2922ab1c21c10d120c23c27b7"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.json"></a>

```
{
  "[Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field)" : String,
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-conditions-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.yaml"></a>

```
[Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field): String
[Values](#cfn-elasticloadbalancingv2-listenerrule-conditions-values):
  - String
```

## Properties<a name="w2922ab1c21c10d120c23c27b9"></a>

`Field`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions-field"></a>
The name of the condition that you want to define, such as `path-pattern` \(which forwards requests based on the URL of the request\)\.  
*Valid values*: `host-header` \| `path-pattern`  
*Length constraints*: Maximum length of 64  
*Required*: No  
*Type*: String

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions-values"></a>
The value for the field that you specified in the `Field` property\.  
If you specified `host-header` for `Field`, you can specify a single host name \(for example, my\.example\.com\)\. A host name is case insensitive, can be up to 128 characters in length, and can contain any of the following characters\. You can include up to three wildcard characters\.  
+ A\-Z, a\-z, 0\-9
+ \- \.
+ \* \(matches 0 or more characters\)
+ ? \(matches exactly 1 character\)
If you specified `path-pattern` for `Field`, you can specify a single path pattern \(for example, /img/\*\)\. A path pattern is case\-sensitive, can be up to 128 characters in length, and can contain any of the following characters\. You can include up to three wildcard characters\.  
+ A\-Z, a\-z, 0\-9
+ \_ \- \. $ / \~ " ' @ : \+
+ & \(using &amp;\)
+ \* \(matches 0 or more characters\)
+ ? \(matches exactly 1 character\)
*Required*: No  
*Type*: List of String values
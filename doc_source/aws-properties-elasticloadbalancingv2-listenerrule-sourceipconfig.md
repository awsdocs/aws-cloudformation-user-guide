# AWS::ElasticLoadBalancingV2::ListenerRule SourceIpConfig<a name="aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig"></a>

Information about a source IP condition\.

You can use this condition to route based on the IP address of the source that connects to the load balancer\. If a client is behind a proxy, this is the IP address of the proxy not the IP address of the client\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig-syntax.json"></a>

```
{
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-sourceipconfig-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig-syntax.yaml"></a>

```
  [Values](#cfn-elasticloadbalancingv2-listenerrule-sourceipconfig-values): 
    - String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig-properties"></a>

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-sourceipconfig-values"></a>
One or more source IP addresses, in CIDR format\. You can use both IPv4 and IPv6 addresses\. Wildcards are not supported\.  
If you specify multiple addresses, the condition is satisfied if the source IP address of the request matches one of the CIDR blocks\. This condition is not satisfied by the addresses in the X\-Forwarded\-For header\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
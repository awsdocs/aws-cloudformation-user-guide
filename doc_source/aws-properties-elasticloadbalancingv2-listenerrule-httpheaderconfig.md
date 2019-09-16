# AWS::ElasticLoadBalancingV2::ListenerRule HttpHeaderConfig<a name="aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig"></a>

Information about an HTTP header condition\.

There is a set of standard HTTP header fields\. You can also define custom HTTP header fields\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig-syntax.json"></a>

```
{
  "[HttpHeaderName](#cfn-elasticloadbalancingv2-listenerrule-httpheaderconfig-httpheadername)" : String,
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-httpheaderconfig-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig-syntax.yaml"></a>

```
  [HttpHeaderName](#cfn-elasticloadbalancingv2-listenerrule-httpheaderconfig-httpheadername): String
  [Values](#cfn-elasticloadbalancingv2-listenerrule-httpheaderconfig-values): 
    - String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig-properties"></a>

`HttpHeaderName`  <a name="cfn-elasticloadbalancingv2-listenerrule-httpheaderconfig-httpheadername"></a>
The name of the HTTP header field\. The maximum size is 40 characters\. The header name is case insensitive\. The allowed characters are specified by RFC 7230\. Wildcards are not supported\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-httpheaderconfig-values"></a>
One or more strings to compare against the value of the HTTP header\. The maximum size of each string is 128 characters\. The comparison strings are case insensitive\. The following wildcard characters are supported: \* \(matches 0 or more characters\) and ? \(matches exactly 1 character\)\.  
If the same header appears multiple times in the request, we search them in order until a match is found\.  
If you specify multiple strings, the condition is satisfied if one of the strings matches the value of the HTTP header\. To require that all of the strings are a match, create one condition per string\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
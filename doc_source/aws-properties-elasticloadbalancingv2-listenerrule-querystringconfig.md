# AWS::ElasticLoadBalancingV2::ListenerRule QueryStringConfig<a name="aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig"></a>

Information about a query string condition\.

The query string component of a URI starts after the first '?' character and is terminated by either a '\#' character or the end of the URI\. A typical query string contains key/value pairs separated by '&' characters\. The allowed characters are specified by RFC 3986\. Any character can be percentage encoded\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig-syntax.json"></a>

```
{
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-querystringconfig-values)" : [ QueryStringKeyValue, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig-syntax.yaml"></a>

```
  [Values](#cfn-elasticloadbalancingv2-listenerrule-querystringconfig-values): 
    - QueryStringKeyValue
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig-properties"></a>

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-querystringconfig-values"></a>
One or more key/value pairs or values to find in the query string\. The maximum size of each string is 128 characters\. The comparison is case insensitive\. The following wildcard characters are supported: \* \(matches 0 or more characters\) and ? \(matches exactly 1 character\)\. To search for a literal '\*' or '?' character in a query string, you must escape these characters in `Values` using a '\\' character\.  
If you specify multiple key/value pairs or values, the condition is satisfied if one of them is found in the query string\.  
*Required*: No  
*Type*: List of [QueryStringKeyValue](aws-properties-elasticloadbalancingv2-listenerrule-querystringkeyvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
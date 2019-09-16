# AWS::ElasticLoadBalancingV2::ListenerRule PathPatternConfig<a name="aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig"></a>

Information about a path pattern condition\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig-syntax.json"></a>

```
{
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-pathpatternconfig-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig-syntax.yaml"></a>

```
  [Values](#cfn-elasticloadbalancingv2-listenerrule-pathpatternconfig-values): 
    - String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig-properties"></a>

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-pathpatternconfig-values"></a>
One or more path patterns to compare against the request URL\. The maximum size of each string is 128 characters\. The comparison is case sensitive\. The following wildcard characters are supported: \* \(matches 0 or more characters\) and ? \(matches exactly 1 character\)\.  
If you specify multiple strings, the condition is satisfied if one of them matches the request URL\. The path pattern is compared only to the path of the URL, not to its query string\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
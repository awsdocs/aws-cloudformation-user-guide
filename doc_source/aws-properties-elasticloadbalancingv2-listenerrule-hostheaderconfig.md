# AWS::ElasticLoadBalancingV2::ListenerRule HostHeaderConfig<a name="aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig"></a>

Information about a host header condition\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig-syntax.json"></a>

```
{
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-hostheaderconfig-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig-syntax.yaml"></a>

```
  [Values](#cfn-elasticloadbalancingv2-listenerrule-hostheaderconfig-values): 
    - String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig-properties"></a>

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-hostheaderconfig-values"></a>
One or more host names\. The maximum size of each name is 128 characters\. The comparison is case insensitive\. The following wildcard characters are supported: \* \(matches 0 or more characters\) and ? \(matches exactly 1 character\)\.  
If you specify multiple strings, the condition is satisfied if one of the strings matches the host name\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
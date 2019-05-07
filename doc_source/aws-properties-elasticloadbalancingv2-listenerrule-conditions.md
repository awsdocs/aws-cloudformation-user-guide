# AWS::ElasticLoadBalancingV2::ListenerRule RuleCondition<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions"></a>

Specifies a condition for a listener rule\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.json"></a>

```
{
  "[Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field)" : String,
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-conditions-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.yaml"></a>

```
﻿  [Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field) : String
﻿  [Values](#cfn-elasticloadbalancingv2-listenerrule-conditions-values) : 
    - String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-properties"></a>

`Field`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions-field"></a>
The field in the HTTP request\. The following are the possible values:  
+  `http-header` 
+  `http-request-method` 
+  `host-header` 
+  `path-pattern` 
+  `query-string` 
+  `source-ip` 
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions-values"></a>
The condition value\. You can use `Values` if the rule contains only `host-header` and `path-pattern` conditions\. Otherwise, you can use `HostHeaderConfig` for `host-header` conditions and `PathPatternConfig` for `path-pattern` conditions\.  
If `Field` is `host-header`, you can specify a single host name \(for example, my\.example\.com\)\. A host name is case insensitive, can be up to 128 characters in length, and can contain any of the following characters\.  
+ A\-Z, a\-z, 0\-9
+ \- \.
+ \* \(matches 0 or more characters\)
+ ? \(matches exactly 1 character\)
If `Field` is `path-pattern`, you can specify a single path pattern \(for example, /img/\*\)\. A path pattern is case\-sensitive, can be up to 128 characters in length, and can contain any of the following characters\.  
+ A\-Z, a\-z, 0\-9
+ \_ \- \. $ / \~ " ' @ : \+
+ & \(using &amp;\)
+ \* \(matches 0 or more characters\)
+ ? \(matches exactly 1 character\)
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
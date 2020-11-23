# AWS::ElasticLoadBalancingV2::ListenerRule RuleCondition<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions"></a>

Specifies a condition for a listener rule\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.json"></a>

```
{
  "[Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field)" : String,
  "[HostHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-hostheaderconfig)" : HostHeaderConfig,
  "[HttpHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httpheaderconfig)" : HttpHeaderConfig,
  "[HttpRequestMethodConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httprequestmethodconfig)" : HttpRequestMethodConfig,
  "[PathPatternConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-pathpatternconfig)" : PathPatternConfig,
  "[QueryStringConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-querystringconfig)" : QueryStringConfig,
  "[SourceIpConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-sourceipconfig)" : SourceIpConfig,
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-conditions-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.yaml"></a>

```
  [Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field): String
  [HostHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-hostheaderconfig): 
    HostHeaderConfig
  [HttpHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httpheaderconfig): 
    HttpHeaderConfig
  [HttpRequestMethodConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httprequestmethodconfig): 
    HttpRequestMethodConfig
  [PathPatternConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-pathpatternconfig): 
    PathPatternConfig
  [QueryStringConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-querystringconfig): 
    QueryStringConfig
  [SourceIpConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-sourceipconfig): 
    SourceIpConfig
  [Values](#cfn-elasticloadbalancingv2-listenerrule-conditions-values): 
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

`HostHeaderConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-hostheaderconfig"></a>
Information for a host header condition\. Specify only when `Field` is `host-header`\.  
*Required*: No  
*Type*: [HostHeaderConfig](aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpHeaderConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-httpheaderconfig"></a>
Information for an HTTP header condition\. Specify only when `Field` is `http-header`\.  
*Required*: Conditional  
*Type*: [HttpHeaderConfig](aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpRequestMethodConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-httprequestmethodconfig"></a>
Information for an HTTP method condition\. Specify only when `Field` is `http-request-method`\.  
*Required*: Conditional  
*Type*: [HttpRequestMethodConfig](aws-properties-elasticloadbalancingv2-listenerrule-httprequestmethodconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PathPatternConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-pathpatternconfig"></a>
Information for a path pattern condition\. Specify only when `Field` is `path-pattern`\.  
*Required*: No  
*Type*: [PathPatternConfig](aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-querystringconfig"></a>
Information for a query string condition\. Specify only when `Field` is `query-string`\.  
*Required*: Conditional  
*Type*: [QueryStringConfig](aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceIpConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-sourceipconfig"></a>
Information for a source IP condition\. Specify only when `Field` is `source-ip`\.  
*Required*: Conditional  
*Type*: [SourceIpConfig](aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions-values"></a>
The condition value\. Specify only when `Field` is `host-header` or `path-pattern`\. Alternatively, to specify multiple host names or multiple path patterns, use `HostHeaderConfig` or `PathPatternConfig`\.  
If `Field` is `host-header` and you're not using `HostHeaderConfig`, you can specify a single host name \(for example, my\.example\.com\)\. A host name is case insensitive, can be up to 128 characters in length, and can contain any of the following characters\.  
+ A\-Z, a\-z, 0\-9
+ \- \.
+ \* \(matches 0 or more characters\)
+ ? \(matches exactly 1 character\)
If `Field` is `path-pattern` and you're not using `PathPatternConfig`, you can specify a single path pattern \(for example, /img/\*\)\. A path pattern is case\-sensitive, can be up to 128 characters in length, and can contain any of the following characters\.  
+ A\-Z, a\-z, 0\-9
+ \_ \- \. $ / \~ " ' @ : \+
+ & \(using &amp;\)
+ \* \(matches 0 or more characters\)
+ ? \(matches exactly 1 character\)
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
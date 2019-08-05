# AWS::ElasticLoadBalancingV2::ListenerRule RuleCondition<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions"></a>

Specifies a condition for a listener rule\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.json"></a>

```
{
  "[Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field)" : String,
  "[HostHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-hostheaderconfig)" : [HostHeaderConfig](aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig.md),
  "[HttpHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httpheaderconfig)" : [HttpHeaderConfig](aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig.md),
  "[HttpRequestMethodConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httprequestmethodconfig)" : [HttpRequestMethodConfig](aws-properties-elasticloadbalancingv2-listenerrule-httprequestmethodconfig.md),
  "[PathPatternConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-pathpatternconfig)" : [PathPatternConfig](aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig.md),
  "[QueryStringConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-querystringconfig)" : [QueryStringConfig](aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig.md),
  "[SourceIpConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-sourceipconfig)" : [SourceIpConfig](aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig.md),
  "[Values](#cfn-elasticloadbalancingv2-listenerrule-conditions-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-conditions-syntax.yaml"></a>

```
  [Field](#cfn-elasticloadbalancingv2-listenerrule-conditions-field): String
  [HostHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-hostheaderconfig):
    [HostHeaderConfig](aws-properties-elasticloadbalancingv2-listenerrule-hostheaderconfig.md)
  [HttpHeaderConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httpheaderconfig):
    [HttpHeaderConfig](aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig.md)
  [HttpRequestMethodConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-httprequestmethodconfig):
    [HttpRequestMethodConfig](aws-properties-elasticloadbalancingv2-listenerrule-httprequestmethodconfig.md)
  [PathPatternConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-pathpatternconfig):
    [PathPatternConfig](aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig.md)
  [QueryStringConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-querystringconfig):
    [QueryStringConfig](aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig.md)
  [SourceIpConfig](#cfn-elasticloadbalancingv2-listenerrule-rulecondition-sourceipconfig):
    [SourceIpConfig](aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig.md)
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
*Required*: No
*Type*: [HttpHeaderConfig](aws-properties-elasticloadbalancingv2-listenerrule-httpheaderconfig.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpRequestMethodConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-httprequestmethodconfig"></a>
Information for an HTTP method condition\. Specify only when `Field` is `http-request-method`\.
*Required*: No
*Type*: [HttpRequestMethodConfig](aws-properties-elasticloadbalancingv2-listenerrule-httprequestmethodconfig.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PathPatternConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-pathpatternconfig"></a>
Information for a path pattern condition\. Specify only when `Field` is `path-pattern`\.
Conditional: Required if `HttpHeaderConfig` is used\.
*Required*: No
*Type*: [PathPatternConfig](aws-properties-elasticloadbalancingv2-listenerrule-pathpatternconfig.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-querystringconfig"></a>
Information for a query string condition\. Specify only when `Field` is `query-string`\.
Conditional: Required if `HttpHeaderConfig` is used\.
*Required*: No
*Type*: [QueryStringConfig](aws-properties-elasticloadbalancingv2-listenerrule-querystringconfig.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceIpConfig`  <a name="cfn-elasticloadbalancingv2-listenerrule-rulecondition-sourceipconfig"></a>
Information for a source IP condition\. Specify only when `Field` is `source-ip`\.
Conditional: Required if `HttpHeaderConfig` is used\.
*Required*: No
*Type*: [SourceIpConfig](aws-properties-elasticloadbalancingv2-listenerrule-sourceipconfig.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions-values"></a>
The condition value\.
You can only use `Values` if the condition type is `host-header` and `path-pattern`\. You can not specify both `Values` and `HostHeaderConfig` at the same time\.
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

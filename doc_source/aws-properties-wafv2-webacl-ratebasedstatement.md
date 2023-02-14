# AWS::WAFv2::WebACL RateBasedStatement<a name="aws-properties-wafv2-webacl-ratebasedstatement"></a>

A rate\-based rule tracks the rate of requests for each originating IP address, and triggers the rule action when the rate exceeds a limit that you specify on the number of requests in any 5\-minute time span\. You can use this to put a temporary block on requests from an IP address that is sending excessive requests\.

When the rule action triggers, AWS WAF blocks additional requests from the IP address until the request rate falls below the limit\.

You can optionally nest another statement inside the rate\-based statement, to narrow the scope of the rule so that it only counts requests that match the nested statement\. For example, based on recent requests that you have seen from an attacker, you might create a rate\-based rule with a nested AND rule statement that contains the following nested statements:
+ An IP match statement with an IP set that specified the address 192\.0\.2\.44\.
+ A string match statement that searches in the User\-Agent header for the string BadBot\.

In this rate\-based rule, you also define a rate limit\. For this example, the rate limit is 1,000\. Requests that meet both of the conditions in the statements are counted\. If the count exceeds 1,000 requests per five minutes, the rule action triggers\. Requests that do not meet both conditions are not counted towards the rate limit and are not affected by this rule\.

You cannot nest a `RateBasedStatement`, for example for use inside a `NotStatement` or `OrStatement`\. It can only be referenced as a top\-level statement within a rule\.

## Syntax<a name="aws-properties-wafv2-webacl-ratebasedstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatement-syntax.json"></a>

```
{
  "[AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatement-aggregatekeytype)" : String,
  "[ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatement-forwardedipconfig)" : ForwardedIPConfiguration,
  "[Limit](#cfn-wafv2-webacl-ratebasedstatement-limit)" : Integer,
  "[ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatement-scopedownstatement)" : Statement
}
```

### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatement-syntax.yaml"></a>

```
  [AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatement-aggregatekeytype): String
  [ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatement-forwardedipconfig): 
    ForwardedIPConfiguration
  [Limit](#cfn-wafv2-webacl-ratebasedstatement-limit): Integer
  [ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatement-scopedownstatement): 
    Statement
```

## Properties<a name="aws-properties-wafv2-webacl-ratebasedstatement-properties"></a>

`AggregateKeyType`  <a name="cfn-wafv2-webacl-ratebasedstatement-aggregatekeytype"></a>
Setting that indicates how to aggregate the request counts\. The options are the following:  
+ IP \- Aggregate the request counts on the IP address from the web request origin\.
+ FORWARDED\_IP \- Aggregate the request counts on the first IP address in an HTTP header\. If you use this, configure the `ForwardedIPConfig`, to specify the header to use\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `FORWARDED_IP | IP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedIPConfig`  <a name="cfn-wafv2-webacl-ratebasedstatement-forwardedipconfig"></a>
The configuration for inspecting IP addresses in an HTTP header that you specify, instead of using the IP address that's reported by the web request origin\. Commonly, this is the X\-Forwarded\-For \(XFF\) header, but you can specify any header name\.   
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
This is required if `AggregateKeyType` is set to `FORWARDED_IP`\.  
*Required*: No  
*Type*: [ForwardedIPConfiguration](aws-properties-wafv2-webacl-forwardedipconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limit`  <a name="cfn-wafv2-webacl-ratebasedstatement-limit"></a>
The limit on requests per 5\-minute period for a single originating IP address\. If the statement includes a `ScopeDownStatement`, this limit is applied only to the requests that match the statement\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScopeDownStatement`  <a name="cfn-wafv2-webacl-ratebasedstatement-scopedownstatement"></a>
An optional nested statement that narrows the scope of the rate\-based statement to matching web requests\. This can be any nestable statement, and you can nest statements at any level below this scope\-down statement\.  
*Required*: No  
*Type*: [Statement](aws-properties-wafv2-webacl-statement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
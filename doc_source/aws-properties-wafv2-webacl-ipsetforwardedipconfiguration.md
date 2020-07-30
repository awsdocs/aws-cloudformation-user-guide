# AWS::WAFv2::WebACL IPSetForwardedIPConfiguration<a name="aws-properties-wafv2-webacl-ipsetforwardedipconfiguration"></a>

The configuration for inspecting IP addresses in an HTTP header that you specify, instead of using the IP address that's reported by the web request origin\. Commonly, this is the X\-Forwarded\-For \(XFF\) header, but you can specify any header name\. 

**Note**  
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.

This configuration is used only for `IPSetReferenceStatement`\. For `GeoMatchStatement` and `RateBasedStatement`, use `ForwardedIPConfig` instead\. 

## Syntax<a name="aws-properties-wafv2-webacl-ipsetforwardedipconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ipsetforwardedipconfiguration-syntax.json"></a>

```
{
  "[FallbackBehavior](#cfn-wafv2-webacl-ipsetforwardedipconfiguration-fallbackbehavior)" : String,
  "[HeaderName](#cfn-wafv2-webacl-ipsetforwardedipconfiguration-headername)" : String,
  "[Position](#cfn-wafv2-webacl-ipsetforwardedipconfiguration-position)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-ipsetforwardedipconfiguration-syntax.yaml"></a>

```
  [FallbackBehavior](#cfn-wafv2-webacl-ipsetforwardedipconfiguration-fallbackbehavior): String
  [HeaderName](#cfn-wafv2-webacl-ipsetforwardedipconfiguration-headername): String
  [Position](#cfn-wafv2-webacl-ipsetforwardedipconfiguration-position): String
```

## Properties<a name="aws-properties-wafv2-webacl-ipsetforwardedipconfiguration-properties"></a>

`FallbackBehavior`  <a name="cfn-wafv2-webacl-ipsetforwardedipconfiguration-fallbackbehavior"></a>
The match status to assign to the web request if the request doesn't have a valid IP address in the specified position\.  
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
You can specify the following fallback behaviors:  
+ MATCH \- Treat the web request as matching the rule statement\. AWS WAF applies the rule action to the request\.
+ NO\_MATCH \- Treat the web request as not matching the rule statement\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `MATCH | NO_MATCH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderName`  <a name="cfn-wafv2-webacl-ipsetforwardedipconfiguration-headername"></a>
The name of the HTTP header to use for the IP address\. For example, to use the X\-Forwarded\-For \(XFF\) header, set this to `X-Forwarded-For`\.  
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-wafv2-webacl-ipsetforwardedipconfiguration-position"></a>
The position in the header to search for the IP address\. The header can contain IP addresses of the original client and also of proxies\. For example, the header value could be `10.1.1.1, 127.0.0.0, 10.10.10.10` where the first IP address identifies the original client and the rest identify proxies that the request went through\.   
The options for this setting are the following:   
+ FIRST \- Inspect the first IP address in the list of IP addresses in the header\. This is usually the client's original IP\.
+ LAST \- Inspect the last IP address in the list of IP addresses in the header\.
+ ANY \- Inspect all IP addresses in the header for a match\. If the header contains more than 10 IP addresses, AWS WAF inspects the last 10\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ANY | FIRST | LAST`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
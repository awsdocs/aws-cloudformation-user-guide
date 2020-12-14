# AWS::WAFv2::WebACL RateBasedStatementTwo<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo"></a>

Rules statement\. 

## Syntax<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-syntax.json"></a>

```
{
  "[AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatementtwo-aggregatekeytype)" : String,
  "[ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatementtwo-forwardedipconfig)" : ForwardedIPConfiguration,
  "[Limit](#cfn-wafv2-webacl-ratebasedstatementtwo-limit)" : Integer,
  "[ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatementtwo-scopedownstatement)" : StatementThree
}
```

### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-syntax.yaml"></a>

```
  [AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatementtwo-aggregatekeytype): String
  [ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatementtwo-forwardedipconfig): 
    ForwardedIPConfiguration
  [Limit](#cfn-wafv2-webacl-ratebasedstatementtwo-limit): Integer
  [ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatementtwo-scopedownstatement): 
    StatementThree
```

## Properties<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-properties"></a>

`AggregateKeyType`  <a name="cfn-wafv2-webacl-ratebasedstatementtwo-aggregatekeytype"></a>
Setting that indicates how to aggregate the request counts\. The options are the following:  
+ IP \- Aggregate the request counts on the IP address from the web request origin\.
+ FORWARDED\_IP \- Aggregate the request counts on the first IP address in an HTTP header\. If you use this, configure the `ForwardedIPConfig`, to specify the header to use\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `FORWARDED_IP | IP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedIPConfig`  <a name="cfn-wafv2-webacl-ratebasedstatementtwo-forwardedipconfig"></a>
The configuration for inspecting IP addresses in an HTTP header that you specify, instead of using the IP address that's reported by the web request origin\. Commonly, this is the X\-Forwarded\-For \(XFF\) header, but you can specify any header name\.   
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
This configuration is used for `GeoMatchStatement` and `RateBasedStatement`\. For `IPSetReferenceStatement`, use `IPSetForwardedIPConfig` instead\.   
AWS WAF only evaluates the first IP address found in the specified HTTP header\.   
*Required*: No  
*Type*: [ForwardedIPConfiguration](aws-properties-wafv2-webacl-forwardedipconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limit`  <a name="cfn-wafv2-webacl-ratebasedstatementtwo-limit"></a>
Limit on the web request that match any nested statement criteria in any 5 minute period\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScopeDownStatement`  <a name="cfn-wafv2-webacl-ratebasedstatementtwo-scopedownstatement"></a>
Statement nested inside a rate\-based statement to narrow the scope of the requests that AWS WAF counts\.  
*Required*: No  
*Type*: [StatementThree](aws-properties-wafv2-webacl-statementthree.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
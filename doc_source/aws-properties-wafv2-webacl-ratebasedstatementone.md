# AWS::WAFv2::WebACL RateBasedStatementOne<a name="aws-properties-wafv2-webacl-ratebasedstatementone"></a>

A rate\-based rule tracks the rate of requests for each originating IP address, and triggers the rule action when the rate exceeds a limit that you specify on the number of requests in any 5\-minute time span\. You can use this to put a temporary block on requests from an IP address that's sending excessive requests\. 

 When the rule action triggers, AWS WAF blocks additional requests from the IP address until the request rate falls below the limit\. 

 You can optionally nest another statement inside the rate\-based statement, to narrow the scope of the rule so that it only counts requests that match the nested statement\. You can't nest a RateBasedStatement, for example for use inside a NotStatement or OrStatement\. It can only be referenced as a top\-level statement within a rule\.

## Syntax<a name="aws-properties-wafv2-webacl-ratebasedstatementone-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatementone-syntax.json"></a>

```
{
  "[AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatementone-aggregatekeytype)" : String,
  "[ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatementone-forwardedipconfig)" : ForwardedIPConfiguration,
  "[Limit](#cfn-wafv2-webacl-ratebasedstatementone-limit)" : Integer,
  "[ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatementone-scopedownstatement)" : StatementTwo
}
```

### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatementone-syntax.yaml"></a>

```
  [AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatementone-aggregatekeytype): String
  [ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatementone-forwardedipconfig): 
    ForwardedIPConfiguration
  [Limit](#cfn-wafv2-webacl-ratebasedstatementone-limit): Integer
  [ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatementone-scopedownstatement): 
    StatementTwo
```

## Properties<a name="aws-properties-wafv2-webacl-ratebasedstatementone-properties"></a>

`AggregateKeyType`  <a name="cfn-wafv2-webacl-ratebasedstatementone-aggregatekeytype"></a>
Setting that indicates how to aggregate the request counts\. The options are the following:  
+ IP \- Aggregate the request counts on the IP address from the web request origin\.
+ FORWARDED\_IP \- Aggregate the request counts on the first IP address in an HTTP header\. If you use this, configure the `ForwardedIPConfig`, to specify the header to use\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `FORWARDED_IP | IP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedIPConfig`  <a name="cfn-wafv2-webacl-ratebasedstatementone-forwardedipconfig"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [ForwardedIPConfiguration](aws-properties-wafv2-webacl-forwardedipconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limit`  <a name="cfn-wafv2-webacl-ratebasedstatementone-limit"></a>
Limit on the web request that match any nested statement criteria in any 5 minute period\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScopeDownStatement`  <a name="cfn-wafv2-webacl-ratebasedstatementone-scopedownstatement"></a>
Statement nested inside a rate\-based statement to narrow the scope of the requests that AWS WAF counts\.  
*Required*: No  
*Type*: [StatementTwo](aws-properties-wafv2-webacl-statementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
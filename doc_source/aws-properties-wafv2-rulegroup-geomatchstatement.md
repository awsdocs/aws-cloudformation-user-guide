# AWS::WAFv2::RuleGroup GeoMatchStatement<a name="aws-properties-wafv2-rulegroup-geomatchstatement"></a>

A rule statement used to identify web requests based on country of origin\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-geomatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-geomatchstatement-syntax.json"></a>

```
{
  "[CountryCodes](#cfn-wafv2-rulegroup-geomatchstatement-countrycodes)" : [ String, ... ],
  "[ForwardedIPConfig](#cfn-wafv2-rulegroup-geomatchstatement-forwardedipconfig)" : ForwardedIPConfiguration
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-geomatchstatement-syntax.yaml"></a>

```
  [CountryCodes](#cfn-wafv2-rulegroup-geomatchstatement-countrycodes): 
    - String
  [ForwardedIPConfig](#cfn-wafv2-rulegroup-geomatchstatement-forwardedipconfig): 
    ForwardedIPConfiguration
```

## Properties<a name="aws-properties-wafv2-rulegroup-geomatchstatement-properties"></a>

`CountryCodes`  <a name="cfn-wafv2-rulegroup-geomatchstatement-countrycodes"></a>
An array of two\-character country codes, for example, `[ "US", "CN" ]`, from the alpha\-2 country ISO codes of the ISO 3166 international standard\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedIPConfig`  <a name="cfn-wafv2-rulegroup-geomatchstatement-forwardedipconfig"></a>
The configuration for inspecting IP addresses in an HTTP header that you specify, instead of using the IP address that's reported by the web request origin\. Commonly, this is the X\-Forwarded\-For \(XFF\) header, but you can specify any header name\.   
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
*Required*: No  
*Type*: [ForwardedIPConfiguration](aws-properties-wafv2-rulegroup-forwardedipconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
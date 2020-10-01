# AWS::WAFv2::RuleGroup IPSetReferenceStatement<a name="aws-properties-wafv2-rulegroup-ipsetreferencestatement"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A rule statement used to detect web requests coming from particular IP addresses or address ranges\. To use this, create an IPSet that specifies the addresses you want to detect, then use the ARN of that set in this statement\. To create an IP set, see CreateIPSet\.

Each IP set rule statement references an IP set\. You create and maintain the set independent of your rules\. This allows you to use the single set in multiple rules\. When you update the referenced set, AWS WAF automatically updates all rules that reference it\.

## Syntax<a name="aws-properties-wafv2-rulegroup-ipsetreferencestatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-ipsetreferencestatement-syntax.json"></a>

```
{
  "[Arn](#cfn-wafv2-rulegroup-ipsetreferencestatement-arn)" : String,
  "[IPSetForwardedIPConfig](#cfn-wafv2-rulegroup-ipsetreferencestatement-ipsetforwardedipconfig)" : IPSetForwardedIPConfiguration
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-ipsetreferencestatement-syntax.yaml"></a>

```
  [Arn](#cfn-wafv2-rulegroup-ipsetreferencestatement-arn): String
  [IPSetForwardedIPConfig](#cfn-wafv2-rulegroup-ipsetreferencestatement-ipsetforwardedipconfig): 
    IPSetForwardedIPConfiguration
```

## Properties<a name="aws-properties-wafv2-rulegroup-ipsetreferencestatement-properties"></a>

`Arn`  <a name="cfn-wafv2-rulegroup-ipsetreferencestatement-arn"></a>
The Amazon Resource Name \(ARN\) of the IPSet that this statement references\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPSetForwardedIPConfig`  <a name="cfn-wafv2-rulegroup-ipsetreferencestatement-ipsetforwardedipconfig"></a>
The configuration for inspecting IP addresses in an HTTP header that you specify, instead of using the IP address that's reported by the web request origin\. Commonly, this is the X\-Forwarded\-For \(XFF\) header, but you can specify any header name\.   
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
*Required*: No  
*Type*: [IPSetForwardedIPConfiguration](aws-properties-wafv2-rulegroup-ipsetforwardedipconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
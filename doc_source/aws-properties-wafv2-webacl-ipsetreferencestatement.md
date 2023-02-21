# AWS::WAFv2::WebACL IPSetReferenceStatement<a name="aws-properties-wafv2-webacl-ipsetreferencestatement"></a>

A rule statement used to detect web requests coming from particular IP addresses or address ranges\. To use this, create an [AWS::WAFv2::IPSet](aws-resource-wafv2-ipset.md) that specifies the addresses you want to detect, then use the ARN of that set in this statement\. 

Each IP set rule statement references an IP set\. You create and maintain the set independent of your rules\. This allows you to use the single set in multiple rules\. When you update the referenced set, AWS WAF automatically updates all rules that reference it\.

## Syntax<a name="aws-properties-wafv2-webacl-ipsetreferencestatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ipsetreferencestatement-syntax.json"></a>

```
{
  "[Arn](#cfn-wafv2-webacl-ipsetreferencestatement-arn)" : String,
  "[IPSetForwardedIPConfig](#cfn-wafv2-webacl-ipsetreferencestatement-ipsetforwardedipconfig)" : IPSetForwardedIPConfiguration
}
```

### YAML<a name="aws-properties-wafv2-webacl-ipsetreferencestatement-syntax.yaml"></a>

```
  [Arn](#cfn-wafv2-webacl-ipsetreferencestatement-arn): String
  [IPSetForwardedIPConfig](#cfn-wafv2-webacl-ipsetreferencestatement-ipsetforwardedipconfig): 
    IPSetForwardedIPConfiguration
```

## Properties<a name="aws-properties-wafv2-webacl-ipsetreferencestatement-properties"></a>

`Arn`  <a name="cfn-wafv2-webacl-ipsetreferencestatement-arn"></a>
The Amazon Resource Name \(ARN\) of the [AWS::WAFv2::IPSet](aws-resource-wafv2-ipset.md) that this statement references\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPSetForwardedIPConfig`  <a name="cfn-wafv2-webacl-ipsetreferencestatement-ipsetforwardedipconfig"></a>
The configuration for inspecting IP addresses in an HTTP header that you specify, instead of using the IP address that's reported by the web request origin\. Commonly, this is the X\-Forwarded\-For \(XFF\) header, but you can specify any header name\.   
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
*Required*: No  
*Type*: [IPSetForwardedIPConfiguration](aws-properties-wafv2-webacl-ipsetforwardedipconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS WAF IPSet IPSetDescriptors<a name="aws-properties-waf-ipset-ipsetdescriptors"></a>

`IPSetDescriptors` is a property of the [AWS::WAF::IPSet](aws-resource-waf-ipset.md) resource that specifies the IP address type and IP address range \(in CIDR notation\) from which web requests originate\.

## Syntax<a name="w3ab2c21c14e1637b5"></a>

### JSON<a name="aws-properties-waf-ipset-ipsetdescriptors-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-ipset-ipsetdescriptors-type)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-ipset-ipsetdescriptors-value)" : String
}
```

### YAML<a name="aws-properties-waf-ipset-ipsetdescriptors-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-ipset-ipsetdescriptors-type): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-ipset-ipsetdescriptors-value): String
```

## Properties<a name="w3ab2c21c14e1637b7"></a>

`Type`  
The IP address type, such as `IPV4`\. For valid values, see the `Type` contents of the [IPSetDescriptor](http://docs.aws.amazon.com/waf/latest/APIReference/API_IPSetDescriptor.html) data type in the *AWS WAF API Reference*\.  
*Required: *Yes  
*Type*: String

`Value`  
An IP address \(in CIDR notation\) that AWS WAF permits, blocks, or counts\. For example, to specify a single IP address such as `192.0.2.44`, specify `192.0.2.44/32`\. To specify a range of IP addresses such as `192.0.2.0` to `192.0.2.255`, specify `192.0.2.0/24`\.  
*Required: *Yes  
*Type*: String
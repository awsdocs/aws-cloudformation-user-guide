# AWS::WAFRegional::IPSet IPSetDescriptor<a name="aws-properties-wafregional-ipset-ipsetdescriptor"></a>

Specifies the IP address type \(`IPV4` or `IPV6`\) and the IP address range \(in CIDR format\) that web requests originate from\.

## Syntax<a name="aws-properties-wafregional-ipset-ipsetdescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafregional-ipset-ipsetdescriptor-syntax.json"></a>

```
{
  "[Type](#cfn-wafregional-ipset-ipsetdescriptor-type)" : String,
  "[Value](#cfn-wafregional-ipset-ipsetdescriptor-value)" : String
}
```

### YAML<a name="aws-properties-wafregional-ipset-ipsetdescriptor-syntax.yaml"></a>

```
  [Type](#cfn-wafregional-ipset-ipsetdescriptor-type): String
  [Value](#cfn-wafregional-ipset-ipsetdescriptor-value): String
```

## Properties<a name="aws-properties-wafregional-ipset-ipsetdescriptor-properties"></a>

`Type`  <a name="cfn-wafregional-ipset-ipsetdescriptor-type"></a>
Specify `IPV4` or `IPV6`\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `IPV4 | IPV6`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-wafregional-ipset-ipsetdescriptor-value"></a>
Specify an IPv4 address by using CIDR notation\. For example:  
+ To configure AWS WAF to allow, block, or count requests that originated from the IP address 192\.0\.2\.44, specify `192.0.2.44/32`\.
+ To configure AWS WAF to allow, block, or count requests that originated from IP addresses from 192\.0\.2\.0 to 192\.0\.2\.255, specify `192.0.2.0/24`\.
For more information about CIDR notation, see the Wikipedia entry [Classless Inter\-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\.  
Specify an IPv6 address by using CIDR notation\. For example:  
+ To configure AWS WAF to allow, block, or count requests that originated from the IP address 1111:0000:0000:0000:0000:0000:0000:0111, specify `1111:0000:0000:0000:0000:0000:0000:0111/128`\.
+ To configure AWS WAF to allow, block, or count requests that originated from IP addresses 1111:0000:0000:0000:0000:0000:0000:0000 to 1111:0000:0000:0000:ffff:ffff:ffff:ffff, specify `1111:0000:0000:0000:0000:0000:0000:0000/64`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`

# Amazon Simple Email Service ReceiptFilter IpFilter<a name="aws-properties-ses-receiptfilter-ipfilter"></a>

<a name="aws-properties-ses-receiptfilter-ipfilter-description"></a>The `IpFilter` property type specifies whether to accept or reject mail originating from an IP address or range of IP addresses for Amazon SES\.

<a name="aws-properties-ses-receiptfilter-ipfilter-inheritance"></a> `IpFilter` is a property of the [Amazon Simple Email Service ReceiptFilter Filter](aws-properties-ses-receiptfilter-filter.md) property type\.

## Syntax<a name="aws-properties-ses-receiptfilter-ipfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptfilter-ipfilter-syntax.json"></a>

```
{
  "[Policy](#cfn-ses-receiptfilter-ipfilter-policy)" : String,
  "[Cidr](#cfn-ses-receiptfilter-ipfilter-cidr)" : String
}
```

### YAML<a name="aws-properties-ses-receiptfilter-ipfilter-syntax.yaml"></a>

```
[Policy](#cfn-ses-receiptfilter-ipfilter-policy): String
[Cidr](#cfn-ses-receiptfilter-ipfilter-cidr): String
```

## Properties<a name="aws-properties-ses-receiptfilter-ipfilter-properties"></a>

`Policy`  <a name="cfn-ses-receiptfilter-ipfilter-policy"></a>
Indicates whether to block or allow incoming mail from the specified IP addresses\.  
Valid values include `Allow` and `Block`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Cidr`  <a name="cfn-ses-receiptfilter-ipfilter-cidr"></a>
A single IP address or a range of IP addresses that you want to block or allow, specified in Classless Inter\-Domain Routing \(CIDR\) notation\. An example of a single email address is 10\.0\.0\.1\. An example of a range of IP addresses is 10\.0\.0\.1/24\. For more information about CIDR notation, see RFC 2317\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptfilter-ipfilter-seealso"></a>
+ [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*
+ [ReceiptIpFilter](http://docs.aws.amazon.com/ses/latest/APIReference/API_ReceiptIpFilter.html) in the *Amazon Simple Email Service API Reference*
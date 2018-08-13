# Amazon Simple Email Service ReceiptFilter Filter<a name="aws-properties-ses-receiptfilter-filter"></a>

<a name="aws-properties-ses-receiptfilter-filter-description"></a>The `Filter` property type specifies specify whether to accept or reject mail originating from an IP address or range of IP addresses for Amazon SES\.

<a name="aws-properties-ses-receiptfilter-filter-inheritance"></a> `Filter` is a property of the [AWS::SES::ReceiptFilter](aws-resource-ses-receiptfilter.md) property type\.

## Syntax<a name="aws-properties-ses-receiptfilter-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptfilter-filter-syntax.json"></a>

```
{
  "[IpFilter](#cfn-ses-receiptfilter-filter-ipfilter)" : [*IpFilter*](aws-properties-ses-receiptfilter-ipfilter.md),
  "[Name](#cfn-ses-receiptfilter-filter-name)" : String
}
```

### YAML<a name="aws-properties-ses-receiptfilter-filter-syntax.yaml"></a>

```
[IpFilter](#cfn-ses-receiptfilter-filter-ipfilter): [*IpFilter*](aws-properties-ses-receiptfilter-ipfilter.md)
[Name](#cfn-ses-receiptfilter-filter-name): String
```

## Properties<a name="aws-properties-ses-receiptfilter-filter-properties"></a>

`IpFilter`  <a name="cfn-ses-receiptfilter-filter-ipfilter"></a>
The IP addresses to block or allow, and whether to block or allow incoming mail from them\.  
 *Required*: Yes  
 *Type*: [Amazon SES ReceiptFilter IpFilter](aws-properties-ses-receiptfilter-ipfilter.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ses-receiptfilter-filter-name"></a>
The name of the IP address filter\. The name must:  
+ Contain only ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Start and end with a letter or number\.
+ Contain less than 64 characters\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptfilter-filter-seealso"></a>
+ [Creating IP Address Filters for Amazon SES Email Receiving](url-ses-dev;receiving-email-ip-filters.html) in the *Amazon Simple Email Service Developer Guide*
+ [ReceiptFilter](http://docs.aws.amazon.com/ses/latest/APIReference/API_ReceiptFilter.html) in the *Amazon Simple Email Service API Reference*
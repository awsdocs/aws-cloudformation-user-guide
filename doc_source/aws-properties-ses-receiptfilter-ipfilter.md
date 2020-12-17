# AWS::SES::ReceiptFilter IpFilter<a name="aws-properties-ses-receiptfilter-ipfilter"></a>

Receipt IP address filters enable you to specifically accept or reject incoming email that originates from an IP address or range of IP addresses\.

For information about setting up IP address filters, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-ip-filters.html)\.

## Syntax<a name="aws-properties-ses-receiptfilter-ipfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptfilter-ipfilter-syntax.json"></a>

```
{
  "[Cidr](#cfn-ses-receiptfilter-ipfilter-cidr)" : String,
  "[Policy](#cfn-ses-receiptfilter-ipfilter-policy)" : String
}
```

### YAML<a name="aws-properties-ses-receiptfilter-ipfilter-syntax.yaml"></a>

```
  [Cidr](#cfn-ses-receiptfilter-ipfilter-cidr): String
  [Policy](#cfn-ses-receiptfilter-ipfilter-policy): String
```

## Properties<a name="aws-properties-ses-receiptfilter-ipfilter-properties"></a>

`Cidr`  <a name="cfn-ses-receiptfilter-ipfilter-cidr"></a>
An IP address or a range of IP addresses that you want to block or allow, specified in Classless Inter\-Domain Routing \(CIDR\) notation\. An example of a single email address is 10\.0\.0\.1\. An example of a range of IP addresses is 10\.0\.0\.1/24\. For more information about CIDR notation, see [RFC 2317](https://tools.ietf.org/html/rfc2317)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policy`  <a name="cfn-ses-receiptfilter-ipfilter-policy"></a>
Indicates whether to block or allow incoming mail from the specified IP addresses\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
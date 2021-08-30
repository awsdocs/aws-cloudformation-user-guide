# AWS::SES::ReceiptFilter Filter<a name="aws-properties-ses-receiptfilter-filter"></a>

Specifies an IP address filter\.

## Syntax<a name="aws-properties-ses-receiptfilter-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptfilter-filter-syntax.json"></a>

```
{
  "[IpFilter](#cfn-ses-receiptfilter-filter-ipfilter)" : IpFilter,
  "[Name](#cfn-ses-receiptfilter-filter-name)" : String
}
```

### YAML<a name="aws-properties-ses-receiptfilter-filter-syntax.yaml"></a>

```
  [IpFilter](#cfn-ses-receiptfilter-filter-ipfilter): 
    IpFilter
  [Name](#cfn-ses-receiptfilter-filter-name): String
```

## Properties<a name="aws-properties-ses-receiptfilter-filter-properties"></a>

`IpFilter`  <a name="cfn-ses-receiptfilter-filter-ipfilter"></a>
A structure that provides the IP addresses to block or allow, and whether to block or allow incoming mail from them\.  
*Required*: Yes  
*Type*: [IpFilter](aws-properties-ses-receiptfilter-ipfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ses-receiptfilter-filter-name"></a>
The name of the IP address filter\. The name must meet the following requirements:  
+ Contain only ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Start and end with a letter or number\.
+ Contain 64 characters or fewer\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
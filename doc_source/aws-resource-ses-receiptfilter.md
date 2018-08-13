# AWS::SES::ReceiptFilter<a name="aws-resource-ses-receiptfilter"></a>

The `AWS::SES::ReceiptFilter` resource whether to accept or reject mail originating from an IP address or range of IP addresses for Amazon SES\. For more information, see [Creating IP Address Filters for Amazon SES Email Receiving](url-ses-dev;receiving-email-ip-filters.html) in the *Amazon Simple Email Service Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-ses-receiptfilter-syntax)
+ [Properties](#aws-resource-ses-receiptfilter-properties)
+ [Example](#aws-resource-ses-receiptfilter-examples)
+ [See Also](#aws-resource-ses-receiptfilter-seealso)

## Syntax<a name="aws-resource-ses-receiptfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-receiptfilter-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ReceiptFilter",
  "Properties" : {
    "[Filter](#cfn-ses-receiptfilter-filter)" : [*Filter*](aws-properties-ses-receiptfilter-filter.md)
  }
}
```

### YAML<a name="aws-resource-ses-receiptfilter-syntax.yaml"></a>

```
Type: "AWS::SES::ReceiptFilter"
Properties:
  [Filter](#cfn-ses-receiptfilter-filter): [*Filter*](aws-properties-ses-receiptfilter-filter.md)
```

## Properties<a name="aws-resource-ses-receiptfilter-properties"></a>

`Filter`  <a name="cfn-ses-receiptfilter-filter"></a>
The IP addresses to block or allow, and whether to block or allow incoming mail from them\.  
 *Required*: Yes  
 *Type*: [Amazon SES ReceiptFilter Filter](aws-properties-ses-receiptfilter-filter.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Example<a name="aws-resource-ses-receiptfilter-examples"></a>

### <a name="aws-resource-ses-receiptfilter-example1"></a>

#### JSON<a name="aws-resource-ses-receiptfilter-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES ReceiptFilter Sample Template",
    "Parameters": {
        "FilterName": {
            "Type": "String"
        },
        "Policy": {
            "Type": "String"
        },
        "Cidr": {
            "Type": "String"
        }
    },
    "Resources": {
        "ReceiptFilter": {
            "Type": "AWS::SES::ReceiptFilter",
            "Properties": {
                "Filter": {
                    "Name": {
                        "Ref": "FilterName"
                    },
                    "IpFilter": {
                        "Policy": {
                            "Ref": "Policy"
                        },
                        "Cidr": {
                            "Ref": "Cidr"
                        }
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-receiptfilter-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'AWS SES ReceiptFilter Sample Template'
Parameters:
  FilterName:
    Type: String
  Policy:
    Type: String
  Cidr:
    Type: String
Resources:
  ReceiptFilter:
    Type: 'AWS::SES::ReceiptFilter'
    Properties:
      Filter:
        Name: !Ref FilterName
        IpFilter:
          Policy: !Ref Policy
          Cidr: !Ref Cidr
```

## See Also<a name="aws-resource-ses-receiptfilter-seealso"></a>
+ [Creating IP Address Filters for Amazon SES Email Receiving](url-ses-dev;receiving-email-ip-filters.html) in the *Amazon Simple Email Service Developer Guide*
+ [ReceiptFilter](http://docs.aws.amazon.com/ses/latest/APIReference/API_ReceiptFilter.html) in the *Amazon Simple Email Service API Reference*
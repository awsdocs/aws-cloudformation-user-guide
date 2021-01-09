# AWS::SES::ReceiptFilter<a name="aws-resource-ses-receiptfilter"></a>

Specify a new IP address filter\. You use IP address filters when you receive email with Amazon SES\. For more information, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-concepts.html)\.

## Syntax<a name="aws-resource-ses-receiptfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-receiptfilter-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ReceiptFilter",
  "Properties" : {
      "[Filter](#cfn-ses-receiptfilter-filter)" : Filter
    }
}
```

### YAML<a name="aws-resource-ses-receiptfilter-syntax.yaml"></a>

```
Type: AWS::SES::ReceiptFilter
Properties: 
  [Filter](#cfn-ses-receiptfilter-filter): 
    Filter
```

## Properties<a name="aws-resource-ses-receiptfilter-properties"></a>

`Filter`  <a name="cfn-ses-receiptfilter-filter"></a>
A data structure that describes the IP address filter that you want to specify\. This object consists of a name, an IP address range, and a boolean that indicates whether to allow or block mail from the IP range\.  
*Required*: Yes  
*Type*: [Filter](aws-properties-ses-receiptfilter-filter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-ses-receiptfilter--examples"></a>

Specifies an IP address filter for incoming email\.

### <a name="aws-resource-ses-receiptfilter--examples--"></a>



#### JSON<a name="aws-resource-ses-receiptfilter--examples----json"></a>

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

#### YAML<a name="aws-resource-ses-receiptfilter--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS SES ReceiptFilter Sample Template
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
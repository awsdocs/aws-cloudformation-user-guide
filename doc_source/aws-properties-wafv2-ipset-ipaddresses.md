# AWS::WAFv2::IPSet IPAddresses<a name="aws-properties-wafv2-ipset-ipaddresses"></a>

An array of IP addresses or blocks of IP addresses specified in Classless Inter\-Domain Routing \(CIDR\) notation\. AWS WAF supports any CIDR range\. 

## Syntax<a name="aws-properties-wafv2-ipset-ipaddresses-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-ipset-ipaddresses-syntax.json"></a>

```
{
  "[IPAddresses](#cfn-wafv2-ipset-ipaddresses-ipaddresses)" : [ [String](#aws-properties-wafv2-ipset-ipaddresses), ... ]
}
```

### YAML<a name="aws-properties-wafv2-ipset-ipaddresses-syntax.yaml"></a>

```
  [IPAddresses](#cfn-wafv2-ipset-ipaddresses-ipaddresses): 
    - [String](#aws-properties-wafv2-ipset-ipaddresses)
```

## Properties<a name="aws-properties-wafv2-ipset-ipaddresses-properties"></a>

`IPAddresses`  <a name="cfn-wafv2-ipset-ipaddresses-ipaddresses"></a>
An array of IP addresses or blocks of IP addresses specified in Classless Inter\-Domain Routing \(CIDR\) notation\. AWS WAF supports any CIDR range\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-ipset-ipaddresses) of [String](#aws-properties-wafv2-ipset-ipaddresses)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
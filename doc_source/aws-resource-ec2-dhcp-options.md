# AWS::EC2::DHCPOptions<a name="aws-resource-ec2-dhcp-options"></a>

Creates a set of DHCP options for your VPC\.

For more information, see [CreateDhcpOptions](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateDhcpOptions.html) in the *Amazon EC2 API Reference*\.

**Topics**
+ [Syntax](#aws-resource-ec2-dhcpoptions-syntax)
+ [Properties](#w3ab2c21c10d383c11)
+ [Conditional Properties](#dhcp-options-conditional-note)
+ [Return Values](#w3ab2c21c10d383c15)
+ [Example](#w3ab2c21c10d383c17)
+ [See Also](#w3ab2c21c10d383c19)

## Syntax<a name="aws-resource-ec2-dhcpoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-dhcpoptions-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::DHCPOptions",
   "Properties" : {
      "[DomainName](#cfn-ec2-dhcpoptions-domainname)" : String,
      "[DomainNameServers](#cfn-ec2-dhcpoptions-domainnameservers)" : [ String, ... ],
      "[NetbiosNameServers](#cfn-ec2-dhcpoptions-netbiosnameservers)" : [ String, ... ],
      "[NetbiosNodeType](#cfn-ec2-dhcpoptions-netbiosnodetype)" : Number,
      "[NtpServers](#cfn-ec2-dhcpoptions-ntpservers)" : [ String, ... ],
      "[Tags](#cfn-ec2-dhcpoptions-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-dhcpoptions-syntax.yaml"></a>

```
Type: "AWS::EC2::DHCPOptions"
Properties:
  [DomainName](#cfn-ec2-dhcpoptions-domainname): String
  [DomainNameServers](#cfn-ec2-dhcpoptions-domainnameservers):
    - String
  [NetbiosNameServers](#cfn-ec2-dhcpoptions-netbiosnameservers):
    - String
  [NetbiosNodeType](#cfn-ec2-dhcpoptions-netbiosnodetype): Number
  [NtpServers](#cfn-ec2-dhcpoptions-ntpservers):
    - String
  [Tags](#cfn-ec2-dhcpoptions-tags):
    -Resource Tag
```

## Properties<a name="w3ab2c21c10d383c11"></a>

`DomainName`  <a name="cfn-ec2-dhcpoptions-domainname"></a>
A domain name of your choice\.  
*Required*: Conditional; see [note](#dhcp-options-conditional-note)\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
*Example*: `"example.com"`

`DomainNameServers`  <a name="cfn-ec2-dhcpoptions-domainnameservers"></a>
The IP \(IPv4\) address of a domain name server\. You can specify up to four addresses\.  
*Required*: Conditional; see [note](#dhcp-options-conditional-note)\.  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
*Example*: `"DomainNameServers" : [ "10.0.0.1", "10.0.0.2" ]`  
*Example*: To preserve the order of IP addresses, specify a comma delimited list as a single string: `"DomainNameServers" : [ "10.0.0.1, 10.0.0.2" ]`

`NetbiosNameServers`  <a name="cfn-ec2-dhcpoptions-netbiosnameservers"></a>
The IP address \(IPv4\) of a NetBIOS name server\. You can specify up to four addresses\.  
*Required*: Conditional; see [note](#dhcp-options-conditional-note)\.  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
*Example*: `"NetbiosNameServers" : [ "10.0.0.1", "10.0.0.2" ]`  
*Example*: To preserve the order of IP addresses, specify a comma delimited list as a single string: `"NetbiosNameServers" : [ "10.0.0.1, 10.0.0.2" ]`

`NetbiosNodeType`  <a name="cfn-ec2-dhcpoptions-netbiosnodetype"></a>
An integer value indicating the NetBIOS node type:  
+ **1**: Broadcast \("B"\)
+ **2**: Point\-to\-point \("P"\)
+ **4**: Mixed mode \("M"\)
+ **8**: Hybrid \("H"\)
For more information about these values and about NetBIOS node types, see [RFC 2132](http://www.ietf.org/rfc/rfc2132.txt), [RFC 1001](http://tools.ietf.org/rfc/rfc1001.txt), and [RFC 1002](http://tools.ietf.org/rfc/rfc1002.txt)\. We recommend that you use only the value `2` at this time \(broadcast and multicast are not currently supported\)\.  
*Required*: Required if `NetBiosNameServers` is specified; optional otherwise\.  
*Type*: List of numbers  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
*Example*: `"NetbiosNodeType" : 2`

`NtpServers`  <a name="cfn-ec2-dhcpoptions-ntpservers"></a>
The IP address \(IPv4\) of a Network Time Protocol \(NTP\) server\. You can specify up to four addresses\.  
*Required*: Conditional; see [note](#dhcp-options-conditional-note)\.  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
*Example*: `"NtpServers" : [ "10.0.0.1" ]`  
*Example*: To preserve the order of IP addresses, specify a comma delimited list as a single string: `"NtpServers" : [ "10.0.0.1, 10.0.0.2" ]`

`Tags`  <a name="cfn-ec2-dhcpoptions-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this resource\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

## Conditional Properties<a name="dhcp-options-conditional-note"></a>

*At least one* of the following properties must be specified:
+ [DomainNameServers](#cfn-ec2-dhcpoptions-domainnameservers)
+ [NetbiosNameServers](#cfn-ec2-dhcpoptions-netbiosnameservers)
+ [NtpServers](#cfn-ec2-dhcpoptions-ntpservers)

After this condition has been fulfilled, the rest of these properties are optional\.

If you specify `NetbiosNameServers`, then `NetbiosNodeType` is required\.

## Return Values<a name="w3ab2c21c10d383c15"></a>

### Ref<a name="w3ab2c21c10d383c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d383c17"></a>

### JSON<a name="aws-resource-ec2-dhcpoptions-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDhcpOptions" : {
         "Type" : "AWS::EC2::DHCPOptions",
         "Properties" : {
            "DomainName" : "example.com",
            "DomainNameServers" : [ "AmazonProvidedDNS" ],
            "NtpServers" : [ "10.2.5.1" ],
            "NetbiosNameServers" : [ "10.2.5.1" ],
            "NetbiosNodeType" : 2,
            "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-dhcpoptions-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDhcpOptions: 
    Type: "AWS::EC2::DHCPOptions"
    Properties: 
      DomainName: example.com
      DomainNameServers: 
        - AmazonProvidedDNS
      NtpServers: 
        - 10.2.5.1
      NetbiosNameServers: 
        - 10.2.5.1
      NetbiosNodeType: 2
      Tags: 
        - 
          Key: foo
          Value: bar
```

## See Also<a name="w3ab2c21c10d383c19"></a>
+ [CreateDhcpOptions](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateDhcpOptions.html) in the *Amazon EC2 API Reference*
+ [Using Tags](http://docs.aws.amazon.com/AWSEC2/latest/DeveloperGuide/Using_Tags.html) in the *Amazon Elastic Compute Cloud User Guide*\.
+ [RFC 2132](http://www.ietf.org/rfc/rfc2132.txt) \- *DHCP Options and BOOTP Vendor Extensions*, Network Working Group, 1997
+ [RFC 1001](http://tools.ietf.org/rfc/rfc1001.txt) \- *Protocol Standard for a NetBIOS Service on a TCP/UDP Transport: Concepts and Methods*, Network Working Group, 1987
+ [RFC 1002](http://tools.ietf.org/rfc/rfc1002.txt) \- *Protocol Standard for a NetBIOS Service on a TCP/UDP Transport: Detailed Specifications*, Network Working Group, 1987
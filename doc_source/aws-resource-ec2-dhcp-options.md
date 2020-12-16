# AWS::EC2::DHCPOptions<a name="aws-resource-ec2-dhcp-options"></a>

Specifies a set of DHCP options for your VPC\.

You must specify at least one of the following properties: `DomainNameServers`, `NetbiosNameServers`, `NtpServers`\. If you specify `NetbiosNameServers`, you must specify `NetbiosNodeType`\.

## Syntax<a name="aws-resource-ec2-dhcp-options-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-dhcp-options-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::DHCPOptions",
  "Properties" : {
      "[DomainName](#cfn-ec2-dhcpoptions-domainname)" : String,
      "[DomainNameServers](#cfn-ec2-dhcpoptions-domainnameservers)" : [ String, ... ],
      "[NetbiosNameServers](#cfn-ec2-dhcpoptions-netbiosnameservers)" : [ String, ... ],
      "[NetbiosNodeType](#cfn-ec2-dhcpoptions-netbiosnodetype)" : Integer,
      "[NtpServers](#cfn-ec2-dhcpoptions-ntpservers)" : [ String, ... ],
      "[Tags](#cfn-ec2-dhcpoptions-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-dhcp-options-syntax.yaml"></a>

```
Type: AWS::EC2::DHCPOptions
Properties: 
  [DomainName](#cfn-ec2-dhcpoptions-domainname): String
  [DomainNameServers](#cfn-ec2-dhcpoptions-domainnameservers): 
    - String
  [NetbiosNameServers](#cfn-ec2-dhcpoptions-netbiosnameservers): 
    - String
  [NetbiosNodeType](#cfn-ec2-dhcpoptions-netbiosnodetype): Integer
  [NtpServers](#cfn-ec2-dhcpoptions-ntpservers): 
    - String
  [Tags](#cfn-ec2-dhcpoptions-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-dhcp-options-properties"></a>

`DomainName`  <a name="cfn-ec2-dhcpoptions-domainname"></a>
This value is used to complete unqualified DNS hostnames\. If you're using AmazonProvidedDNS in `us-east-1`, specify `ec2.internal`\. If you're using AmazonProvidedDNS in another Region, specify *region*\.`compute.internal` \(for example, `ap-northeast-1.compute.internal`\)\. Otherwise, specify a domain name \(for example, *MyCompany\.com*\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainNameServers`  <a name="cfn-ec2-dhcpoptions-domainnameservers"></a>
The IPv4 addresses of up to four domain name servers, or AmazonProvidedDNS\. The default DHCP option set specifies `AmazonProvidedDNS`\. If specifying more than one domain name server, specify the IP addresses in a single parameter, separated by commas\. To have your instance to receive a custom DNS hostname as specified in `DomainName`, you must set this to a custom DNS server\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetbiosNameServers`  <a name="cfn-ec2-dhcpoptions-netbiosnameservers"></a>
The IPv4 addresses of up to four NetBIOS name servers\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetbiosNodeType`  <a name="cfn-ec2-dhcpoptions-netbiosnodetype"></a>
The NetBIOS node type \(1, 2, 4, or 8\)\. We recommend that you specify 2 \(broadcast and multicast are not currently supported\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NtpServers`  <a name="cfn-ec2-dhcpoptions-ntpservers"></a>
The IPv4 addresses of up to four Network Time Protocol \(NTP\) servers\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-dhcpoptions-tags"></a>
Any tags assigned to the DHCP options set\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-dhcp-options-return-values"></a>

### Ref<a name="aws-resource-ec2-dhcp-options-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-dhcp-options--examples"></a>

### <a name="aws-resource-ec2-dhcp-options--examples--"></a>



#### YAML<a name="aws-resource-ec2-dhcp-options--examples----yaml"></a>

```
myDhcpOptions: 
    Type: AWS::EC2::DHCPOptions
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
          - Key: project
          Value: 123
```

### <a name="aws-resource-ec2-dhcp-options--examples--"></a>



#### JSON<a name="aws-resource-ec2-dhcp-options--examples----json"></a>

```
{
    "myDhcpOptions" : {
        "Type" : "AWS::EC2::DHCPOptions",
        "Properties" : {
            "DomainName" : "example.com",
            "DomainNameServers" : [ "AmazonProvidedDNS" ],
            "NtpServers" : [ "10.2.5.1" ],
            "NetbiosNameServers" : [ "10.2.5.1" ],
            "NetbiosNodeType" : 2,
            "Tags" : [ { "Key" : "project", "Value" : "123" } ]
        }
    }
}
```

## See also<a name="aws-resource-ec2-dhcp-options--seealso"></a>
+  [CreateDhcpOptions](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateDhcpOptions.html) in the *Amazon Elastic Compute Cloud API Reference* 
+ [DHCP Options Sets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_DHCP_Options.html) in the *Amazon Virtual Private Cloud User Guide*


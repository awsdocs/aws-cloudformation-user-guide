# Amazon EC2 LaunchTemplate NetworkInterface<a name="aws-properties-ec2-launchtemplate-networkinterface"></a>

<a name="aws-properties-ec2-launchtemplate-networkinterface-description"></a>The `NetworkInterface` property type specifies parameters for a network interface in an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-networkinterface-inheritance"></a> `NetworkInterface` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-networkinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-networkinterface-syntax.json"></a>

```
{
  "[Description](#cfn-ec2-launchtemplate-networkinterface-description)" : String,
  "[PrivateIpAddress](#cfn-ec2-launchtemplate-networkinterface-privateipaddress)" : String,
  "[PrivateIpAddresses](#cfn-ec2-launchtemplate-networkinterface-privateipaddresses)" : [ [*PrivateIpAdd*](aws-properties-ec2-launchtemplate-privateipadd.md), ... ],
  "[SecondaryPrivateIpAddressCount](#cfn-ec2-launchtemplate-networkinterface-secondaryprivateipaddresscount)" : Integer,
  "[Ipv6AddressCount](#cfn-ec2-launchtemplate-networkinterface-ipv6addresscount)" : Integer,
  "[Groups](#cfn-ec2-launchtemplate-networkinterface-groups)" : [ String, ... ],
  "[DeviceIndex](#cfn-ec2-launchtemplate-networkinterface-deviceindex)" : Integer,
  "[SubnetId](#cfn-ec2-launchtemplate-networkinterface-subnetid)" : String,
  "[Ipv6Addresses](#cfn-ec2-launchtemplate-networkinterface-ipv6addresses)" : [ [*Ipv6Add*](aws-properties-ec2-launchtemplate-ipv6add.md), ... ],
  "[AssociatePublicIpAddress](#cfn-ec2-launchtemplate-networkinterface-associatepublicipaddress)" : Boolean,
  "[NetworkInterfaceId](#cfn-ec2-launchtemplate-networkinterface-networkinterfaceid)" : String,
  "[DeleteOnTermination](#cfn-ec2-launchtemplate-networkinterface-deleteontermination)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-networkinterface-syntax.yaml"></a>

```
[Description](#cfn-ec2-launchtemplate-networkinterface-description): String
[PrivateIpAddress](#cfn-ec2-launchtemplate-networkinterface-privateipaddress): String
[PrivateIpAddresses](#cfn-ec2-launchtemplate-networkinterface-privateipaddresses): 
  - [*PrivateIpAdd*](aws-properties-ec2-launchtemplate-privateipadd.md)
[SecondaryPrivateIpAddressCount](#cfn-ec2-launchtemplate-networkinterface-secondaryprivateipaddresscount): Integer
[Ipv6AddressCount](#cfn-ec2-launchtemplate-networkinterface-ipv6addresscount): Integer
[Groups](#cfn-ec2-launchtemplate-networkinterface-groups): 
  - String
[DeviceIndex](#cfn-ec2-launchtemplate-networkinterface-deviceindex): Integer
[SubnetId](#cfn-ec2-launchtemplate-networkinterface-subnetid): String
[Ipv6Addresses](#cfn-ec2-launchtemplate-networkinterface-ipv6addresses): 
  - [*Ipv6Add*](aws-properties-ec2-launchtemplate-ipv6add.md)
[AssociatePublicIpAddress](#cfn-ec2-launchtemplate-networkinterface-associatepublicipaddress): Boolean
[NetworkInterfaceId](#cfn-ec2-launchtemplate-networkinterface-networkinterfaceid): String
[DeleteOnTermination](#cfn-ec2-launchtemplate-networkinterface-deleteontermination): Boolean
```

## Properties<a name="aws-properties-ec2-launchtemplate-networkinterface-properties"></a>

`AssociatePublicIpAddress`  <a name="cfn-ec2-launchtemplate-networkinterface-associatepublicipaddress"></a>
Associates a public IPv4 address with eth0 for a new network interface\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DeleteOnTermination`  <a name="cfn-ec2-launchtemplate-networkinterface-deleteontermination"></a>
Indicates whether the network interface is deleted when the instance is terminated\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-ec2-launchtemplate-networkinterface-description"></a>
A description for the network interface\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DeviceIndex`  <a name="cfn-ec2-launchtemplate-networkinterface-deviceindex"></a>
The device index for the network interface attachment\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Groups`  <a name="cfn-ec2-launchtemplate-networkinterface-groups"></a>
The IDs of one or more security groups\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Ipv6AddressCount`  <a name="cfn-ec2-launchtemplate-networkinterface-ipv6addresscount"></a>
The number of IPv6 addresses to assign to a network interface\. Amazon EC2 automatically selects the IPv6 addresses from the subnet range\. You can't use this option if specifying specific IPv6 addresses\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Ipv6Addresses`  <a name="cfn-ec2-launchtemplate-networkinterface-ipv6addresses"></a>
One or more specific IPv6 addresses from the IPv6 CIDR block range of your subnet\. You can't use this option if you're specifying a number of IPv6 addresses\.  
 *Required*: No  
 *Type*: List of [Amazon EC2 LaunchTemplate Ipv6Add](aws-properties-ec2-launchtemplate-ipv6add.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NetworkInterfaceId`  <a name="cfn-ec2-launchtemplate-networkinterface-networkinterfaceid"></a>
The ID of the network interface\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PrivateIpAddress`  <a name="cfn-ec2-launchtemplate-networkinterface-privateipaddress"></a>
The primary private IPv4 address of the network interface\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PrivateIpAddresses`  <a name="cfn-ec2-launchtemplate-networkinterface-privateipaddresses"></a>
One or more private IPv4 addresses\.  
 *Required*: No  
 *Type*: List of [Amazon EC2 LaunchTemplate PrivateIpAdd](aws-properties-ec2-launchtemplate-privateipadd.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecondaryPrivateIpAddressCount`  <a name="cfn-ec2-launchtemplate-networkinterface-secondaryprivateipaddresscount"></a>
The number of secondary private IPv4 addresses to assign to a network interface\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetId`  <a name="cfn-ec2-launchtemplate-networkinterface-subnetid"></a>
The ID of the subnet for the network interface\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-networkinterface-seealso"></a>
+ [LaunchTemplateInstanceNetworkInterfaceSpecificationRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateInstanceNetworkInterfaceSpecificationRequest.html) in the *Amazon EC2 API Reference*
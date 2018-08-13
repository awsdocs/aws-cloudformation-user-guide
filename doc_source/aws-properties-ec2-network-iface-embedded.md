# EC2 NetworkInterface Embedded Property Type<a name="aws-properties-ec2-network-iface-embedded"></a>

The `EC2 Network Interface` type is an embedded property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) type\. It specifies a network interface that is to be attached\.

## Syntax<a name="w3ab2c21c14d735b5"></a>

### JSON<a name="aws-properties-ec2-network-iface-embedded-syntax.json"></a>

```
{
  "[AssociatePublicIpAddress](#aws-properties-ec2-network-iface-embedded-associatepubip)" : Boolean,
  "[DeleteOnTermination](#aws-properties-ec2-network-iface-embedded-delete)" : Boolean,
  "[Description](#aws-properties-ec2-network-iface-embedded-description)" : String,
  "[DeviceIndex](#aws-properties-ec2-network-iface-embedded-deviceindex)" : String,
  "[GroupSet](#aws-properties-ec2-network-iface-embedded-groupset)" : [ String, ... ],
  "[NetworkInterfaceId](#aws-properties-ec2-network-iface-embedded-network-iface)" : String,
  "[Ipv6AddressCount](#aws-properties-ec2-network-iface-embedded-ipv6addresscount)" : Integer,
  "[Ipv6Addresses](#aws-properties-ec2-network-iface-embedded-ipv6addresses)" : [ IPv6 Address Type, ... ],
  "[PrivateIpAddress](#aws-properties-ec2-network-iface-embedded-privateipaddress)" : String,
  "[PrivateIpAddresses](#aws-properties-ec2-network-iface-embedded-privateipaddresses)" : [ PrivateIpAddressSpecification, ... ],
  "[SecondaryPrivateIpAddressCount](#aws-properties-ec2-network-iface-embedded-secondprivateip)" : Integer,
  "[SubnetId](#aws-properties-ec2-network-iface-embedded-subnetid)" : String
}
```

### YAML<a name="aws-properties-ec2-network-iface-embedded-syntax.yaml"></a>

```
[AssociatePublicIpAddress](#aws-properties-ec2-network-iface-embedded-associatepubip): Boolean
[DeleteOnTermination](#aws-properties-ec2-network-iface-embedded-delete): Boolean
[Description](#aws-properties-ec2-network-iface-embedded-description): String
[DeviceIndex](#aws-properties-ec2-network-iface-embedded-deviceindex): String
[GroupSet](#aws-properties-ec2-network-iface-embedded-groupset):
  - String
[NetworkInterfaceId](#aws-properties-ec2-network-iface-embedded-network-iface): String
[Ipv6AddressCount](#aws-properties-ec2-network-iface-embedded-ipv6addresscount): Integer
[Ipv6Addresses](#aws-properties-ec2-network-iface-embedded-ipv6addresses):
  - IPv6 Address Type
[PrivateIpAddress](#aws-properties-ec2-network-iface-embedded-privateipaddress): String
[PrivateIpAddresses](#aws-properties-ec2-network-iface-embedded-privateipaddresses):
  - PrivateIpAddressSpecification
[SecondaryPrivateIpAddressCount](#aws-properties-ec2-network-iface-embedded-secondprivateip): Integer
[SubnetId](#aws-properties-ec2-network-iface-embedded-subnetid): String
```

## Properties<a name="w3ab2c21c14d735b7"></a>

`AssociatePublicIpAddress`  <a name="aws-properties-ec2-network-iface-embedded-associatepubip"></a>
Indicates whether the network interface receives a public IP address\. You can associate a public IP address with a network interface only if it has a device index of `eth0` and if it is a new network interface \(not an existing one\)\. In other words, if you specify true, don't specify a network interface ID\. For more information, see [Amazon EC2 Instance IP Addressing](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-instance-addressing.html)\.  
*Required*: No  
*Type*: Boolean\.

`DeleteOnTermination`  <a name="aws-properties-ec2-network-iface-embedded-delete"></a>
Whether to delete the network interface when the instance terminates\.  
*Required*: No  
*Type*: Boolean\.

`Description`  <a name="aws-properties-ec2-network-iface-embedded-description"></a>
The description of this network interface\.  
*Required*: No  
*Type*: String

`DeviceIndex`  <a name="aws-properties-ec2-network-iface-embedded-deviceindex"></a>
The network interface's position in the attachment order\.  
*Required*: Yes  
*Type*: String

`GroupSet`  <a name="aws-properties-ec2-network-iface-embedded-groupset"></a>
A list of security group IDs associated with this network interface\.  
*Required*: No  
*Type*: List of strings\.

`NetworkInterfaceId`  <a name="aws-properties-ec2-network-iface-embedded-network-iface"></a>
An existing network interface ID\.  
*Required*: Conditional\. If you don't specify the `SubnetId` property, you must specify this property\.  
*Type*: String

`Ipv6AddressCount`  <a name="aws-properties-ec2-network-iface-embedded-ipv6addresscount"></a>
The number of IPv6 addresses to associate with the network interface\. Amazon EC2 automatically selects the IPv6 addresses from the subnet range\. To specify specific IPv6 addresses, use the `Ipv6Addresses` property and don't specify this property\.  
For restrictions on which instance types support IPv6 addresses, see the [RunInstances](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-RunInstances.html) action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: Integer

`Ipv6Addresses`  <a name="aws-properties-ec2-network-iface-embedded-ipv6addresses"></a>
One or more specific IPv6 addresses from the IPv6 CIDR block range of your subnet to associate with the network interface\. To specify a number of IPv6 addresses, use the `Ipv6AddressCount` property and don't specify this property\.  
For information about restrictions on which instance types support IPv6 addresses, see the [RunInstances](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-RunInstances.html) action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: List of [EC2 NetworkInterface Ipv6Addresses](aws-properties-ec2-networkinterface-ipv6addresses.md)

`PrivateIpAddress`  <a name="aws-properties-ec2-network-iface-embedded-privateipaddress"></a>
Assigns a single private IP address to the network interface, which is used as the primary private IP address\. If you want to specify multiple private IP address, use the `PrivateIpAddresses` property\.  
*Required*: No  
*Type*: String

`PrivateIpAddresses`  <a name="aws-properties-ec2-network-iface-embedded-privateipaddresses"></a>
Assigns a list of private IP addresses to the network interface\. You can specify a primary private IP address by setting the value of the `Primary` property to `true` in the `PrivateIpAddressSpecification` property\. If you want Amazon EC2 to automatically assign private IP addresses, use the `SecondaryPrivateIpCount` property and do not specify this property\.  
For information about the maximum number of private IP addresses, see [Private IP Addresses Per ENI Per Instance Type](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableIpPerENI) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: list of [PrivateIpAddressSpecification](aws-properties-ec2-network-interface-privateipspec.md)

`SecondaryPrivateIpAddressCount`  <a name="aws-properties-ec2-network-iface-embedded-secondprivateip"></a>
The number of secondary private IP addresses that Amazon EC2 auto assigns to the network interface\. Amazon EC2 uses the value of the `PrivateIpAddress` property as the primary private IP address\. If you don't specify that property, Amazon EC2 auto assigns both the primary and secondary private IP addresses\.  
If you want to specify your own list of private IP addresses, use the `PrivateIpAddresses` property and do not specify this property\.  
For information about the maximum number of private IP addresses, see [Private IP Addresses Per ENI Per Instance Type](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableIpPerENI) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: Integer\.

`SubnetId`  <a name="aws-properties-ec2-network-iface-embedded-subnetid"></a>
The ID of the subnet to associate with the network interface\.  
*Required*: Conditional\. If you don't specify the `NetworkInterfaceId` property, you must specify this property\.  
*Type*: String
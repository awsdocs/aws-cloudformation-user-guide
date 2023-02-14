# AWS::EC2::Instance NetworkInterface<a name="aws-properties-ec2-network-iface-embedded"></a>

Specifies a network interface that is to be attached to an instance\.

You can create a network interface when launching an instance\. For an example, see the [AWS::EC2::Instance examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html#aws-properties-ec2-instance--examples--Automatically_assign_a_public_IP_address)\.

Alternatively, you can attach an existing network interface when launching an instance\. For an example, see the [AWS::EC2:NetworkInterface examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-networkinterface.html#aws-resource-ec2-networkinterface--examples)\.

## Syntax<a name="aws-properties-ec2-network-iface-embedded-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-network-iface-embedded-syntax.json"></a>

```
{
  "[AssociateCarrierIpAddress](#cfn-ec2-instance-networkinterface-associatecarrieripaddress)" : Boolean,
  "[AssociatePublicIpAddress](#aws-properties-ec2-network-iface-embedded-associatepubip)" : Boolean,
  "[DeleteOnTermination](#aws-properties-ec2-network-iface-embedded-delete)" : Boolean,
  "[Description](#aws-properties-ec2-network-iface-embedded-description)" : String,
  "[DeviceIndex](#aws-properties-ec2-network-iface-embedded-deviceindex)" : String,
  "[GroupSet](#aws-properties-ec2-network-iface-embedded-groupset)" : [ String, ... ],
  "[Ipv6AddressCount](#cfn-ec2-instance-networkinterface-ipv6addresscount)" : Integer,
  "[Ipv6Addresses](#cfn-ec2-instance-networkinterface-ipv6addresses)" : [ InstanceIpv6Address, ... ],
  "[NetworkInterfaceId](#aws-properties-ec2-network-iface-embedded-network-iface)" : String,
  "[PrivateIpAddress](#aws-properties-ec2-network-iface-embedded-privateipaddress)" : String,
  "[PrivateIpAddresses](#aws-properties-ec2-network-iface-embedded-privateipaddresses)" : [ PrivateIpAddressSpecification, ... ],
  "[SecondaryPrivateIpAddressCount](#aws-properties-ec2-network-iface-embedded-secondprivateip)" : Integer,
  "[SubnetId](#aws-properties-ec2-network-iface-embedded-subnetid)" : String
}
```

### YAML<a name="aws-properties-ec2-network-iface-embedded-syntax.yaml"></a>

```
  [AssociateCarrierIpAddress](#cfn-ec2-instance-networkinterface-associatecarrieripaddress): Boolean
  [AssociatePublicIpAddress](#aws-properties-ec2-network-iface-embedded-associatepubip): Boolean
  [DeleteOnTermination](#aws-properties-ec2-network-iface-embedded-delete): Boolean
  [Description](#aws-properties-ec2-network-iface-embedded-description): String
  [DeviceIndex](#aws-properties-ec2-network-iface-embedded-deviceindex): String
  [GroupSet](#aws-properties-ec2-network-iface-embedded-groupset): 
    - String
  [Ipv6AddressCount](#cfn-ec2-instance-networkinterface-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-instance-networkinterface-ipv6addresses): 
    - InstanceIpv6Address
  [NetworkInterfaceId](#aws-properties-ec2-network-iface-embedded-network-iface): String
  [PrivateIpAddress](#aws-properties-ec2-network-iface-embedded-privateipaddress): String
  [PrivateIpAddresses](#aws-properties-ec2-network-iface-embedded-privateipaddresses): 
    - PrivateIpAddressSpecification
  [SecondaryPrivateIpAddressCount](#aws-properties-ec2-network-iface-embedded-secondprivateip): Integer
  [SubnetId](#aws-properties-ec2-network-iface-embedded-subnetid): String
```

## Properties<a name="aws-properties-ec2-network-iface-embedded-properties"></a>

`AssociateCarrierIpAddress`  <a name="cfn-ec2-instance-networkinterface-associatecarrieripaddress"></a>
Indicates whether to assign a carrier IP address to the network interface\.  
You can only assign a carrier IP address to a network interface that is in a subnet in a Wavelength Zone\. For more information about carrier IP addresses, see [Carrier IP address](https://docs.aws.amazon.com/wavelength/latest/developerguide/how-wavelengths-work.html#provider-owned-ip) in the * AWS Wavelength Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssociatePublicIpAddress`  <a name="aws-properties-ec2-network-iface-embedded-associatepubip"></a>
Indicates whether to assign a public IPv4 address to an instance\. Applies only if creating a network interface when launching an instance\. The network interface must be the primary network interface\. If launching into a default subnet, the default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeleteOnTermination`  <a name="aws-properties-ec2-network-iface-embedded-delete"></a>
Indicates whether the network interface is deleted when the instance is terminated\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="aws-properties-ec2-network-iface-embedded-description"></a>
The description of the network interface\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceIndex`  <a name="aws-properties-ec2-network-iface-embedded-deviceindex"></a>
The position of the network interface in the attachment order\. A primary network interface has a device index of 0\.  
If you create a network interface when launching an instance, you must specify the device index\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupSet`  <a name="aws-properties-ec2-network-iface-embedded-groupset"></a>
The IDs of the security groups for the network interface\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ipv6AddressCount`  <a name="cfn-ec2-instance-networkinterface-ipv6addresscount"></a>
A number of IPv6 addresses to assign to the network interface\. Amazon EC2 chooses the IPv6 addresses from the range of the subnet\. You cannot specify this option and the option to assign specific IPv6 addresses in the same request\. You can specify this option if you've specified a minimum number of instances to launch\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ipv6Addresses`  <a name="cfn-ec2-instance-networkinterface-ipv6addresses"></a>
The IPv6 addresses to assign to the network interface\. You cannot specify this option and the option to assign a number of IPv6 addresses in the same request\. You cannot specify this option if you've specified a minimum number of instances to launch\.  
*Required*: No  
*Type*: List of [InstanceIpv6Address](aws-properties-ec2-instance-instanceipv6address.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="aws-properties-ec2-network-iface-embedded-network-iface"></a>
The ID of the network interface, when attaching an existing network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="aws-properties-ec2-network-iface-embedded-privateipaddress"></a>
The private IPv4 address of the network interface\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddresses`  <a name="aws-properties-ec2-network-iface-embedded-privateipaddresses"></a>
One or more private IPv4 addresses to assign to the network interface\. Only one private IPv4 address can be designated as primary\.  
*Required*: No  
*Type*: List of [PrivateIpAddressSpecification](aws-properties-ec2-network-interface-privateipspec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryPrivateIpAddressCount`  <a name="aws-properties-ec2-network-iface-embedded-secondprivateip"></a>
The number of secondary private IPv4 addresses\. You can't specify this option and specify more than one private IP address using the private IP addresses option\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="aws-properties-ec2-network-iface-embedded-subnetid"></a>
The ID of the subnet associated with the network interface\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
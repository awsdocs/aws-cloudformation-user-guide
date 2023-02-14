# AWS::EC2::SpotFleet InstanceNetworkInterfaceSpecification<a name="aws-properties-ec2-spotfleet-instancenetworkinterfacespecification"></a>

Describes a network interface\.

## Syntax<a name="aws-properties-ec2-spotfleet-instancenetworkinterfacespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-instancenetworkinterfacespecification-syntax.json"></a>

```
{
  "[AssociatePublicIpAddress](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-associatepublicipaddress)" : Boolean,
  "[DeleteOnTermination](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-deleteontermination)" : Boolean,
  "[Description](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-description)" : String,
  "[DeviceIndex](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-deviceindex)" : Integer,
  "[Groups](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-groups)" : [ String, ... ],
  "[Ipv6AddressCount](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-ipv6addresscount)" : Integer,
  "[Ipv6Addresses](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-ipv6addresses)" : [ InstanceIpv6Address, ... ],
  "[NetworkInterfaceId](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-networkinterfaceid)" : String,
  "[PrivateIpAddresses](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-privateipaddresses)" : [ PrivateIpAddressSpecification, ... ],
  "[SecondaryPrivateIpAddressCount](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-secondaryprivateipaddresscount)" : Integer,
  "[SubnetId](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-subnetid)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-instancenetworkinterfacespecification-syntax.yaml"></a>

```
  [AssociatePublicIpAddress](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-associatepublicipaddress): Boolean
  [DeleteOnTermination](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-deleteontermination): Boolean
  [Description](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-description): String
  [DeviceIndex](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-deviceindex): Integer
  [Groups](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-groups): 
    - String
  [Ipv6AddressCount](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-ipv6addresses): 
    - InstanceIpv6Address
  [NetworkInterfaceId](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-networkinterfaceid): String
  [PrivateIpAddresses](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-privateipaddresses): 
    - PrivateIpAddressSpecification
  [SecondaryPrivateIpAddressCount](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-secondaryprivateipaddresscount): Integer
  [SubnetId](#cfn-ec2-spotfleet-instancenetworkinterfacespecification-subnetid): String
```

## Properties<a name="aws-properties-ec2-spotfleet-instancenetworkinterfacespecification-properties"></a>

`AssociatePublicIpAddress`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-associatepublicipaddress"></a>
Indicates whether to assign a public IPv4 address to an instance you launch in a VPC\. The public IP address can only be assigned to a network interface for eth0, and can only be assigned to a new network interface, not an existing one\. You cannot specify more than one network interface in the request\. If launching into a default subnet, the default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeleteOnTermination`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-deleteontermination"></a>
Indicates whether the network interface is deleted when the instance is terminated\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-description"></a>
The description of the network interface\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeviceIndex`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-deviceindex"></a>
The position of the network interface in the attachment order\. A primary network interface has a device index of 0\.  
If you specify a network interface when launching an instance, you must specify the device index\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Groups`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-groups"></a>
The IDs of the security groups for the network interface\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ipv6AddressCount`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-ipv6addresscount"></a>
A number of IPv6 addresses to assign to the network interface\. Amazon EC2 chooses the IPv6 addresses from the range of the subnet\. You cannot specify this option and the option to assign specific IPv6 addresses in the same request\. You can specify this option if you've specified a minimum number of instances to launch\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ipv6Addresses`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-ipv6addresses"></a>
The IPv6 addresses to assign to the network interface\. You cannot specify this option and the option to assign a number of IPv6 addresses in the same request\. You cannot specify this option if you've specified a minimum number of instances to launch\.  
*Required*: No  
*Type*: List of [InstanceIpv6Address](aws-properties-ec2-spotfleet-instanceipv6address.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInterfaceId`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-networkinterfaceid"></a>
The ID of the network interface\.  
If you are creating a Spot Fleet, omit this parameter because you can’t specify a network interface ID in a launch specification\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrivateIpAddresses`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-privateipaddresses"></a>
The private IPv4 addresses to assign to the network interface\. Only one private IPv4 address can be designated as primary\. You cannot specify this option if you're launching more than one instance in a [RunInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RunInstances.html) request\.  
*Required*: No  
*Type*: List of [PrivateIpAddressSpecification](aws-properties-ec2-spotfleet-privateipaddressspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecondaryPrivateIpAddressCount`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-secondaryprivateipaddresscount"></a>
The number of secondary private IPv4 addresses\. You can't specify this option and specify more than one private IP address using the private IP addresses option\. You cannot specify this option if you're launching more than one instance in a [RunInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RunInstances.html) request\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-spotfleet-instancenetworkinterfacespecification-subnetid"></a>
The ID of the subnet associated with the network interface\. Applies only if creating a network interface when launching an instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
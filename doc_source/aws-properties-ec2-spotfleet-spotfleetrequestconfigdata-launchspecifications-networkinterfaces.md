# Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications NetworkInterfaces<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces"></a>

`NetworkInterfaces` is a property of the [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that defines the network interface of the instances in a Spot fleet\.

## Syntax<a name="w3ab2c21c14d634b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-associatepublicipaddress)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-deleteontermination)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-description)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-deviceindex)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-groups)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-ipv6addresscount)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-ipv6addresses)" : [ IPv6 Address Type, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-networkinterfaceid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses)" : [ PrivateIpAddresses, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-secondaryprivateipaddresscount)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-subnetid)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-associatepublicipaddress): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-deleteontermination): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-description): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-deviceindex): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-groups):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-ipv6addresscount): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-ipv6addresses):
  - IPv6 Address Type
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-networkinterfaceid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses):
  - PrivateIpAddresses
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-secondaryprivateipaddresscount): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-subnetid): String
```

## Properties<a name="w3ab2c21c14d634b7"></a>

`AssociatePublicIpAddress`  
Indicates whether to assign a public IP address to an instance that you launch in a VPC\. You can assign the public IP address can only to a network interface for eth0, and only to a new network interface, not an existing one\.  
*Required: *No  
*Type*: Boolean

`DeleteOnTermination`  
Indicates whether to delete the network interface when the instance terminates\.  
*Required: *No  
*Type*: Boolean

`Description`  
The description of this network interface\.  
*Required: *No  
*Type*: String

`DeviceIndex`  
The network interface's position in the attachment order\.  
*Required: *No  
*Type*: Integer

`Groups`  
A list of security group IDs to associate with this network interface\.  
*Required: *No  
*Type*: List of String values

`Ipv6AddressCount`  
The number of IPv6 addresses to associate with the network interface\. Amazon Elastic Compute Cloud automatically selects the IPv6 addresses from the subnet range\. To specify specific IPv6 addresses, use the `Ipv6Addresses` property and don't specify this property\.  
*Required: *No  
*Type*: Integer

`Ipv6Addresses`  
One or more specific IPv6 addresses from the IPv6 CIDR block range of your subnet to associate with the network interface\. To specify a number of IPv6 addresses, use the `Ipv6AddressCount` property and don't specify this property\.  
*Required: *No  
*Type*: List of [EC2 NetworkInterface Ipv6Addresses](aws-properties-ec2-networkinterface-ipv6addresses.md)

`NetworkInterfaceId`  
A network interface ID\.  
*Required: *No  
*Type*: String

`PrivateIpAddresses`  
One or more private IP addresses to assign to the network interface\.  
*Required: *No  
*Type*: List of [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications NetworkInterfaces PrivateIpAddresses](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-networkinterfaces-privateipaddresses.md)

`SecondaryPrivateIpAddressCount`  
The number of secondary private IP addresses that Amazon EC2 automatically assigns to the network interface\.  
*Required: *No  
*Type*: Integer

`SubnetId`  
The ID of the subnet to associate with the network interface\.  
*Required: *Conditional\. If you don't specify the `NetworkInterfaceId` property, you must specify this property\.  
*Type*: String
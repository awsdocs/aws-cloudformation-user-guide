# AWS::EC2::NetworkInterface<a name="aws-resource-ec2-networkinterface"></a>

Describes a network interface in an Amazon EC2 instance for AWS CloudFormation\.

## Syntax<a name="aws-resource-ec2-networkinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinterface-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInterface",
  "Properties" : {
      "[Description](#cfn-ec2-networkinterface-description)" : String,
      "[GroupSet](#cfn-ec2-networkinterface-groupset)" : [ String, ... ],
      "[InterfaceType](#cfn-ec2-networkinterface-interfacetype)" : String,
      "[Ipv6AddressCount](#cfn-ec2-networkinterface-ipv6addresscount)" : Integer,
      "[Ipv6Addresses](#cfn-ec2-networkinterface-ipv6addresses)" : [ InstanceIpv6Address, ... ],
      "[PrivateIpAddress](#cfn-ec2-networkinterface-privateipaddress)" : String,
      "[PrivateIpAddresses](#cfn-ec2-networkinterface-privateipaddresses)" : [ PrivateIpAddressSpecification, ... ],
      "[SecondaryPrivateIpAddressCount](#cfn-ec2-networkinterface-secondaryprivateipaddresscount)" : Integer,
      "[SourceDestCheck](#cfn-ec2-networkinterface-sourcedestcheck)" : Boolean,
      "[SubnetId](#cfn-ec2-networkinterface-subnetid)" : String,
      "[Tags](#cfn-ec2-networkinterface-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-networkinterface-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkInterface
Properties: 
  [Description](#cfn-ec2-networkinterface-description): String
  [GroupSet](#cfn-ec2-networkinterface-groupset): 
    - String
  [InterfaceType](#cfn-ec2-networkinterface-interfacetype): String
  [Ipv6AddressCount](#cfn-ec2-networkinterface-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-networkinterface-ipv6addresses): 
    - InstanceIpv6Address
  [PrivateIpAddress](#cfn-ec2-networkinterface-privateipaddress): String
  [PrivateIpAddresses](#cfn-ec2-networkinterface-privateipaddresses): 
    - PrivateIpAddressSpecification
  [SecondaryPrivateIpAddressCount](#cfn-ec2-networkinterface-secondaryprivateipaddresscount): Integer
  [SourceDestCheck](#cfn-ec2-networkinterface-sourcedestcheck): Boolean
  [SubnetId](#cfn-ec2-networkinterface-subnetid): String
  [Tags](#cfn-ec2-networkinterface-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-networkinterface-properties"></a>

`Description`  <a name="cfn-ec2-networkinterface-description"></a>
A description for the network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupSet`  <a name="cfn-ec2-networkinterface-groupset"></a>
The security group IDs associated with this network interface\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InterfaceType`  <a name="cfn-ec2-networkinterface-interfacetype"></a>
The type of network interface\. The default is `interface`\. The supported values are `efa` and `trunk`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `branch | efa | trunk`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ipv6AddressCount`  <a name="cfn-ec2-networkinterface-ipv6addresscount"></a>
The number of IPv6 addresses to assign to a network interface\. Amazon EC2 automatically selects the IPv6 addresses from the subnet range\. To specify specific IPv6 addresses, use the `Ipv6Addresses` property and don't specify this property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ipv6Addresses`  <a name="cfn-ec2-networkinterface-ipv6addresses"></a>
One or more specific IPv6 addresses from the IPv6 CIDR block range of your subnet to associate with the network interface\. If you're specifying a number of IPv6 addresses, use the `Ipv6AddressCount` property and don't specify this property\.  
*Required*: No  
*Type*: List of [InstanceIpv6Address](aws-properties-ec2-networkinterface-instanceipv6address.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-networkinterface-privateipaddress"></a>
Assigns a single private IP address to the network interface, which is used as the primary private IP address\. If you want to specify multiple private IP address, use the `PrivateIpAddresses` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrivateIpAddresses`  <a name="cfn-ec2-networkinterface-privateipaddresses"></a>
Assigns private IP addresses to the network interface\. You can specify a primary private IP address by setting the value of the `Primary` property to `true` in the `PrivateIpAddressSpecification` property\. If you want EC2 to automatically assign private IP addresses, use the `SecondaryPrivateIpAddressCount` property and do not specify this property\.  
*Required*: No  
*Type*: List of [PrivateIpAddressSpecification](aws-properties-ec2-networkinterface-privateipaddressspecification.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SecondaryPrivateIpAddressCount`  <a name="cfn-ec2-networkinterface-secondaryprivateipaddresscount"></a>
The number of secondary private IPv4 addresses to assign to a network interface\. When you specify a number of secondary IPv4 addresses, Amazon EC2 selects these IP addresses within the subnet's IPv4 CIDR range\. You can't specify this option and specify more than one private IP address using `privateIpAddresses`\.  
You can't specify a count of private IPv4 addresses if you've specified one of the following: specific private IPv4 addresses, specific IPv4 prefixes, or a count of IPv4 prefixes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceDestCheck`  <a name="cfn-ec2-networkinterface-sourcedestcheck"></a>
Enable or disable source/destination checks, which ensure that the instance is either the source or the destination of any traffic that it receives\. If the value is `true`, source/destination checks are enabled; otherwise, they are disabled\. The default value is `true`\. You must disable source/destination checks if the instance runs services such as network address translation, routing, or firewalls\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-ec2-networkinterface-subnetid"></a>
The ID of the subnet to associate with the network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-networkinterface-tags"></a>
An arbitrary set of tags \(key\-value pairs\) for this network interface\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-networkinterface-return-values"></a>

### Ref<a name="aws-resource-ec2-networkinterface-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the network interface\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-networkinterface-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-networkinterface-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the network interface\.

`PrimaryPrivateIpAddress`  <a name="PrimaryPrivateIpAddress-fn::getatt"></a>
The primary private IP address of the network interface\. For example, `10.0.0.192`\.

`SecondaryPrivateIpAddresses`  <a name="SecondaryPrivateIpAddresses-fn::getatt"></a>
The secondary private IP addresses of the network interface\. For example, `["10.0.0.161", "10.0.0.162", "10.0.0.163"]`\.

## Examples<a name="aws-resource-ec2-networkinterface--examples"></a>



### Basic network interface<a name="aws-resource-ec2-networkinterface--examples--Basic_network_interface"></a>

This example creates a standalone elastic network interface \(ENI\)\. To learn how to attach this network interface to an instance at launch, see the next example on this page\.

#### JSON<a name="aws-resource-ec2-networkinterface--examples--Basic_network_interface--json"></a>

```
"myENI" : {
   "Type" : "AWS::EC2::NetworkInterface",
   "Properties" : {
      "Tags": [{"Key":"stack","Value":"production"}],
      "Description": "A nice description.",
      "SourceDestCheck": "false",
      "GroupSet": ["sg-75zzz219"],
      "SubnetId": "subnet-3z648z53",
      "PrivateIpAddress": "10.0.0.16"
   }
}
```

#### YAML<a name="aws-resource-ec2-networkinterface--examples--Basic_network_interface--yaml"></a>

```
   myENI:
      Type: AWS::EC2::NetworkInterface
      Properties:
         Tags:
         - Key: stack
           Value: production
         Description: A nice description.
         SourceDestCheck: 'false'
         GroupSet:
         - sg-75zzz219
         SubnetId: subnet-3z648z53
         PrivateIpAddress: 10.0.0.16
```

### Attach a network interface to an EC2 instance at launch<a name="aws-resource-ec2-networkinterface--examples--Attach_a_network_interface_to_an_EC2_instance_at_launch"></a>

This example attaches a network interface to an EC2 instance\. You can use the NetworkInterface property to add more than one network interface\. However, you can specify multiple network interfaces if they all have only private IP addresses \(no associated public IP address\)\. If you have a network interface with a public IP address, specify when you launch the instance and then use `AWS::EC2::NetworkInterfaceAttachment` to attach the additional network interfaces\.

#### JSON<a name="aws-resource-ec2-networkinterface--examples--Attach_a_network_interface_to_an_EC2_instance_at_launch--json"></a>

```
"Ec2Instance" : {
   "Type" : "AWS::EC2::Instance",
   "Properties" : {
      "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]},
      "KeyName" : { "Ref" : "KeyName" },
      "SecurityGroupIds" : [{ "Ref" : "WebSecurityGroup" }],
      "SubnetId" : { "Ref" : "SubnetId" },
      "NetworkInterfaces" : [ {
         "NetworkInterfaceId" : {"Ref" : "myENI"}, "DeviceIndex" : "1" } ],
      "Tags" : [ {"Key" : "Role", "Value" : "Test Instance"}],
      "UserData" : { "Fn::Base64" : { "Ref" : "WebServerPort" }}
   }
}
```

#### YAML<a name="aws-resource-ec2-networkinterface--examples--Attach_a_network_interface_to_an_EC2_instance_at_launch--yaml"></a>

```
Ec2Instance:
   Type: AWS::EC2::Instance
   Properties:
      ImageId:
         Fn::FindInMap:
         - RegionMap
         - Ref: AWS::Region
         - AMI
      KeyName:
         Ref: KeyName
      SecurityGroupIds:
      - Ref: WebSecurityGroup
      SubnetId:
         Ref: SubnetId
      NetworkInterfaces:
      - NetworkInterfaceId:
         Ref: myENI
        DeviceIndex: '1'
      Tags:
      - Key: Role
        Value: Test Instance
      UserData:
         Fn::Base64:
            Ref: WebServerPort
```

## See also<a name="aws-resource-ec2-networkinterface--seealso"></a>
+ [NetworkInterface](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_NetworkInterface.html) in the *Amazon EC2 API Reference*


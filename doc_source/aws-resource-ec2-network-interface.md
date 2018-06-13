# AWS::EC2::NetworkInterface<a name="aws-resource-ec2-network-interface"></a>

Describes a network interface in an Elastic Compute Cloud \(EC2\) instance for AWS CloudFormation\. This is provided in a list in the `NetworkInterfaces` property of [AWS::EC2::Instance](aws-properties-ec2-instance.md)\.

**Topics**
+ [Syntax](#aws-resource-ec2-networkinterface-syntax)
+ [Properties](#w3ab2c21c10d438b9)
+ [Return Values](#w3ab2c21c10d438c11)
+ [Examples](#cfn-awsec2networkinterface-templateexamples)
+ [More Info](#w3ab2c21c10d438c15)

## Syntax<a name="aws-resource-ec2-networkinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinterface-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::NetworkInterface",
   "Properties" : {
      "[Description](#cfn-awsec2networkinterface-description)" : String,
      "[GroupSet](#cfn-awsec2networkinterface-groupset)" : [ String, ... ],
      "[Ipv6AddressCount](#cfn-ec2-networkinterface-ipv6addresscount)" : Integer,
      "[Ipv6Addresses](#cfn-ec2-networkinterface-ipv6addresses)" : [ Ipv6Address, ... ],
      "[PrivateIpAddress](#cfn-awsec2networkinterface-privateipaddress)" : String,
      "[PrivateIpAddresses](#cfn-awsec2networkinterface-privateipaddresses)" : [ PrivateIpAddressSpecification, ... ],
      "[SecondaryPrivateIpAddressCount](#cfn-awsec2networkinterface-secondaryprivateipcount)" : Integer,
      "[SourceDestCheck](#cfn-awsec2networkinterface-sourcedestcheck)" : Boolean,
      "[SubnetId](#cfn-awsec2networkinterface-subnetid)" : String,
      "[Tags](#cfn-awsec2networkinterface-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-networkinterface-syntax.yaml"></a>

```
Type: "AWS::EC2::NetworkInterface"
Properties: 
  [Description](#cfn-awsec2networkinterface-description): String
  [GroupSet](#cfn-awsec2networkinterface-groupset):
    - String
  [Ipv6AddressCount](#cfn-ec2-networkinterface-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-networkinterface-ipv6addresses):
    - Ipv6Address
  [PrivateIpAddress](#cfn-awsec2networkinterface-privateipaddress): String
  [PrivateIpAddresses](#cfn-awsec2networkinterface-privateipaddresses):
    - PrivateIpAddressSpecification
  [SecondaryPrivateIpAddressCount](#cfn-awsec2networkinterface-secondaryprivateipcount): Integer
  [SourceDestCheck](#cfn-awsec2networkinterface-sourcedestcheck): Boolean
  [SubnetId](#cfn-awsec2networkinterface-subnetid): String
  [Tags](#cfn-awsec2networkinterface-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d438b9"></a>

`Description`  <a name="cfn-awsec2networkinterface-description"></a>
The description of this network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`GroupSet`  <a name="cfn-awsec2networkinterface-groupset"></a>
A list of security group IDs associated with this network interface\.  
*Required*: No  
*Type*: List of strings\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Ipv6AddressCount`  <a name="cfn-ec2-networkinterface-ipv6addresscount"></a>
The number of IPv6 addresses to associate with the network interface\. EC2 automatically selects the IPv6 addresses from the subnet range\. To specify specific IPv6 addresses, use the `Ipv6Addresses` property and don't specify this property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Ipv6Addresses`  <a name="cfn-ec2-networkinterface-ipv6addresses"></a>
One or more specific IPv6 addresses from the IPv6 CIDR block range of your subnet to associate with the network interface\. If you're specifying a number of IPv6 addresses, use the `Ipv6AddressCount` property and don't specify this property\.  
*Required*: No  
*Type*: List of [EC2 NetworkInterface Ipv6Addresses](aws-properties-ec2-networkinterface-ipv6addresses.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PrivateIpAddress`  <a name="cfn-awsec2networkinterface-privateipaddress"></a>
Assigns a single private IP address to the network interface, which is used as the primary private IP address\. If you want to specify multiple private IP address, use the `PrivateIpAddresses` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`PrivateIpAddresses`  <a name="cfn-awsec2networkinterface-privateipaddresses"></a>
Assigns a list of private IP addresses to the network interface\. You can specify a primary private IP address by setting the value of the `Primary` property to `true` in the `PrivateIpAddressSpecification` property\. If you want EC2 to automatically assign private IP addresses, use the `SecondaryPrivateIpAddressCount` property and do not specify this property\.  
For information about the maximum number of private IP addresses, see [Private IP Addresses Per ENI Per Instance Type](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html#AvailableIpPerENI) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: list of [PrivateIpAddressSpecification](aws-properties-ec2-network-interface-privateipspec.md)\.  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you change the primary private IP address\. If not, update requires [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`SecondaryPrivateIpAddressCount`  <a name="cfn-awsec2networkinterface-secondaryprivateipcount"></a>
The number of secondary private IP addresses that EC2 automatically assigns to the network interface\. EC2 uses the value of the `PrivateIpAddress` property as the primary private IP address\. If you don't specify that property, EC2 automatically assigns both the primary and secondary private IP addresses\.  
If you want to specify your own list of private IP addresses, use the `PrivateIpAddresses` property and do not specify this property\.  
For information about the maximum number of private IP addresses, see [Private IP Addresses Per ENI Per Instance Type](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html#AvailableIpPerENI) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: Integer\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`SourceDestCheck`  <a name="cfn-awsec2networkinterface-sourcedestcheck"></a>
Flag indicating whether traffic to or from the instance is validated\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`SubnetId`  <a name="cfn-awsec2networkinterface-subnetid"></a>
The ID of the subnet to associate with the network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`Tags`  <a name="cfn-awsec2networkinterface-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this network interface\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

## Return Values<a name="w3ab2c21c10d438c11"></a>

### Ref<a name="w3ab2c21c10d438c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d438c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`PrimaryPrivateIpAddress`  
Returns the primary private IP address of the network interface\. For example, `10.0.0.192`\.

`SecondaryPrivateIpAddresses`  
Returns the secondary private IP addresses of the network interface\. For example, `["10.0.0.161", "10.0.0.162", "10.0.0.163"]`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="cfn-awsec2networkinterface-templateexamples"></a>

**Tip**  
For more NetworkInterface template examples, see [Elastic Network Interface \(ENI\) Template Snippets](quickref-ec2.md#cfn-template-snippets-eni)\.

### Simple Standalone ENI<a name="w3ab2c21c10d438c13b4"></a>

This is a simple standalone Elastic Network Interface \(ENI\), using all of the available properties\.

#### JSON<a name="aws-resource-ec2-networkinterface-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Description" : "Simple Standalone ENI",
   "Resources" : {
      "myENI" : {
         "Type" : "AWS::EC2::NetworkInterface",
         "Properties" : {
            "Tags": [{"Key":"foo","Value":"bar"}],
            "Description": "A nice description.",
            "SourceDestCheck": "false",
            "GroupSet": ["sg-75zzz219"],
            "SubnetId": "subnet-3z648z53",
            "PrivateIpAddress": "10.0.0.16"
         }
      }
   }
}
```

#### YAML<a name="aws-resource-ec2-networkinterface-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Simple Standalone ENI
Resources:
  myENI:
    Type: AWS::EC2::NetworkInterface
    Properties:
      Tags:
      - Key: foo
        Value: bar
      Description: A nice description.
      SourceDestCheck: 'false'
      GroupSet:
      - sg-75zzz219
      SubnetId: subnet-3z648z53
      PrivateIpAddress: 10.0.0.16
```

### ENI on an EC2 instance<a name="w3ab2c21c10d438c13b6"></a>

This is an example of an ENI on an EC2 instance\. In this example, one ENI is added to the instance\. If you want to add more than one ENI, you can specify a list for the `NetworkInterface` property\. However, you can specify multiple ENIs only if all the ENIs have just private IP addresses \(no associated public IP address\)\. If you have an ENI with a public IP address, specify it and then use the `AWS::EC2::NetworkInterfaceAttachment` resource to add additional ENIs\.

#### JSON<a name="aws-resource-ec2-networkinterface-example-2.json"></a>

```
"Ec2Instance" : {
   "Type" : "AWS::EC2::Instance",
   "Properties" : {
      "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]},
      "KeyName" : { "Ref" : "KeyName" },
      "SecurityGroupIds" : [{ "Ref" : "WebSecurityGroup" }],
      "SubnetId" : { "Ref" : "SubnetId" },
      "NetworkInterfaces" : [ {
         "NetworkInterfaceId" : {"Ref" : "controlXface"}, "DeviceIndex" : "1" } ],
      "Tags" : [ {"Key" : "Role", "Value" : "Test Instance"}],
      "UserData" : { "Fn::Base64" : { "Ref" : "WebServerPort" }}
   }
}
```

#### YAML<a name="aws-resource-ec2-networkinterface-example-2.yaml"></a>

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
        Ref: controlXface
      DeviceIndex: '1'
    Tags:
    - Key: Role
      Value: Test Instance
    UserData:
      Fn::Base64:
        Ref: WebServerPort
```

## More Info<a name="w3ab2c21c10d438c15"></a>
+ [NetworkInterface](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_NetworkInterface.html) in the *Amazon Elastic Compute Cloud API Reference*
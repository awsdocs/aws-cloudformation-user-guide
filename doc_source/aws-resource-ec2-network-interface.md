# AWS::EC2::NetworkInterface<a name="aws-resource-ec2-network-interface"></a>

Describes a network interface in an Elastic Compute Cloud \(EC2\) instance for AWS CloudFormation\.

## Syntax<a name="aws-resource-ec2-network-interface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-network-interface-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInterface",
  "Properties" : {
      "[Description](#cfn-awsec2networkinterface-description)" : String,
      "[GroupSet](#cfn-awsec2networkinterface-groupset)" : [ String, ... ],
      "[InterfaceType](#cfn-ec2-networkinterface-interfacetype)" : String,
      "[Ipv6AddressCount](#cfn-ec2-networkinterface-ipv6addresscount)" : Integer,
      "[Ipv6Addresses](#cfn-ec2-networkinterface-ipv6addresses)" : [ InstanceIpv6Address, ... ],
      "[PrivateIpAddress](#cfn-awsec2networkinterface-privateipaddress)" : String,
      "[PrivateIpAddresses](#cfn-awsec2networkinterface-privateipaddresses)" : [ PrivateIpAddressSpecification, ... ],
      "[SecondaryPrivateIpAddressCount](#cfn-awsec2networkinterface-secondaryprivateipcount)" : Integer,
      "[SourceDestCheck](#cfn-awsec2networkinterface-sourcedestcheck)" : Boolean,
      "[SubnetId](#cfn-awsec2networkinterface-subnetid)" : String,
      "[Tags](#cfn-awsec2networkinterface-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-network-interface-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkInterface
Properties: 
  [Description](#cfn-awsec2networkinterface-description): String
  [GroupSet](#cfn-awsec2networkinterface-groupset): 
    - String
  [InterfaceType](#cfn-ec2-networkinterface-interfacetype): String
  [Ipv6AddressCount](#cfn-ec2-networkinterface-ipv6addresscount): Integer
  [Ipv6Addresses](#cfn-ec2-networkinterface-ipv6addresses): 
    - InstanceIpv6Address
  [PrivateIpAddress](#cfn-awsec2networkinterface-privateipaddress): String
  [PrivateIpAddresses](#cfn-awsec2networkinterface-privateipaddresses): 
    - PrivateIpAddressSpecification
  [SecondaryPrivateIpAddressCount](#cfn-awsec2networkinterface-secondaryprivateipcount): Integer
  [SourceDestCheck](#cfn-awsec2networkinterface-sourcedestcheck): Boolean
  [SubnetId](#cfn-awsec2networkinterface-subnetid): String
  [Tags](#cfn-awsec2networkinterface-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-network-interface-properties"></a>

`Description`  <a name="cfn-awsec2networkinterface-description"></a>
A description for the network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupSet`  <a name="cfn-awsec2networkinterface-groupset"></a>
A list of security group IDs associated with this network interface\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InterfaceType`  <a name="cfn-ec2-networkinterface-interfacetype"></a>
Indicates the type of network interface\. To create an Elastic Fabric Adapter \(EFA\), specify `efa`\. For more information, see [ Elastic Fabric Adapter](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/efa.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `efa`  
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

`PrivateIpAddress`  <a name="cfn-awsec2networkinterface-privateipaddress"></a>
Assigns a single private IP address to the network interface, which is used as the primary private IP address\. If you want to specify multiple private IP address, use the `PrivateIpAddresses` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrivateIpAddresses`  <a name="cfn-awsec2networkinterface-privateipaddresses"></a>
Assigns a list of private IP addresses to the network interface\. You can specify a primary private IP address by setting the value of the `Primary` property to `true` in the `PrivateIpAddressSpecification` property\. If you want EC2 to automatically assign private IP addresses, use the `SecondaryPrivateIpAddressCount` property and do not specify this property\.  
*Required*: No  
*Type*: List of [PrivateIpAddressSpecification](aws-properties-ec2-network-interface-privateipspec.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`SecondaryPrivateIpAddressCount`  <a name="cfn-awsec2networkinterface-secondaryprivateipcount"></a>
The number of secondary private IPv4 addresses to assign to a network interface\. When you specify a number of secondary IPv4 addresses, Amazon EC2 selects these IP addresses within the subnet's IPv4 CIDR range\. You can't specify this option and specify more than one private IP address using `privateIpAddresses`\.  
The number of IP addresses you can assign to a network interface varies by instance type\. For more information, see [IP Addresses Per ENI Per Instance Type](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html#AvailableIpPerENI) in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceDestCheck`  <a name="cfn-awsec2networkinterface-sourcedestcheck"></a>
Indicates whether traffic to or from the instance is validated\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-awsec2networkinterface-subnetid"></a>
The ID of the subnet to associate with the network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-awsec2networkinterface-tags"></a>
An arbitrary set of tags \(key\-value pairs\) for this network interface\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-network-interface-return-values"></a>

### Ref<a name="aws-resource-ec2-network-interface-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-network-interface-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-network-interface-return-values-fn--getatt-fn--getatt"></a>

`PrimaryPrivateIpAddress`  <a name="PrimaryPrivateIpAddress-fn::getatt"></a>
Returns the primary private IP address of the network interface\. For example, `10.0.0.192`\.

`SecondaryPrivateIpAddresses`  <a name="SecondaryPrivateIpAddresses-fn::getatt"></a>
Returns the secondary private IP addresses of the network interface\. For example, `["10.0.0.161", "10.0.0.162", "10.0.0.163"]`\.

## Examples<a name="aws-resource-ec2-network-interface--examples"></a>

 *Tip* 

For more `NetworkInterface` template examples, see [Elastic Network Interface \(ENI\) Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-ec2.html#cfn-template-snippets-eni)\.

### Simple Standalone ENI<a name="aws-resource-ec2-network-interface--examples--Simple_Standalone_ENI"></a>

This is a simple standalone Elastic Network Interface \(ENI\), using all of the available properties\.

#### JSON<a name="aws-resource-ec2-network-interface--examples--Simple_Standalone_ENI--json"></a>

```
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
```

#### YAML<a name="aws-resource-ec2-network-interface--examples--Simple_Standalone_ENI--yaml"></a>

```
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

### ENI on an EC2 instance<a name="aws-resource-ec2-network-interface--examples--ENI_on_an_EC2_instance"></a>

This is an example of an ENI on an EC2 instance\. In this example, one ENI is added to the instance\. If you want to add more than one ENI, you can specify a list for the NetworkInterface property\. However, you can specify multiple ENIs only if all the ENIs have just private IP addresses \(no associated public IP address\)\. If you have an ENI with a public IP address, specify it and then use the `AWS::EC2::NetworkInterfaceAttachment` resource to add additional ENIs\.

#### JSON<a name="aws-resource-ec2-network-interface--examples--ENI_on_an_EC2_instance--json"></a>

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

#### YAML<a name="aws-resource-ec2-network-interface--examples--ENI_on_an_EC2_instance--yaml"></a>

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
        DeviceIndex: '0'
      Tags:
      - Key: Role
        Value: Test Instance
      UserData:
         Fn::Base64:
            Ref: WebServerPort
```

## See also<a name="aws-resource-ec2-network-interface--seealso"></a>
+ [NetworkInterface](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_NetworkInterface.html) in the *Amazon Elastic Compute Cloud API Reference*


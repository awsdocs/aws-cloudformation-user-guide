# AWS::EC2::Subnet<a name="aws-resource-ec2-subnet"></a>

Specifies a subnet for the specified VPC\.

For an IPv4 only subnet, specify an IPv4 CIDR block\. If the VPC has an IPv6 CIDR block, you can create an IPv6 only subnet or a dual stack subnet instead\. For an IPv6 only subnet, specify an IPv6 CIDR block\. For a dual stack subnet, specify both an IPv4 CIDR block and an IPv6 CIDR block\.

For more information, see [Subnets for your VPC](https://docs.aws.amazon.com/vpc/latest/userguide/configure-subnets.html) in the *Amazon VPC User Guide*\.

## Syntax<a name="aws-resource-ec2-subnet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnet-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Subnet",
  "Properties" : {
      "[AssignIpv6AddressOnCreation](#cfn-ec2-subnet-assignipv6addressoncreation)" : Boolean,
      "[AvailabilityZone](#cfn-ec2-subnet-availabilityzone)" : String,
      "[AvailabilityZoneId](#cfn-ec2-subnet-availabilityzoneid)" : String,
      "[CidrBlock](#cfn-ec2-subnet-cidrblock)" : String,
      "[EnableDns64](#cfn-ec2-subnet-enabledns64)" : Boolean,
      "[Ipv6CidrBlock](#cfn-ec2-subnet-ipv6cidrblock)" : String,
      "[Ipv6Native](#cfn-ec2-subnet-ipv6native)" : Boolean,
      "[MapPublicIpOnLaunch](#cfn-ec2-subnet-mappubliciponlaunch)" : Boolean,
      "[OutpostArn](#cfn-ec2-subnet-outpostarn)" : String,
      "[PrivateDnsNameOptionsOnLaunch](#cfn-ec2-subnet-privatednsnameoptionsonlaunch)" : PrivateDnsNameOptionsOnLaunch,
      "[Tags](#cfn-ec2-subnet-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-ec2-subnet-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-subnet-syntax.yaml"></a>

```
Type: AWS::EC2::Subnet
Properties: 
  [AssignIpv6AddressOnCreation](#cfn-ec2-subnet-assignipv6addressoncreation): Boolean
  [AvailabilityZone](#cfn-ec2-subnet-availabilityzone): String
  [AvailabilityZoneId](#cfn-ec2-subnet-availabilityzoneid): String
  [CidrBlock](#cfn-ec2-subnet-cidrblock): String
  [EnableDns64](#cfn-ec2-subnet-enabledns64): Boolean
  [Ipv6CidrBlock](#cfn-ec2-subnet-ipv6cidrblock): String
  [Ipv6Native](#cfn-ec2-subnet-ipv6native): Boolean
  [MapPublicIpOnLaunch](#cfn-ec2-subnet-mappubliciponlaunch): Boolean
  [OutpostArn](#cfn-ec2-subnet-outpostarn): String
  [PrivateDnsNameOptionsOnLaunch](#cfn-ec2-subnet-privatednsnameoptionsonlaunch): 
    PrivateDnsNameOptionsOnLaunch
  [Tags](#cfn-ec2-subnet-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-ec2-subnet-vpcid): String
```

## Properties<a name="aws-resource-ec2-subnet-properties"></a>

`AssignIpv6AddressOnCreation`  <a name="cfn-ec2-subnet-assignipv6addressoncreation"></a>
Indicates whether a network interface created in this subnet receives an IPv6 address\. The default value is `false`\.  
If you specify `AssignIpv6AddressOnCreation`, you must also specify `Ipv6CidrBlock`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-subnet-availabilityzone"></a>
The Availability Zone of the subnet\.  
If you update this property, you must also update the `CidrBlock` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AvailabilityZoneId`  <a name="cfn-ec2-subnet-availabilityzoneid"></a>
The AZ ID of the subnet\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CidrBlock`  <a name="cfn-ec2-subnet-cidrblock"></a>
The IPv4 CIDR block assigned to the subnet\.  
If you update this property, we create a new subnet, and then delete the existing one\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableDns64`  <a name="cfn-ec2-subnet-enabledns64"></a>
Indicates whether DNS queries made to the Amazon\-provided DNS Resolver in this subnet should return synthetic IPv6 addresses for IPv4\-only destinations\. For more information, see [DNS64 and NAT64](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html#nat-gateway-nat64-dns64) in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ipv6CidrBlock`  <a name="cfn-ec2-subnet-ipv6cidrblock"></a>
The IPv6 CIDR block\.  
If you specify `AssignIpv6AddressOnCreation`, you must also specify `Ipv6CidrBlock`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Ipv6Native`  <a name="cfn-ec2-subnet-ipv6native"></a>
Indicates whether this is an IPv6 only subnet\. For more information, see [Subnet basics](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html#subnet-basics) in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MapPublicIpOnLaunch`  <a name="cfn-ec2-subnet-mappubliciponlaunch"></a>
Indicates whether instances launched in this subnet receive a public IPv4 address\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutpostArn`  <a name="cfn-ec2-subnet-outpostarn"></a>
The Amazon Resource Name \(ARN\) of the Outpost\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrivateDnsNameOptionsOnLaunch`  <a name="cfn-ec2-subnet-privatednsnameoptionsonlaunch"></a>
The hostname type for EC2 instances launched into this subnet and how DNS A and AAAA record queries to the instances should be handled\. For more information, see [Amazon EC2 instance hostname types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-naming.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Available options:  
+ EnableResourceNameDnsAAAARecord \(true \| false\)
+ EnableResourceNameDnsARecord \(true \| false\)
+ HostnameType \(ip\-name \| resource\-name\)
*Required*: No  
*Type*: [PrivateDnsNameOptionsOnLaunch](aws-properties-ec2-subnet-privatednsnameoptionsonlaunch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-subnet-tags"></a>
Any tags assigned to the subnet\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-subnet-vpcid"></a>
The ID of the VPC the subnet is in\.  
If you update this property, you must also update the `CidrBlock` property\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-subnet-return-values"></a>

### Ref<a name="aws-resource-ec2-subnet-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the subnet\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-subnet-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-subnet-return-values-fn--getatt-fn--getatt"></a>

`AvailabilityZone`  <a name="AvailabilityZone-fn::getatt"></a>
The Availability Zone of this subnet\. For example:  
 `{ "Fn::GetAtt" : [ "mySubnet", "AvailabilityZone" ] } ` 

`Ipv6CidrBlocks`  <a name="Ipv6CidrBlocks-fn::getatt"></a>
The IPv6 CIDR blocks that are associated with the subnet, such as `[ 2001:db8:1234:1a00::/64 ]`\.

`NetworkAclAssociationId`  <a name="NetworkAclAssociationId-fn::getatt"></a>
The ID of the network ACL that is associated with the subnet's VPC, such as `acl-5fb85d36`\.

`OutpostArn`  <a name="OutpostArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Outpost\.

`SubnetId`  <a name="SubnetId-fn::getatt"></a>
The ID of the subnet\.

`VpcId`  <a name="VpcId-fn::getatt"></a>
The ID of the subnet's VPC, such as `vpc-11ad4878`\.

## Examples<a name="aws-resource-ec2-subnet--examples"></a>



### Subnet<a name="aws-resource-ec2-subnet--examples--Subnet"></a>

The following example uses the VPC ID from a VPC named myVPC that was declared elsewhere in the same template\. For an example with IPv6 enabled, see [Creating an IPv6 enabled VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-cidr.html#intrinsic-function-reference-cidr-example2)\.

#### JSON<a name="aws-resource-ec2-subnet--examples--Subnet--json"></a>

```
"mySubnet" : {
   "Type" : "AWS::EC2::Subnet",
   "Properties" : {
      "VpcId" : { "Ref" : "myVPC" },
      "CidrBlock" : "10.0.0.0/24",
      "AvailabilityZone" : "us-east-1a",
      "Tags" : [ { "Key" : "stack", "Value" : "production" } ]
   }
}
```

#### YAML<a name="aws-resource-ec2-subnet--examples--Subnet--yaml"></a>

```
  mySubnet:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: myVPC
      CidrBlock: 10.0.0.0/24
      AvailabilityZone: "us-east-1a"
      Tags:
      - Key: stack
        Value: production
```

## See also<a name="aws-resource-ec2-subnet--seealso"></a>
+  [CreateSubnet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSubnet.html) in the *Amazon EC2 API Reference*
+  [VPC and subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) in the *Amazon VPC User Guide*


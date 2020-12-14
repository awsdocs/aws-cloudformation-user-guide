# AWS::EC2::Subnet<a name="aws-resource-ec2-subnet"></a>

Specifies a subnet for a VPC\.

When you create each subnet, you provide the VPC ID and IPv4 CIDR block for the subnet\. After you create a subnet, you can't change its CIDR block\. The size of the subnet's IPv4 CIDR block can be the same as a VPC's IPv4 CIDR block, or a subset of a VPC's IPv4 CIDR block\. If you create more than one subnet in a VPC, the subnets' CIDR blocks must not overlap\. The smallest IPv4 subnet \(and VPC\) you can create uses a /28 netmask \(16 IPv4 addresses\), and the largest uses a /16 netmask \(65,536 IPv4 addresses\)\.

If you've associated an IPv6 CIDR block with your VPC, you can create a subnet with an IPv6 CIDR block that uses a /64 prefix length\. 

## Syntax<a name="aws-resource-ec2-subnet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnet-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Subnet",
  "Properties" : {
      "[AssignIpv6AddressOnCreation](#cfn-ec2-subnet-assignipv6addressoncreation)" : Boolean,
      "[AvailabilityZone](#cfn-ec2-subnet-availabilityzone)" : String,
      "[CidrBlock](#cfn-ec2-subnet-cidrblock)" : String,
      "[Ipv6CidrBlock](#cfn-ec2-subnet-ipv6cidrblock)" : String,
      "[MapPublicIpOnLaunch](#cfn-ec2-subnet-mappubliciponlaunch)" : Boolean,
      "[OutpostArn](#cfn-ec2-subnet-outpostarn)" : String,
      "[Tags](#cfn-ec2-subnet-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-awsec2subnet-prop-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-subnet-syntax.yaml"></a>

```
Type: AWS::EC2::Subnet
Properties: 
  [AssignIpv6AddressOnCreation](#cfn-ec2-subnet-assignipv6addressoncreation): Boolean
  [AvailabilityZone](#cfn-ec2-subnet-availabilityzone): String
  [CidrBlock](#cfn-ec2-subnet-cidrblock): String
  [Ipv6CidrBlock](#cfn-ec2-subnet-ipv6cidrblock): String
  [MapPublicIpOnLaunch](#cfn-ec2-subnet-mappubliciponlaunch): Boolean
  [OutpostArn](#cfn-ec2-subnet-outpostarn): String
  [Tags](#cfn-ec2-subnet-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-awsec2subnet-prop-vpcid): String
```

## Properties<a name="aws-resource-ec2-subnet-properties"></a>

`AssignIpv6AddressOnCreation`  <a name="cfn-ec2-subnet-assignipv6addressoncreation"></a>
Indicates whether a network interface created in this subnet receives an IPv6 address\. The default value is `false`\.  
If you specify `AssignIpv6AddressOnCreation`, you must also specify `Ipv6CidrBlock`\.  
If you specify `AssignIpv6AddressOnCreation`, you cannot specify `MapPublicIpOnLaunch`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-subnet-availabilityzone"></a>
The Availability Zone of the subnet\.  
If you update this property, you must also update the `CidrBlock` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CidrBlock`  <a name="cfn-ec2-subnet-cidrblock"></a>
The IPv4 CIDR block assigned to the subnet\.  
If you update this property, you must also update the `AvailabilityZone` property\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ipv6CidrBlock`  <a name="cfn-ec2-subnet-ipv6cidrblock"></a>
The IPv6 CIDR block\.  
If you specify `AssignIpv6AddressOnCreation`, you must also specify `Ipv6CidrBlock`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapPublicIpOnLaunch`  <a name="cfn-ec2-subnet-mappubliciponlaunch"></a>
Indicates whether instances launched in this subnet receive a public IPv4 address\. The default value is `false`\.  
If you specify `MapPublicIpOnLaunch`, you cannot specify `AssignIpv6AddressOnCreation`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutpostArn`  <a name="cfn-ec2-subnet-outpostarn"></a>
The Amazon Resource Name \(ARN\) of the Outpost\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-subnet-tags"></a>
Any tags assigned to the subnet\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-awsec2subnet-prop-vpcid"></a>
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

`VpcId`  <a name="VpcId-fn::getatt"></a>
The ID of the subnet's VPC, such as `vpc-11ad4878`\.

## Examples<a name="aws-resource-ec2-subnet--examples"></a>



### Subnet<a name="aws-resource-ec2-subnet--examples--Subnet"></a>

The following example uses the VPC ID from a VPC named myVPC that was declared elsewhere in the same template\.

#### JSON<a name="aws-resource-ec2-subnet--examples--Subnet--json"></a>

```
"mySubnet" : {
   "Type" : "AWS::EC2::Subnet",
   "Properties" : {
      "VpcId" : { "Ref" : "myVPC" },
      "CidrBlock" : "10.0.0.0/24",
      "AvailabilityZone" : "us-east-1a",
      "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
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
      - Key: foo
        Value: bar
```

## See also<a name="aws-resource-ec2-subnet--seealso"></a>
+  [CreateSubnet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSubnet.html) in the *Amazon EC2 API Reference*
+  [Your VPC and Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) in the *Amazon Virtual Private Cloud User Guide*


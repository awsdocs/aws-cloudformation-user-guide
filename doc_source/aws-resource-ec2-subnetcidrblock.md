# AWS::EC2::SubnetCidrBlock<a name="aws-resource-ec2-subnetcidrblock"></a>

The `AWS::EC2::SubnetCidrBlock` resource associates a single IPv6 CIDR block with an Amazon VPC subnet\.

**Topics**
+ [Syntax](#aws-resource-ec2-subnetcidrblock-syntax)
+ [Properties](#w3ab2c21c10d488b9)
+ [Example](#w3ab2c21c10d488c11)

## Syntax<a name="aws-resource-ec2-subnetcidrblock-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnetcidrblock-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::SubnetCidrBlock",
   "Properties" : {
      "[Ipv6CidrBlock](#cfn-ec2-subnetcidrblock-ipv6cidrblock)" : String,
      "[SubnetId](#cfn-ec2-subnetcidrblock-subnetid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-subnetcidrblock-syntax.yaml"></a>

```
Type: "AWS::EC2::SubnetCidrBlock"
Properties: 
  [Ipv6CidrBlock](#cfn-ec2-subnetcidrblock-ipv6cidrblock): String
  [SubnetId](#cfn-ec2-subnetcidrblock-subnetid): String
```

## Properties<a name="w3ab2c21c10d488b9"></a>

`Ipv6CidrBlock`  <a name="cfn-ec2-subnetcidrblock-ipv6cidrblock"></a>
The IPv6 CIDR block for the subnet\. The CIDR block must have a prefix length of /64\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SubnetId`  <a name="cfn-ec2-subnetcidrblock-subnetid"></a>
The ID of the subnet to associate the IPv6 CIDR block with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Example<a name="w3ab2c21c10d488c11"></a>

The following example associates an IPv6 CIDR block \(with a prefix length of /64\) with the `Ipv6TestSubnet` subnet\.

### JSON<a name="aws-resource-ec2-subnetcidrblock-example.json"></a>

```
{
  "Ipv6TestSubnetCidrBlock": {
    "Type": "AWS::EC2::SubnetCidrBlock",
    "Properties": {
      "Ipv6CidrBlock": { "Ref" : "Ipv6SubnetCidrBlock" },
      "SubnetId": { "Ref" : "Ipv6TestSubnet" }
    }
  }
}
```

### YAML<a name="aws-resource-ec2-subnetcidrblock-example.yaml"></a>

```
Ipv6TestSubnetCidrBlock:
  Type: "AWS::EC2::SubnetCidrBlock"
  Properties:
    Ipv6CidrBlock: !Ref Ipv6SubnetCidrBlock
    SubnetId: !Ref Ipv6TestSubnet
```
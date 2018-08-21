# AWS::EC2::VPCCidrBlock<a name="aws-resource-ec2-vpccidrblock"></a>

The `AWS::EC2::VPCCidrBlock` resource associates a single Amazon\-provided IPv6 CIDR block or a single user\-specified IPv4 CIDR block with a Virtual Private Cloud \(VPC\)\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpccidrblock-syntax)
+ [Properties](#aws-resource-ec2-vpccidrblock-properties)
+ [Examples](#aws-resource-ec2-vpccidrblock-examples)

## Syntax<a name="aws-resource-ec2-vpccidrblock-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpccidrblock-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPCCidrBlock",
   "Properties" : {
      "[AmazonProvidedIpv6CidrBlock](#cfn-ec2-vpccidrblock-amazonprovidedipv6cidrblock)" : Boolean,
      "[CidrBlock](#cfn-ec2-vpccidrblock-cidrblock)" : String,
      "[VpcId](#cfn-ec2-vpccidrblock-vpcid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-vpccidrblock-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCCidrBlock"
Properties: 
  [AmazonProvidedIpv6CidrBlock](#cfn-ec2-vpccidrblock-amazonprovidedipv6cidrblock): Boolean
  [CidrBlock](#cfn-ec2-vpccidrblock-cidrblock): String
  [VpcId](#cfn-ec2-vpccidrblock-vpcid): String
```

## Properties<a name="aws-resource-ec2-vpccidrblock-properties"></a>

`AmazonProvidedIpv6CidrBlock`  <a name="cfn-ec2-vpccidrblock-amazonprovidedipv6cidrblock"></a>
Whether to request an Amazon\-provided IPv6 CIDR block with a /56 prefix length for the VPC\. You can't specify the range of IPv6 addresses or the size of the CIDR block\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CidrBlock`  <a name="cfn-ec2-vpccidrblock-cidrblock"></a>
An IPv4 CIDR block to associate with the VPC\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VpcId`  <a name="cfn-ec2-vpccidrblock-vpcid"></a>
The ID of the VPC to associate the Amazon\-provided IPv6 CIDR block with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Examples<a name="aws-resource-ec2-vpccidrblock-examples"></a>

### Associate an Amazon\-provided IPv6 CIDR block<a name="aws-resource-ec2-vpccidrblock-example1"></a>

The following snippet associates an Amazon\-provided IPv6 CIDR block \(with a prefix length of /56\) with the `TestVPCIpv6` VPC\.

#### JSON<a name="aws-resource-ec2-vpccidrblock-example1.json"></a>

```
{
  "Ipv6VPCCidrBlock": {
    "Type": "AWS::EC2::VPCCidrBlock",
    "Properties": {
      "AmazonProvidedIpv6CidrBlock": true,
      "VpcId": { "Ref" : "TestVPCIpv6" }
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-vpccidrblock-example1.yaml"></a>

```
Ipv6VPCCidrBlock:
  Type: "AWS::EC2::VPCCidrBlock"
  Properties:
    AmazonProvidedIpv6CidrBlock: true
    VpcId: !Ref TestVPCIpv6
```

### Associate an IPv4 CIDR block and Amazon\-provided IPv6 CIDR block<a name="aws-resource-ec2-vpccidrblock-example2"></a>

The following example associates an IPv4 CIDR block and an Amazon\-provided IPv6 CIDR block with a VPC\. It also outputs the list of IPv4 CIDR block association IDs and IPv6 CIDR blocks that are associated with the VPC\.

#### JSON<a name="aws-resource-ec2-vpccidrblock-example2.json"></a>

```
{
    "Resources": {
        "VPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": "10.0.0.0/24"
            }
        },
        "VpcCidrBlock": {
            "Type": "AWS::EC2::VPCCidrBlock",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": "192.0.0.0/24"
            }
        },
        "VpcCidrBlockIpv6": {
            "Type": "AWS::EC2::VPCCidrBlock",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                },
                "AmazonProvidedIpv6CidrBlock": true
            }
        }
    },
    "Outputs": {
        "VpcId": {
            "Value": {
                "Ref": "VPC"
            }
        },
        "PrimaryCidrBlock": {
            "Value": {
                "Fn::GetAtt": [
                    "VPC",
                    "CidrBlock"
                ]
            }
        },
        "Ipv6CidrBlock": {
            "Value": {
                "Fn::Select": [
                    0,
                    {
                        "Fn::GetAtt": [
                            "VPC",
                            "Ipv6CidrBlocks"
                        ]
                    }
                ]
            }
        },
        "CidrBlockAssociation": {
            "Value": {
                "Fn::Select": [
                    0,
                    {
                        "Fn::GetAtt": [
                            "VPC",
                            "CidrBlockAssociations"
                        ]
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ec2-vpccidrblock-example2.yaml"></a>

```
Resources:
  VPC:
    Type: "AWS::EC2::VPC"
    Properties:
      CidrBlock: 10.0.0.0/24
  VpcCidrBlock:
    Type: "AWS::EC2::VPCCidrBlock"
    Properties:
      VpcId: !Ref VPC
      CidrBlock: 192.0.0.0/24
  VpcCidrBlockIpv6:
    Type: "AWS::EC2::VPCCidrBlock"
    Properties:
      VpcId: !Ref VPC
      AmazonProvidedIpv6CidrBlock: true

Outputs:
  VpcId:
    Value: !Ref VPC
  PrimaryCidrBlock:
    Value: !GetAtt VPC.CidrBlock
  Ipv6CidrBlock:
    Value: !Select [ 0, !GetAtt VPC.Ipv6CidrBlocks ]
  CidrBlockAssociation:
    Value: !Select [ 0, !GetAtt VPC.CidrBlockAssociations ]
```
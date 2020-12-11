# AWS::EC2::VPCCidrBlock<a name="aws-resource-ec2-vpccidrblock"></a>

Associates a CIDR block with your VPC\. You can only associate a single IPv6 CIDR block with your VPC\. The IPv6 CIDR block size is fixed at /56\.

For more information about associating CIDR blocks with your VPC and applicable restrictions, see [VPC and Subnet Sizing](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html#VPC_Sizing) in the *Amazon Virtual Private Cloud User Guide*\.

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
Type: AWS::EC2::VPCCidrBlock
Properties: 
  [AmazonProvidedIpv6CidrBlock](#cfn-ec2-vpccidrblock-amazonprovidedipv6cidrblock): Boolean
  [CidrBlock](#cfn-ec2-vpccidrblock-cidrblock): String
  [VpcId](#cfn-ec2-vpccidrblock-vpcid): String
```

## Properties<a name="aws-resource-ec2-vpccidrblock-properties"></a>

`AmazonProvidedIpv6CidrBlock`  <a name="cfn-ec2-vpccidrblock-amazonprovidedipv6cidrblock"></a>
Requests an Amazon\-provided IPv6 CIDR block with a /56 prefix length for the VPC\. You cannot specify the range of IPv6 addresses, or the size of the CIDR block\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CidrBlock`  <a name="cfn-ec2-vpccidrblock-cidrblock"></a>
An IPv4 CIDR block to associate with the VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-ec2-vpccidrblock-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpccidrblock-return-values"></a>

### Ref<a name="aws-resource-ec2-vpccidrblock-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the association ID for the VPC CIDR block\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-vpccidrblock--examples"></a>



### Associate an Amazon\-provided IPv6 CIDR block<a name="aws-resource-ec2-vpccidrblock--examples--Associate_an_Amazon-provided_IPv6_CIDR_block"></a>

The following example associates an Amazon\-provided IPv6 CIDR block \(with a prefix length of /56\) with the TestVPCIpv6 VPC\. 

#### JSON<a name="aws-resource-ec2-vpccidrblock--examples--Associate_an_Amazon-provided_IPv6_CIDR_block--json"></a>

```
"Ipv6VPCCidrBlock": {
   "Type": "AWS::EC2::VPCCidrBlock",
   "Properties": {
      "AmazonProvidedIpv6CidrBlock": true,
      "VpcId": { "Ref" : "TestVPCIpv6" }
   }
}
```

#### YAML<a name="aws-resource-ec2-vpccidrblock--examples--Associate_an_Amazon-provided_IPv6_CIDR_block--yaml"></a>

```
Ipv6VPCCidrBlock:
   Type: AWS::EC2::VPCCidrBlock
   Properties:
      AmazonProvidedIpv6CidrBlock: true
      VpcId: !Ref TestVPCIpv6
```

### Associate an IPv4 CIDR block and Amazon\-provided IPv6 CIDR block<a name="aws-resource-ec2-vpccidrblock--examples--Associate_an_IPv4_CIDR_block_and_Amazon-provided_IPv6_CIDR_block"></a>

The following example associates an IPv4 CIDR block and an Amazon\-provided IPv6 CIDR block with a VPC\. It also outputs the list of IPv4 CIDR block association IDs and IPv6 CIDR blocks that are associated with the VPC\. 

#### JSON<a name="aws-resource-ec2-vpccidrblock--examples--Associate_an_IPv4_CIDR_block_and_Amazon-provided_IPv6_CIDR_block--json"></a>

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

#### YAML<a name="aws-resource-ec2-vpccidrblock--examples--Associate_an_IPv4_CIDR_block_and_Amazon-provided_IPv6_CIDR_block--yaml"></a>

```
Resources:
  VPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/24
  VpcCidrBlock:
    Type: AWS::EC2::VPCCidrBlock
    Properties:
      VpcId: !Ref VPC
      CidrBlock: 192.0.0.0/24
  VpcCidrBlockIpv6:
    Type: AWS::EC2::VPCCidrBlock
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
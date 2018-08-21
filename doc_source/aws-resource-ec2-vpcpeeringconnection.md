# AWS::EC2::VPCPeeringConnection<a name="aws-resource-ec2-vpcpeeringconnection"></a>

A VPC peering connection enables a network connection between two virtual private clouds \(VPCs\) so that you can route traffic between them using a private IP address\. For more information about VPC peering and its limitations, see [VPC Peering Overview](http://docs.aws.amazon.com/AmazonVPC/latest/PeeringGuide/vpc-peering-overview.html) in the *Amazon VPC Peering Guide*\. 

**Note**  
You can create a peering connection with another AWS account\. For a detailed walkthrough, see [Walkthrough: Peer with an Amazon VPC in Another AWS Account](peer-with-vpc-in-another-account.md)\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcpeeringconnection-syntax)
+ [Properties](#w3ab2c21c10d531c10)
+ [Return Values](#w3ab2c21c10d531c12)
+ [Examples](#w3ab2c21c10d531c14)

## Syntax<a name="aws-resource-ec2-vpcpeeringconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcpeeringconnection-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPCPeeringConnection",
   "Properties" : {
      "[PeerVpcId](#cfn-ec2-vpcpeeringconnection-peervpcid)" : String,
      "[Tags](#cfn-ec2-vpcpeeringconnection-tags)" : [ Resource Tag, ... ],
      "[VpcId](#cfn-ec2-vpcpeeringconnection-vpcid)" : String,
      "[PeerOwnerId](#cfn-ec2-vpcpeeringconnection-peerownerid)" : String,
      "[PeerRoleArn](#cfn-ec2-vpcpeeringconnection-peerrolearn)" :  String
   }
}
```

### YAML<a name="aws-resource-ec2-vpcpeeringconnection-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCPeeringConnection"
Properties: 
  [PeerVpcId](#cfn-ec2-vpcpeeringconnection-peervpcid): String
  [Tags](#cfn-ec2-vpcpeeringconnection-tags):
    - Resource Tag
  [VpcId](#cfn-ec2-vpcpeeringconnection-vpcid): String
  [PeerOwnerId](#cfn-ec2-vpcpeeringconnection-peerownerid): String
  [PeerRoleArn](#cfn-ec2-vpcpeeringconnection-peerrolearn):  String
```

## Properties<a name="w3ab2c21c10d531c10"></a>

`PeerVpcId`  <a name="cfn-ec2-vpcpeeringconnection-peervpcid"></a>
The ID of the VPC with which you are creating the peering connection\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-ec2-vpcpeeringconnection-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this resource\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`VpcId`  <a name="cfn-ec2-vpcpeeringconnection-vpcid"></a>
The ID of the VPC that is requesting a peering connection\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PeerOwnerId`  <a name="cfn-ec2-vpcpeeringconnection-peerownerid"></a>
The AWS account ID of the owner of the VPC that you want to peer with\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PeerRoleArn`  <a name="cfn-ec2-vpcpeeringconnection-peerrolearn"></a>
The Amazon Resource Name \(ARN\) of the VPC peer role for the peering connection in another AWS account\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d531c12"></a>

### Ref<a name="w3ab2c21c10d531c12b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d531c14"></a>

The following example template creates two VPCs to demonstrate how to configure a peering connection\. For a VPC peering connection, you must create a VPC peering route for each VPC route table, as shown in the example by `PeeringRoute1` and `PeeringRoute2`\. If you launch the template, you can connect to the `myInstance` instance using SSH, and then ping the `myPrivateInstance` instance although both instances are in separate VPCs\.

### JSON<a name="aws-resource-ec2-vpcpeeringconnection-example-1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Creates a VPC that and then creates a peering connection with an existing VPC that you specify.",
    "Parameters": {
        "EC2KeyPairName": {
            "Description": "Name of an existing EC2 KeyPair to enable SSH access to the instances",
            "Type": "AWS::EC2::KeyPair::KeyName",
            "ConstraintDescription" : "must be the name of an existing EC2 KeyPair."
        },
        "InstanceType": {
            "Description": "EC2 instance type",
            "Type": "String",
            "Default": "t1.micro",
            "AllowedValues": [
                "t1.micro",
                "m1.small",
                "m3.medium",
                "m3.large",
                "m3.xlarge",
                "m3.2xlarge",
                "c3.large",
                "c3.xlarge",
                "c3.2xlarge",
                "c3.4xlarge",
                "c3.8xlarge"
            ],
            "ConstraintDescription": "must be a valid EC2 instance type."
        },
        "myVPCIDCIDRRange": {
            "Description": "The IP address range for your new VPC.",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "10.1.0.0/16",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
        },
        "myPrivateVPCIDCIDRRange": {
            "Description": "The IP address range for your new Private VPC.",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "10.0.0.0/16",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
        },
        "EC2SubnetCIDRRange": {
            "Description": "The IP address range for a subnet in myPrivateVPC.",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "10.0.0.0/24",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
        },
        "EC2PublicSubnetCIDRRange": {
            "Description": "The IP address range for a subnet in myVPC.",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "10.1.0.0/24",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
        }
    },
    "Mappings": {
        "AWSRegionToAMI": {
            "us-east-1": {
                "64": "ami-fb8e9292"
            },
            "us-west-2": {
                "64": "ami-043a5034"
            },
            "us-west-1": {
                "64": "ami-7aba833f"
            },
            "eu-west-1": {
                "64": "ami-2918e35e"
            },
            "ap-southeast-1": {
                "64": "ami-b40d5ee6"
            },
            "ap-southeast-2": {
                "64": "ami-3b4bd301"
            },
            "ap-northeast-1": {
                "64": "ami-c9562fc8"
            },
            "sa-east-1": {
                "64": "ami-215dff3c"
            }
        }
    },
    "Resources": {
        "myPrivateVPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": {"Ref": "myPrivateVPCIDCIDRRange"},
                "EnableDnsSupport": false,
                "EnableDnsHostnames": false,
                "InstanceTenancy": "default"
            }
        },        
        "myPrivateEC2Subnet" : {
            "Type" : "AWS::EC2::Subnet",
            "Properties" : {
                "VpcId" : { "Ref" : "myPrivateVPC" },
                "CidrBlock" : {"Ref": "EC2SubnetCIDRRange"}
            }
        },
        "RouteTable" : {
            "Type" : "AWS::EC2::RouteTable",
            "Properties" : {
                "VpcId" : {"Ref" : "myPrivateVPC"}            
            }
        },        
        "PeeringRoute1" : {
            "Type" : "AWS::EC2::Route",
            "Properties" : {
                "DestinationCidrBlock": "0.0.0.0/0",
                "RouteTableId" : { "Ref" : "RouteTable" },
                "VpcPeeringConnectionId" : { "Ref" : "myVPCPeeringConnection" }
            }
        },
        "SubnetRouteTableAssociation" : {
            "Type" : "AWS::EC2::SubnetRouteTableAssociation",
            "Properties" : {
                "SubnetId" : { "Ref" : "myPrivateEC2Subnet" },
                "RouteTableId" : { "Ref" : "RouteTable" }
            }
        },
        "myVPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": {"Ref": "myVPCIDCIDRRange"},
                "EnableDnsSupport": true,
                "EnableDnsHostnames": true,
                "InstanceTenancy": "default"
            }
        },        
        "PublicSubnet": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "CidrBlock": {"Ref": "EC2PublicSubnetCIDRRange"},
                "VpcId": {
                    "Ref": "myVPC"
                }
            }
        },
        "myInternetGateway": {
            "Type": "AWS::EC2::InternetGateway"
        },
        "AttachGateway": {
            "Type": "AWS::EC2::VPCGatewayAttachment",
            "Properties": {
                "VpcId": {
                    "Ref": "myVPC"
                },
                "InternetGatewayId": {
                    "Ref": "myInternetGateway"
                }
            }
        },
        "PublicRouteTable": {
            "Type": "AWS::EC2::RouteTable",
            "Properties": {
                "VpcId": {
                    "Ref": "myVPC"
                }
            }
        },
        "PeeringRoute2" : {
            "Type" : "AWS::EC2::Route",
            "Properties" : {
                "DestinationCidrBlock": { "Ref" : "myPrivateVPCIDCIDRRange" },
                "RouteTableId" : { "Ref" : "PublicRouteTable" },
                "VpcPeeringConnectionId" : { "Ref" : "myVPCPeeringConnection" }
            }
        },
        "PublicRoute": {
            "Type": "AWS::EC2::Route",
            "DependsOn": "AttachGateway",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PublicRouteTable"
                },
                "DestinationCidrBlock": "0.0.0.0/0",
                "GatewayId": {
                    "Ref": "myInternetGateway"
                }
            }
        },
        "PublicSubnetRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "SubnetId": {
                    "Ref": "PublicSubnet"
                },
                "RouteTableId": {
                    "Ref": "PublicRouteTable"
                }
            }
        },
        "myPrivateVPCEC2SecurityGroup" : {
            "Type" : "AWS::EC2::SecurityGroup",
            "Properties" : {
                "GroupDescription": "Private instance security group",
                "VpcId" : { "Ref" : "myPrivateVPC" },
                "SecurityGroupIngress" : [
                    {"IpProtocol" : "-1", "FromPort" : "0", "ToPort" : "65535", "CidrIp" : "0.0.0.0/0"}
                ]
            }
        },
        "myVPCEC2SecurityGroup" : {
            "Type" : "AWS::EC2::SecurityGroup",
            "Properties" : {
                "GroupDescription": "Public instance security group",
                "VpcId" : { "Ref" : "myVPC" },
                "SecurityGroupIngress" : [
                    {"IpProtocol" : "tcp", "FromPort" : "80", "ToPort" : "80", "CidrIp" : "0.0.0.0/0"},
                    {"IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : "0.0.0.0/0"}
                ]
            }
        },
        "myPrivateInstance" : {
            "Type" : "AWS::EC2::Instance",
            "Properties" : {
                "SecurityGroupIds" : [{ "Ref" : "myPrivateVPCEC2SecurityGroup" }],
                "SubnetId" : { "Ref" : "myPrivateEC2Subnet" },
                "KeyName": {
                    "Ref": "EC2KeyPairName"
                },
                "ImageId": {
                    "Fn::FindInMap": [
                        "AWSRegionToAMI",
                        {"Ref": "AWS::Region"},
                        "64"
                    ]
                }
            }
        },
        "myInstance" : {
            "Type" : "AWS::EC2::Instance",
            "Properties" : {
                "NetworkInterfaces": [ {
                    "AssociatePublicIpAddress": "true",
                    "DeviceIndex": "0",
                    "GroupSet": [{ "Ref" : "myVPCEC2SecurityGroup" }],
                    "SubnetId": { "Ref" : "PublicSubnet" }
                } ],
                "KeyName": {
                    "Ref": "EC2KeyPairName"
                },
                "ImageId": {
                    "Fn::FindInMap": [
                        "AWSRegionToAMI",
                        {"Ref": "AWS::Region"},
                        "64"
                    ]
                }
            }
        },
        "myVPCPeeringConnection": {
            "Type": "AWS::EC2::VPCPeeringConnection",
            "Properties": {
                "VpcId": {"Ref": "myVPC"},
                "PeerVpcId": {"Ref": "myPrivateVPC"}
            }
        }
    }
}
```

### YAML<a name="aws-resource-ec2-vpcpeeringconnection-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Creates a VPC that and then creates a peering connection with an existing
  VPC that you specify.
Parameters:
  EC2KeyPairName:
    Description: Name of an existing EC2 KeyPair to enable SSH access to the instances
    Type: AWS::EC2::KeyPair::KeyName
    ConstraintDescription: must be the name of an existing EC2 KeyPair.
  InstanceType:
    Description: EC2 instance type
    Type: String
    Default: t1.micro
    AllowedValues:
    - t1.micro
    - m1.small
    - m3.medium
    - m3.large
    - m3.xlarge
    - m3.2xlarge
    - c3.large
    - c3.xlarge
    - c3.2xlarge
    - c3.4xlarge
    - c3.8xlarge
    ConstraintDescription: must be a valid EC2 instance type.
  myVPCIDCIDRRange:
    Description: The IP address range for your new VPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.1.0.0/16
    AllowedPattern: "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})"
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  myPrivateVPCIDCIDRRange:
    Description: The IP address range for your new Private VPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.0.0.0/16
    AllowedPattern: "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})"
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  EC2SubnetCIDRRange:
    Description: The IP address range for a subnet in myPrivateVPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.0.0.0/24
    AllowedPattern: "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})"
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  EC2PublicSubnetCIDRRange:
    Description: The IP address range for a subnet in myVPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.1.0.0/24
    AllowedPattern: "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})"
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
Mappings:
  AWSRegionToAMI:
    us-east-1:
      '64': ami-fb8e9292
    us-west-2:
      '64': ami-043a5034
    us-west-1:
      '64': ami-7aba833f
    eu-west-1:
      '64': ami-2918e35e
    ap-southeast-1:
      '64': ami-b40d5ee6
    ap-southeast-2:
      '64': ami-3b4bd301
    ap-northeast-1:
      '64': ami-c9562fc8
    sa-east-1:
      '64': ami-215dff3c
Resources:
  myPrivateVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock:
        Ref: myPrivateVPCIDCIDRRange
      EnableDnsSupport: false
      EnableDnsHostnames: false
      InstanceTenancy: default
  myPrivateEC2Subnet:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: myPrivateVPC
      CidrBlock:
        Ref: EC2SubnetCIDRRange
  RouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId:
        Ref: myPrivateVPC
  PeeringRoute1:
    Type: AWS::EC2::Route
    Properties:
      DestinationCidrBlock: 0.0.0.0/0
      RouteTableId:
        Ref: RouteTable
      VpcPeeringConnectionId:
        Ref: myVPCPeeringConnection
  SubnetRouteTableAssociation:
    Type: AWS::EC2::SubnetRouteTableAssociation
    Properties:
      SubnetId:
        Ref: myPrivateEC2Subnet
      RouteTableId:
        Ref: RouteTable
  myVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock:
        Ref: myVPCIDCIDRRange
      EnableDnsSupport: true
      EnableDnsHostnames: true
      InstanceTenancy: default
  PublicSubnet:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock:
        Ref: EC2PublicSubnetCIDRRange
      VpcId:
        Ref: myVPC
  myInternetGateway:
    Type: AWS::EC2::InternetGateway
  AttachGateway:
    Type: AWS::EC2::VPCGatewayAttachment
    Properties:
      VpcId:
        Ref: myVPC
      InternetGatewayId:
        Ref: myInternetGateway
  PublicRouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId:
        Ref: myVPC
  PeeringRoute2:
    Type: AWS::EC2::Route
    Properties:
      DestinationCidrBlock:
        Ref: myPrivateVPCIDCIDRRange
      RouteTableId:
        Ref: PublicRouteTable
      VpcPeeringConnectionId:
        Ref: myVPCPeeringConnection
  PublicRoute:
    Type: AWS::EC2::Route
    DependsOn: AttachGateway
    Properties:
      RouteTableId:
        Ref: PublicRouteTable
      DestinationCidrBlock: 0.0.0.0/0
      GatewayId:
        Ref: myInternetGateway
  PublicSubnetRouteTableAssociation:
    Type: AWS::EC2::SubnetRouteTableAssociation
    Properties:
      SubnetId:
        Ref: PublicSubnet
      RouteTableId:
        Ref: PublicRouteTable
  myPrivateVPCEC2SecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Private instance security group
      VpcId:
        Ref: myPrivateVPC
      SecurityGroupIngress:
      - IpProtocol: "-1"
        FromPort: '0'
        ToPort: '65535'
        CidrIp: 0.0.0.0/0
  myVPCEC2SecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Public instance security group
      VpcId:
        Ref: myVPC
      SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: '80'
        ToPort: '80'
        CidrIp: 0.0.0.0/0
      - IpProtocol: tcp
        FromPort: '22'
        ToPort: '22'
        CidrIp: 0.0.0.0/0
  myPrivateInstance:
    Type: AWS::EC2::Instance
    Properties:
      SecurityGroupIds:
      - Ref: myPrivateVPCEC2SecurityGroup
      SubnetId:
        Ref: myPrivateEC2Subnet
      KeyName:
        Ref: EC2KeyPairName
      ImageId:
        Fn::FindInMap:
        - AWSRegionToAMI
        - Ref: AWS::Region
        - '64'
  myInstance:
    Type: AWS::EC2::Instance
    Properties:
      NetworkInterfaces:
      - AssociatePublicIpAddress: 'true'
        DeviceIndex: '0'
        GroupSet:
        - Ref: myVPCEC2SecurityGroup
        SubnetId:
          Ref: PublicSubnet
      KeyName:
        Ref: EC2KeyPairName
      ImageId:
        Fn::FindInMap:
        - AWSRegionToAMI
        - Ref: AWS::Region
        - '64'
  myVPCPeeringConnection:
    Type: AWS::EC2::VPCPeeringConnection
    Properties:
      VpcId:
        Ref: myVPC
      PeerVpcId:
        Ref: myPrivateVPC
```
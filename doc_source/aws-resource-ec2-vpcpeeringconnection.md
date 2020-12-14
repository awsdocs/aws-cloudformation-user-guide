# AWS::EC2::VPCPeeringConnection<a name="aws-resource-ec2-vpcpeeringconnection"></a>

Requests a VPC peering connection between two VPCs: a requester VPC that you own and an accepter VPC with which to create the connection\. The accepter VPC can belong to another AWS account and can be in a different Region to the requester VPC\. The requester VPC and accepter VPC cannot have overlapping CIDR blocks\.

**Note**  
Limitations and rules apply to a VPC peering connection\. For more information, see the [limitations](https://docs.aws.amazon.com/vpc/latest/peering/vpc-peering-basics.html#vpc-peering-limitations) section in the *VPC Peering Guide*\.

The owner of the accepter VPC must accept the peering request to activate the peering connection\. The VPC peering connection request expires after 7 days, after which it cannot be accepted or rejected\.

If you create a VPC peering connection request between VPCs with overlapping CIDR blocks, the VPC peering connection has a status of `failed`\.

## Syntax<a name="aws-resource-ec2-vpcpeeringconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcpeeringconnection-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCPeeringConnection",
  "Properties" : {
      "[PeerOwnerId](#cfn-ec2-vpcpeeringconnection-peerownerid)" : String,
      "[PeerRegion](#cfn-ec2-vpcpeeringconnection-peerregion)" : String,
      "[PeerRoleArn](#cfn-ec2-vpcpeeringconnection-peerrolearn)" : String,
      "[PeerVpcId](#cfn-ec2-vpcpeeringconnection-peervpcid)" : String,
      "[Tags](#cfn-ec2-vpcpeeringconnection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-ec2-vpcpeeringconnection-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpcpeeringconnection-syntax.yaml"></a>

```
Type: AWS::EC2::VPCPeeringConnection
Properties: 
  [PeerOwnerId](#cfn-ec2-vpcpeeringconnection-peerownerid): String
  [PeerRegion](#cfn-ec2-vpcpeeringconnection-peerregion): String
  [PeerRoleArn](#cfn-ec2-vpcpeeringconnection-peerrolearn): String
  [PeerVpcId](#cfn-ec2-vpcpeeringconnection-peervpcid): String
  [Tags](#cfn-ec2-vpcpeeringconnection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-ec2-vpcpeeringconnection-vpcid): String
```

## Properties<a name="aws-resource-ec2-vpcpeeringconnection-properties"></a>

`PeerOwnerId`  <a name="cfn-ec2-vpcpeeringconnection-peerownerid"></a>
The AWS account ID of the owner of the accepter VPC\.  
Default: Your AWS account ID  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerRegion`  <a name="cfn-ec2-vpcpeeringconnection-peerregion"></a>
The Region code for the accepter VPC, if the accepter VPC is located in a Region other than the Region in which you make the request\.  
Default: The Region in which you make the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerRoleArn`  <a name="cfn-ec2-vpcpeeringconnection-peerrolearn"></a>
The Amazon Resource Name \(ARN\) of the VPC peer role for the peering connection in another AWS account\.  
This is required when you are peering a VPC in a different AWS account\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerVpcId`  <a name="cfn-ec2-vpcpeeringconnection-peervpcid"></a>
The ID of the VPC with which you are creating the VPC peering connection\. You must specify this parameter in the request\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-vpcpeeringconnection-tags"></a>
Any tags assigned to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-vpcpeeringconnection-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpcpeeringconnection-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcpeeringconnection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC peering connection\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-vpcpeeringconnection--examples"></a>



### VPC Peering Connection<a name="aws-resource-ec2-vpcpeeringconnection--examples--VPC_Peering_Connection"></a>

The following example creates two VPCs \(`myVPC` and `myPrivateVPC`\) and a subnet in each VPC\. The subnet in `myVPC` is a public subnet\. The example then creates a VPC peering connection between the VPCs and launches an instance in each VPC\. You can test the peering connection by connecting to the instance in the public subnet and pinging the private IP address of the instance in the subnet of the private VPC\. The security group rules for the instance in the private subnet allow incoming ICMP traffic \(and therefore allow the `ping` command\)\.

#### JSON<a name="aws-resource-ec2-vpcpeeringconnection--examples--VPC_Peering_Connection--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Description": "Creates two VPCs, peers the VPCs, and launches an instance in each VPC.",
   "Parameters": {
      "EC2KeyPairName": {
         "Description": "Name of an existing EC2 KeyPair to enable SSH access to the instances",
         "Type": "AWS::EC2::KeyPair::KeyName",
         "ConstraintDescription" : "must be the name of an existing EC2 KeyPair."
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
              "64": "ami-0ff8a91507f77f867"
          },
          "us-west-2": {
             "64": "ami-a0cfeed8"
          },
          "us-west-1": {
              "64": "ami-0bdb828fd58c52235"
          },
          "eu-west-1": {
              "64": "ami-047bb4163c506cd98"
          },
          "ap-southeast-1": {
              "64": "ami-08569b978cc4dfa10"
          },
          "ap-southeast-2": {
              "64": "ami-09b42976632b27e9b"
          },
          "ap-northeast-2": {
              "64": "ami-0d097db2fb6e0f05e"
          },
          "ap-northeast-1": {
              "64": "ami-06cd52961ce9f0d85"
          },
          "sa-east-1": {
              "64": "ami-07b14488da8ea02a0"
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
                 {"IpProtocol" : "icmp", "FromPort" : "-1", "ToPort" : "-1", "CidrIp" : "0.0.0.0/0"}
              ]
         }
     },
     "myVPCEC2SecurityGroup" : {
        "Type" : "AWS::EC2::SecurityGroup",
        "Properties" : {
            "GroupDescription": "Public instance security group",
            "VpcId" : { "Ref" : "myVPC" },
            "SecurityGroupIngress" : [
                {"IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : "0.0.0.0/0"}
            ]
        }
     },
     "myPrivateInstance" : {
         "Type" : "AWS::EC2::Instance",
         "Properties" : {
            "SecurityGroupIds" : [{ "Ref" : "myPrivateVPCEC2SecurityGroup" }],
            "InstanceType" : "t2.micro",
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
            "InstanceType" : "t2.micro",
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

#### YAML<a name="aws-resource-ec2-vpcpeeringconnection--examples--VPC_Peering_Connection--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'Creates two VPCs, peers the VPCs, and launches an instance in each VPC.'
Parameters:
  EC2KeyPairName:
    Description: Name of an existing EC2 KeyPair to enable SSH access to the instances
    Type: 'AWS::EC2::KeyPair::KeyName'
    ConstraintDescription: must be the name of an existing EC2 KeyPair.
  myVPCIDCIDRRange:
    Description: The IP address range for your new VPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.1.0.0/16
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  myPrivateVPCIDCIDRRange:
    Description: The IP address range for your new Private VPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.0.0.0/16
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  EC2SubnetCIDRRange:
    Description: The IP address range for a subnet in myPrivateVPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.0.0.0/24
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  EC2PublicSubnetCIDRRange:
    Description: The IP address range for a subnet in myVPC.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 10.1.0.0/24
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
Mappings:
  AWSRegionToAMI:
    us-east-1:
      '64': ami-0ff8a91507f77f867
    us-west-2:
      '64': ami-a0cfeed8
    us-west-1:
      '64': ami-0bdb828fd58c52235
    eu-west-1:
      '64': ami-047bb4163c506cd98
    ap-southeast-1:
      '64': ami-08569b978cc4dfa10
    ap-southeast-2:
      '64': ami-09b42976632b27e9b
    ap-northeast-2:
      '64': ami-0d097db2fb6e0f05e
    ap-northeast-1:
      '64': ami-06cd52961ce9f0d85
    sa-east-1:
      '64': ami-07b14488da8ea02a0
Resources:
  myPrivateVPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref myPrivateVPCIDCIDRRange
      EnableDnsSupport: false
      EnableDnsHostnames: false
      InstanceTenancy: default
  myPrivateEC2Subnet:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref myPrivateVPC
      CidrBlock: !Ref EC2SubnetCIDRRange
  RouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref myPrivateVPC
  PeeringRoute1:
    Type: 'AWS::EC2::Route'
    Properties:
      DestinationCidrBlock: 0.0.0.0/0
      RouteTableId: !Ref RouteTable
      VpcPeeringConnectionId: !Ref myVPCPeeringConnection
  SubnetRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      SubnetId: !Ref myPrivateEC2Subnet
      RouteTableId: !Ref RouteTable
  myVPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref myVPCIDCIDRRange
      EnableDnsSupport: true
      EnableDnsHostnames: true
      InstanceTenancy: default
  PublicSubnet:
    Type: 'AWS::EC2::Subnet'
    Properties:
      CidrBlock: !Ref EC2PublicSubnetCIDRRange
      VpcId: !Ref myVPC
  myInternetGateway:
    Type: 'AWS::EC2::InternetGateway'
  AttachGateway:
    Type: 'AWS::EC2::VPCGatewayAttachment'
    Properties:
      VpcId: !Ref myVPC
      InternetGatewayId: !Ref myInternetGateway
  PublicRouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref myVPC
  PeeringRoute2:
    Type: 'AWS::EC2::Route'
    Properties:
      DestinationCidrBlock: !Ref myPrivateVPCIDCIDRRange
      RouteTableId: !Ref PublicRouteTable
      VpcPeeringConnectionId: !Ref myVPCPeeringConnection
  PublicRoute:
    Type: 'AWS::EC2::Route'
    DependsOn: AttachGateway
    Properties:
      RouteTableId: !Ref PublicRouteTable
      DestinationCidrBlock: 0.0.0.0/0
      GatewayId: !Ref myInternetGateway
  PublicSubnetRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      SubnetId: !Ref PublicSubnet
      RouteTableId: !Ref PublicRouteTable
  myPrivateVPCEC2SecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Private instance security group
      VpcId: !Ref myPrivateVPC
      SecurityGroupIngress:
        - IpProtocol: icmp
          FromPort: '-1'
          ToPort: '-1'
          CidrIp: 0.0.0.0/0
  myVPCEC2SecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Public instance security group
      VpcId: !Ref myVPC
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '22'
          ToPort: '22'
          CidrIp: 0.0.0.0/0
  myPrivateInstance:
    Type: 'AWS::EC2::Instance'
    Properties:
      SecurityGroupIds:
        - !Ref myPrivateVPCEC2SecurityGroup
      InstanceType: t2.micro
      SubnetId: !Ref myPrivateEC2Subnet
      KeyName: !Ref EC2KeyPairName
      ImageId: !FindInMap 
        - AWSRegionToAMI
        - !Ref 'AWS::Region'
        - '64'
  myInstance:
    Type: 'AWS::EC2::Instance'
    Properties:
      NetworkInterfaces:
        - AssociatePublicIpAddress: 'true'
          DeviceIndex: '0'
          GroupSet:
            - !Ref myVPCEC2SecurityGroup
          SubnetId: !Ref PublicSubnet
      InstanceType: t2.micro
      KeyName: !Ref EC2KeyPairName
      ImageId: !FindInMap 
        - AWSRegionToAMI
        - !Ref 'AWS::Region'
        - '64'
  myVPCPeeringConnection:
    Type: 'AWS::EC2::VPCPeeringConnection'
    Properties:
      VpcId: !Ref myVPC
      PeerVpcId: !Ref myPrivateVPC
```

## See also<a name="aws-resource-ec2-vpcpeeringconnection--seealso"></a>
+ [What is VPC peering](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html) in *AWS Outposts User Guide*
+ [CreateVpcPeeringConnection](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpcPeeringConnection.html) in the *Amazon EC2 API Reference*


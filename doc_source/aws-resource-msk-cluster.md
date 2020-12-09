# AWS::MSK::Cluster<a name="aws-resource-msk-cluster"></a>

The `AWS::MSK::Cluster` resource creates an Amazon MSK cluster\. For more information, see [What Is Amazon MSK?](https://docs.aws.amazon.com/msk/latest/developerguide/what-is-msk.html) in the *Amazon MSK Developer Guide*\.

## Syntax<a name="aws-resource-msk-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::Cluster",
  "Properties" : {
      "[BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo)" : BrokerNodeGroupInfo,
      "[ClientAuthentication](#cfn-msk-cluster-clientauthentication)" : ClientAuthentication,
      "[ClusterName](#cfn-msk-cluster-clustername)" : String,
      "[ConfigurationInfo](#cfn-msk-cluster-configurationinfo)" : ConfigurationInfo,
      "[EncryptionInfo](#cfn-msk-cluster-encryptioninfo)" : EncryptionInfo,
      "[EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring)" : String,
      "[KafkaVersion](#cfn-msk-cluster-kafkaversion)" : String,
      "[LoggingInfo](#cfn-msk-cluster-logginginfo)" : LoggingInfo,
      "[NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes)" : Integer,
      "[OpenMonitoring](#cfn-msk-cluster-openmonitoring)" : OpenMonitoring,
      "[Tags](#cfn-msk-cluster-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-msk-cluster-syntax.yaml"></a>

```
Type: AWS::MSK::Cluster
Properties: 
  [BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo): 
    BrokerNodeGroupInfo
  [ClientAuthentication](#cfn-msk-cluster-clientauthentication): 
    ClientAuthentication
  [ClusterName](#cfn-msk-cluster-clustername): String
  [ConfigurationInfo](#cfn-msk-cluster-configurationinfo): 
    ConfigurationInfo
  [EncryptionInfo](#cfn-msk-cluster-encryptioninfo): 
    EncryptionInfo
  [EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring): String
  [KafkaVersion](#cfn-msk-cluster-kafkaversion): String
  [LoggingInfo](#cfn-msk-cluster-logginginfo): 
    LoggingInfo
  [NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes): Integer
  [OpenMonitoring](#cfn-msk-cluster-openmonitoring): 
    OpenMonitoring
  [Tags](#cfn-msk-cluster-tags): Json
```

## Properties<a name="aws-resource-msk-cluster-properties"></a>

`BrokerNodeGroupInfo`  <a name="cfn-msk-cluster-brokernodegroupinfo"></a>
The setup to be used for brokers in the cluster\.  
*Required*: Yes  
*Type*: [BrokerNodeGroupInfo](aws-properties-msk-cluster-brokernodegroupinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientAuthentication`  <a name="cfn-msk-cluster-clientauthentication"></a>
Includes information related to client authentication\.  
*Required*: No  
*Type*: [ClientAuthentication](aws-properties-msk-cluster-clientauthentication.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterName`  <a name="cfn-msk-cluster-clustername"></a>
The name of the cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationInfo`  <a name="cfn-msk-cluster-configurationinfo"></a>
The Amazon MSK configuration to use for the cluster\.  
*Required*: No  
*Type*: [ConfigurationInfo](aws-properties-msk-cluster-configurationinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionInfo`  <a name="cfn-msk-cluster-encryptioninfo"></a>
Includes all encryption\-related information\.  
*Required*: No  
*Type*: [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnhancedMonitoring`  <a name="cfn-msk-cluster-enhancedmonitoring"></a>
Specifies the level of monitoring for the MSK cluster\. The possible values are `DEFAULT`, `PER_BROKER`, and `PER_TOPIC_PER_BROKER`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KafkaVersion`  <a name="cfn-msk-cluster-kafkaversion"></a>
The version of Apache Kafka\. You can use Amazon MSK to create clusters that use Apache Kafka versions 1\.1\.1 and 2\.2\.1\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingInfo`  <a name="cfn-msk-cluster-logginginfo"></a>
You can configure your MSK cluster to send broker logs to different destination types\. This is a container for the configuration details related to broker logs\.  
*Required*: No  
*Type*: [LoggingInfo](aws-properties-msk-cluster-logginginfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfBrokerNodes`  <a name="cfn-msk-cluster-numberofbrokernodes"></a>
The number of broker nodes you want in the Amazon MSK cluster\. You can submit an update to increase the number of broker nodes in a cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenMonitoring`  <a name="cfn-msk-cluster-openmonitoring"></a>
The settings for open monitoring\.  
*Required*: No  
*Type*: [OpenMonitoring](aws-properties-msk-cluster-openmonitoring.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-msk-cluster-tags"></a>
A map of key:value pairs to apply to this resource\. Both key and value are of type String\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-msk-cluster-return-values"></a>

### Ref<a name="aws-resource-msk-cluster-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon MSK cluster ARN\. For example:

 `REF MyTestCluster` 

For the Amazon MSK cluster `MyTestCluster`, Ref returns the ARN of the cluster\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-msk-cluster--examples"></a>

In the following examples you can find the YAML for each template, followed by the equivalent JSON\. You can use either language\.

### Create an MSK Cluster Where You Only Specify Values for the Required Properties<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Only_Specify_Values_for_the_Required_Properties"></a>

#### YAML<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Only_Specify_Values_for_the_Required_Properties--yaml"></a>

```
Description: MSK Cluster with required properties.
Resources:
  TestCluster:
    Type: 'AWS::MSK::Cluster'
    Properties:
      ClusterName: ClusterWithRequiredProperties
      KafkaVersion: 2.2.1
      NumberOfBrokerNodes: 3
      BrokerNodeGroupInfo:
        InstanceType: kafka.m5.large
        ClientSubnets:
          - ReplaceWithSubnetId1
          - ReplaceWithSubnetId2
          - ReplaceWithSubnetId3
```

#### <a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Only_Specify_Values_for_the_Required_Properties--JSON"></a>

```
{
    "Description": "MSK Cluster with required properties.",
    "Resources": {
        "TestCluster": {
            "Type": "AWS::MSK::Cluster",
            "Properties": {
                "ClusterName": "ClusterWithRequiredProperties",
                "KafkaVersion": "2.2.1",
                "NumberOfBrokerNodes": 3,
                "BrokerNodeGroupInfo": {
                    "InstanceType": "kafka.m5.large",
                    "ClientSubnets": [
                        "ReplaceWithSubnetId1",
                        "ReplaceWithSubnetId2",
                        "ReplaceWithSubnetId3"
                    ]
                }
            }
        }
    }
}
```

### Create an MSK Cluster Where You Explicitly Set All Properties<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Explicitly_Set_All_Properties"></a>

#### YAML<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Explicitly_Set_All_Properties--yaml"></a>

```
Description: MSK Cluster with all properties
Resources:
  TestCluster:
    Type: 'AWS::MSK::Cluster'
    Properties:
      ClusterName: ClusterWithAllProperties
      KafkaVersion: 2.2.1
      NumberOfBrokerNodes: 3
      EnhancedMonitoring: PER_BROKER
      EncryptionInfo:
        EncryptionAtRest:
          DataVolumeKMSKeyId: ReplaceWithKmsKeyArn
        EncryptionInTransit:
          ClientBroker: TLS
          InCluster: true
      OpenMonitoring:
        Prometheus:
          JmxExporter:
            EnabledInBroker: "true"
          NodeExporter:
            EnabledInBroker: "true"
      ConfigurationInfo:
        Arn: ReplaceWithConfigurationArn
        Revision: 1
      ClientAuthentication:
        Tls:
          CertificateAuthorityArnList:
            - ReplaceWithCAArn
      Tags:
        Environment: Test
        Owner: QATeam
      BrokerNodeGroupInfo:
        BrokerAZDistribution: DEFAULT
        InstanceType: kafka.m5.large
        SecurityGroups:
          - ReplaceWithSecurityGroupId
        StorageInfo:
          EBSStorageInfo:
            VolumeSize: 100
        ClientSubnets:
          - ReplaceWithSubnetId1
          - ReplaceWithSubnetId2
          - ReplaceWithSubnetId3
```

#### <a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Explicitly_Set_All_Properties--JSON"></a>

```
{
    "Description": "MSK Cluster with all properties",
    "Resources": {
        "TestCluster": {
            "Type": "AWS::MSK::Cluster",
            "Properties": {
                "ClusterName": "ClusterWithAllProperties",
                "KafkaVersion": "2.2.1",
                "NumberOfBrokerNodes": 3,
                "EnhancedMonitoring": "PER_BROKER",
                "EncryptionInfo": {
                    "EncryptionAtRest": {
                        "DataVolumeKMSKeyId": "ReplaceWithKmsKeyArn"
                    },
                    "EncryptionInTransit": {
                        "ClientBroker": "TLS",
                        "InCluster": true
                    }
                },
                "OpenMonitoring": {
                    "Prometheus": {
                        "JmxExporter": {
                            "EnabledInBroker": "true"
                        }
                        "NodeExporter": {
                            "EnabledInBroker": "true"
                        }
                    }
                },
                "ConfigurationInfo": {
                    "Arn": "ReplaceWithConfigurationArn",
                    "Revision": 1
                },
                "ClientAuthentication": {
                    "Tls": {
                        "CertificateAuthorityArnList": [
                            "ReplaceWithCAArn"
                        ]
                    }
                },
                "Tags": {
                    "Environment": "Test",
                    "Owner" : "QATeam"
                },
                "BrokerNodeGroupInfo": {
                    "BrokerAZDistribution": "DEFAULT",
                    "InstanceType": "kafka.m5.large",
                    "SecurityGroups": [
                        "ReplaceWithSecurityGroupId"
                    ],
                    "StorageInfo": {
                        "EBSStorageInfo": {
                            "VolumeSize": 100
                        }
                    },
                    "ClientSubnets": [
                        "ReplaceWithSubnetId1",
                        "ReplaceWithSubnetId2",
                        "ReplaceWithSubnetId3"
                    ]
                }
            }
        }
    }
}
```

### Get Started With Amazon MSK<a name="aws-resource-msk-cluster--examples--Get_Started_With_Amazon_MSK"></a>

This example template creates an MSK cluster in a simple architecture to help you get started\.

#### YAML<a name="aws-resource-msk-cluster--examples--Get_Started_With_Amazon_MSK--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  KeyName:
    Description: Name of an existing EC2 KeyPair to enable SSH access to the instance
    Type: 'AWS::EC2::KeyPair::KeyName'
    ConstraintDescription: Can contain only ASCII characters.
  SSHLocation:
    Description: The IP address range that can be used to SSH to the EC2 instances
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 0.0.0.0/0
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: Must be a valid IP CIDR range of the form x.x.x.x/x
Mappings:
  SubnetConfig:
    VPC:
      CIDR: 10.0.0.0/16
    PublicOne:
      CIDR: 10.0.0.0/24
    PrivateOne:
      CIDR: 10.0.1.0/24
    PrivateTwo:
      CIDR: 10.0.2.0/24
    PrivateThree:
      CIDR: 10.0.3.0/24
  RegionAMI:
    us-east-1:
      HVM64: ami-0c6b1d09930fac512
    us-west-2:
      HVM64: ami-0cb72367e98845d43
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      EnableDnsSupport: true
      EnableDnsHostnames: true
      CidrBlock: !FindInMap 
        - SubnetConfig
        - VPC
        - CIDR
      Tags:
        - Key: Name
          Value: MMVPC
  PublicSubnetOne:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 0
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PublicOne
        - CIDR
      MapPublicIpOnLaunch: true
      Tags:
        - Key: Name
          Value: MMPublicSubnet
  PrivateSubnetOne:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 0
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PrivateOne
        - CIDR
      Tags:
        - Key: Name
          Value: MMPrivateSubnetOne
  PrivateSubnetTwo:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 1
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PrivateTwo
        - CIDR
      Tags:
        - Key: Name
          Value: MMPrivateSubnetTwo
  PrivateSubnetThree:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 2
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PrivateThree
        - CIDR
      Tags:
        - Key: Name
          Value: MMPrivateSubnetThree
  InternetGateway:
    Type: 'AWS::EC2::InternetGateway'
  GatewayAttachement:
    Type: 'AWS::EC2::VPCGatewayAttachment'
    Properties:
      VpcId: !Ref VPC
      InternetGatewayId: !Ref InternetGateway
  PublicRouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref VPC
  PublicRoute:
    Type: 'AWS::EC2::Route'
    DependsOn: GatewayAttachement
    Properties:
      RouteTableId: !Ref PublicRouteTable
      DestinationCidrBlock: 0.0.0.0/0
      GatewayId: !Ref InternetGateway
  PublicSubnetOneRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      SubnetId: !Ref PublicSubnetOne
      RouteTableId: !Ref PublicRouteTable
  PrivateRouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref VPC
  PrivateSubnetOneRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetOne
  PrivateSubnetTwoRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetTwo
  PrivateSubnetThreeRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetThree
  KafkaClientInstanceSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access via port 22
      VpcId: !Ref VPC
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 22
          ToPort: 22
          CidrIp: !Ref SSHLocation
  MSKSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access via port 22
      VpcId: !Ref VPC
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 2181
          ToPort: 2181
          SourceSecurityGroupId: !GetAtt 
            - KafkaClientInstanceSecurityGroup
            - GroupId
        - IpProtocol: tcp
          FromPort: 9094
          ToPort: 9094
          SourceSecurityGroupId: !GetAtt 
            - KafkaClientInstanceSecurityGroup
            - GroupId
        - IpProtocol: tcp
          FromPort: 9092
          ToPort: 9092
          SourceSecurityGroupId: !GetAtt 
            - KafkaClientInstanceSecurityGroup
            - GroupId
  KafkaClientEC2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: m5.large
      KeyName: !Ref KeyName
      IamInstanceProfile: !Ref EC2InstanceProfile
      AvailabilityZone: !Select 
        - 0
        - !GetAZs 
          Ref: 'AWS::Region'
      SubnetId: !Ref PublicSubnetOne
      SecurityGroupIds:
        - !GetAtt 
          - KafkaClientInstanceSecurityGroup
          - GroupId
      ImageId: !FindInMap 
        - RegionAMI
        - !Ref 'AWS::Region'
        - HVM64
      Tags:
        - Key: Name
          Value: KafkaClientInstance
      UserData: !Base64 >
        #!/bin/bash

        yum update -y 

        yum install python3.7 -y

        yum install java-1.8.0-openjdk-devel -y

        yum erase awscli -y

        cd /home/ec2-user

        echo "export PATH=.local/bin:$PATH" >> .bash_profile

        mkdir kafka

        mkdir mm

        cd kafka

        wget https://archive.apache.org/dist/kafka/2.2.1/kafka_2.12-2.2.1.tgz

        tar -xzf kafka_2.12-2.2.1.tgz

        cd /home/ec2-user

        wget https://bootstrap.pypa.io/get-pip.py

        su -c "python3.7 get-pip.py --user" -s /bin/sh ec2-user

        su -c "/home/ec2-user/.local/bin/pip3 install boto3 --user" -s /bin/sh
        ec2-user

        su -c "/home/ec2-user/.local/bin/pip3 install awscli --user" -s /bin/sh
        ec2-user

        chown -R ec2-user ./kafka

        chgrp -R ec2-user ./kafka

        chown -R ec2-user ./mm

        chgrp -R ec2-user ./mm
  EC2Role:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: ec2.amazonaws.com
            Action: 'sts:AssumeRole'
      Path: /
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/AmazonMSKFullAccess'
        - 'arn:aws:iam::aws:policy/AWSCloudFormationReadOnlyAccess'
  EC2InstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      InstanceProfileName: EC2MSKCFProfile
      Roles:
        - !Ref EC2Role
  MSKCluster:
    Type: 'AWS::MSK::Cluster'
    Properties:
      BrokerNodeGroupInfo:
        ClientSubnets:
          - !Ref PrivateSubnetOne
          - !Ref PrivateSubnetTwo
          - !Ref PrivateSubnetThree
        InstanceType: kafka.m5.large
        SecurityGroups:
          - !GetAtt 
            - MSKSecurityGroup
            - GroupId
        StorageInfo:
          EBSStorageInfo:
            VolumeSize: 2000
      ClusterName: MSKCluster
      EncryptionInfo:
        EncryptionInTransit:
          ClientBroker: TLS
          InCluster: true
      EnhancedMonitoring: PER_TOPIC_PER_BROKER
      KafkaVersion: 2.2.1
      NumberOfBrokerNodes: 3
Outputs:
  VPCId:
    Description: The ID of the VPC created
    Value: !Ref VPC
  PublicSubnetOne:
    Description: The name of the public subnet created
    Value: !Ref PublicSubnetOne
  PrivateSubnetOne:
    Description: The ID of private subnet one created
    Value: !Ref PrivateSubnetOne
  PrivateSubnetTwo:
    Description: The ID of private subnet two created
    Value: !Ref PrivateSubnetTwo
  PrivateSubnetThree:
    Description: The ID of private subnet three created
    Value: !Ref PrivateSubnetThree
  MSKSecurityGroupID:
    Description: The ID of the security group created for the MSK clusters
    Value: !GetAtt 
      - MSKSecurityGroup
      - GroupId
  KafkaClientEC2InstancePublicDNS:
    Description: The Public DNS for the MirrorMaker EC2 instance
    Value: !GetAtt 
      - KafkaClientEC2Instance
      - PublicDnsName
  MSKClusterArn:
    Description: The Arn for the MSKMMCluster1 MSK cluster
    Value: !Ref MSKCluster
```

#### <a name="aws-resource-msk-cluster--examples--Get_Started_With_Amazon_MSK--JSON"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "KeyName": {
            "Description": "Name of an existing EC2 KeyPair to enable SSH access to the instance",
            "Type": "AWS::EC2::KeyPair::KeyName",
            "ConstraintDescription": "Can contain only ASCII characters."
        },
        "SSHLocation": {
            "Description": "The IP address range that can be used to SSH to the EC2 instances",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "0.0.0.0/0",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "Must be a valid IP CIDR range of the form x.x.x.x/x"
        }
    },
    "Mappings": {
        "SubnetConfig": {
            "VPC": {
                "CIDR": "10.0.0.0/16"
            },
            "PublicOne": {
                "CIDR": "10.0.0.0/24"
            },
            "PrivateOne": {
                "CIDR": "10.0.1.0/24"
            },
            "PrivateTwo": {
                "CIDR": "10.0.2.0/24"
            },
            "PrivateThree": {
                "CIDR": "10.0.3.0/24"
            }
        },
        "RegionAMI": {
            "us-east-1": {
                "HVM64": "ami-0c6b1d09930fac512"
            },
            "us-west-2": {
                "HVM64": "ami-0cb72367e98845d43"
            }
        }
    },
    "Resources": {
        "VPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "EnableDnsSupport": true,
                "EnableDnsHostnames": true,
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "VPC",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMVPC"
                    }
                ]
            }
        },
        "PublicSubnetOne": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        0,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PublicOne",
                        "CIDR"
                    ]
                },
                "MapPublicIpOnLaunch": true,
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPublicSubnet"
                    }
                ]
            }
        },
        "PrivateSubnetOne": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        0,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PrivateOne",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPrivateSubnetOne"
                    }
                ]
            }
        },
        "PrivateSubnetTwo": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        1,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PrivateTwo",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPrivateSubnetTwo"
                    }
                ]
            }
        },
        "PrivateSubnetThree": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        2,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PrivateThree",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPrivateSubnetThree"
                    }
                ]
            }
        },
        "InternetGateway": {
            "Type": "AWS::EC2::InternetGateway"
        },
        "GatewayAttachement": {
            "Type": "AWS::EC2::VPCGatewayAttachment",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                },
                "InternetGatewayId": {
                    "Ref": "InternetGateway"
                }
            }
        },
        "PublicRouteTable": {
            "Type": "AWS::EC2::RouteTable",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            }
        },
        "PublicRoute": {
            "Type": "AWS::EC2::Route",
            "DependsOn": "GatewayAttachement",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PublicRouteTable"
                },
                "DestinationCidrBlock": "0.0.0.0/0",
                "GatewayId": {
                    "Ref": "InternetGateway"
                }
            }
        },
        "PublicSubnetOneRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "SubnetId": {
                    "Ref": "PublicSubnetOne"
                },
                "RouteTableId": {
                    "Ref": "PublicRouteTable"
                }
            }
        },
        "PrivateRouteTable": {
            "Type": "AWS::EC2::RouteTable",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            }
        },
        "PrivateSubnetOneRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PrivateRouteTable"
                },
                "SubnetId": {
                    "Ref": "PrivateSubnetOne"
                }
            }
        },
        "PrivateSubnetTwoRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PrivateRouteTable"
                },
                "SubnetId": {
                    "Ref": "PrivateSubnetTwo"
                }
            }
        },
        "PrivateSubnetThreeRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PrivateRouteTable"
                },
                "SubnetId": {
                    "Ref": "PrivateSubnetThree"
                }
            }
        },
        "KafkaClientInstanceSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable SSH access via port 22",
                "VpcId": {
                    "Ref": "VPC"
                },
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 22,
                        "ToPort": 22,
                        "CidrIp": {
                            "Ref": "SSHLocation"
                        }
                    }
                ]
            }
        },
        "MSKSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable SSH access via port 22",
                "VpcId": {
                    "Ref": "VPC"
                },
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 2181,
                        "ToPort": 2181,
                        "SourceSecurityGroupId": {
                            "Fn::GetAtt": [
                                "KafkaClientInstanceSecurityGroup",
                                "GroupId"
                            ]
                        }
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 9094,
                        "ToPort": 9094,
                        "SourceSecurityGroupId": {
                            "Fn::GetAtt": [
                                "KafkaClientInstanceSecurityGroup",
                                "GroupId"
                            ]
                        }
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 9092,
                        "ToPort": 9092,
                        "SourceSecurityGroupId": {
                            "Fn::GetAtt": [
                                "KafkaClientInstanceSecurityGroup",
                                "GroupId"
                            ]
                        }
                    }
                ]
            }
        },
        "KafkaClientEC2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "InstanceType": "m5.large",
                "KeyName": {
                    "Ref": "KeyName"
                },
                "IamInstanceProfile": {
                    "Ref": "EC2InstanceProfile"
                },
                "AvailabilityZone": {
                    "Fn::Select": [
                        0,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "SubnetId": {
                    "Ref": "PublicSubnetOne"
                },
                "SecurityGroupIds": [
                    {
                        "Fn::GetAtt": [
                            "KafkaClientInstanceSecurityGroup",
                            "GroupId"
                        ]
                    }
                ],
                "ImageId": {
                    "Fn::FindInMap": [
                        "RegionAMI",
                        {
                            "Ref": "AWS::Region"
                        },
                        "HVM64"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "KafkaClientInstance"
                    }
                ],
                "UserData": {
                    "Fn::Base64": "#!/bin/bash\nyum update -y \nyum install python3.7 -y\nyum install java-1.8.0-openjdk-devel -y\nyum erase awscli -y\ncd /home/ec2-user\necho \"export PATH=.local/bin:$PATH\" >> .bash_profile\nmkdir kafka\nmkdir mm\ncd kafka\nwget https://archive.apache.org/dist/kafka/2.2.1/kafka_2.12-2.2.1.tgz\ntar -xzf kafka_2.12-2.2.1.tgz\ncd /home/ec2-user\nwget https://bootstrap.pypa.io/get-pip.py\nsu -c \"python3.7 get-pip.py --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install boto3 --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install awscli --user\" -s /bin/sh ec2-user\nchown -R ec2-user ./kafka\nchgrp -R ec2-user ./kafka\nchown -R ec2-user ./mm\nchgrp -R ec2-user ./mm\n"
                }
            }
        },
        "EC2Role": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Sid": "",
                            "Effect": "Allow",
                            "Principal": {
                                "Service": "ec2.amazonaws.com"
                            },
                            "Action": "sts:AssumeRole"
                        }
                    ]
                },
                "Path": "/",
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/AmazonMSKFullAccess",
                    "arn:aws:iam::aws:policy/AWSCloudFormationReadOnlyAccess"
                ]
            }
        },
        "EC2InstanceProfile": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "InstanceProfileName": "EC2MSKCFProfile",
                "Roles": [
                    {
                        "Ref": "EC2Role"
                    }
                ]
            }
        },
        "MSKCluster": {
            "Type": "AWS::MSK::Cluster",
            "Properties": {
                "BrokerNodeGroupInfo": {
                    "ClientSubnets": [
                        {
                            "Ref": "PrivateSubnetOne"
                        },
                        {
                            "Ref": "PrivateSubnetTwo"
                        },
                        {
                            "Ref": "PrivateSubnetThree"
                        }
                    ],
                    "InstanceType": "kafka.m5.large",
                    "SecurityGroups": [
                        {
                            "Fn::GetAtt": [
                                "MSKSecurityGroup",
                                "GroupId"
                            ]
                        }
                    ],
                    "StorageInfo": {
                        "EBSStorageInfo": {
                            "VolumeSize": 2000
                        }
                    }
                },
                "ClusterName": "MSKCluster",
                "EncryptionInfo": {
                    "EncryptionInTransit": {
                        "ClientBroker": "TLS",
                        "InCluster": true
                    }
                },
                "EnhancedMonitoring": "PER_TOPIC_PER_BROKER",
                "KafkaVersion": "2.2.1",
                "NumberOfBrokerNodes": 3
            }
        }
    },
    "Outputs": {
        "VPCId": {
            "Description": "The ID of the VPC created",
            "Value": {
                "Ref": "VPC"
            }
        },
        "PublicSubnetOne": {
            "Description": "The name of the public subnet created",
            "Value": {
                "Ref": "PublicSubnetOne"
            }
        },
        "PrivateSubnetOne": {
            "Description": "The ID of private subnet one created",
            "Value": {
                "Ref": "PrivateSubnetOne"
            }
        },
        "PrivateSubnetTwo": {
            "Description": "The ID of private subnet two created",
            "Value": {
                "Ref": "PrivateSubnetTwo"
            }
        },
        "PrivateSubnetThree": {
            "Description": "The ID of private subnet three created",
            "Value": {
                "Ref": "PrivateSubnetThree"
            }
        },
        "MSKSecurityGroupID": {
            "Description": "The ID of the security group created for the MSK clusters",
            "Value": {
                "Fn::GetAtt": [
                    "MSKSecurityGroup",
                    "GroupId"
                ]
            }
        },
        "KafkaClientEC2InstancePublicDNS": {
            "Description": "The Public DNS for the MirrorMaker EC2 instance",
            "Value": {
                "Fn::GetAtt": [
                    "KafkaClientEC2Instance",
                    "PublicDnsName"
                ]
            }
        },
        "MSKClusterArn": {
            "Description": "The Arn for the MSKMMCluster1 MSK cluster",
            "Value": {
                "Ref": "MSKCluster"
            }
        }
    }
}
```

### Create Two MSK Clusters To Use With Apache MirrorMaker<a name="aws-resource-msk-cluster--examples--Create_Two_MSK_Clusters_To_Use_With_Apache_MirrorMaker"></a>

This YAML shows how to set up two MSK clusters for MirrorMaker\. It also sets up the Amazon VPC, subnets, security groups, and IAM roles that are necessary for this example\. In addition, it creates an EC2 instance that has Apache Kafka, Java, and the AWS CLI\. You can use this EC2 instance to run Apache Kafka tools, including MirrorMaker\. You must manually create the MirrorMaker configuration files\.

#### <a name="aws-resource-msk-cluster--examples--Create_Two_MSK_Clusters_To_Use_With_Apache_MirrorMaker--YAML"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  KeyName:
    Description: The name of an existing EC2 KeyPair to enable SSH access to the instance.
    Type: 'AWS::EC2::KeyPair::KeyName'
    ConstraintDescription: Can contain only ASCII characters.
  SSHLocation:
    Description: The IP address range that can be used to SSH to the EC2 instances.
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 0.0.0.0/0
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: Must be a valid IP CIDR range of the form x.x.x.x/x
Mappings:
  SubnetConfig:
    VPC:
      CIDR: 10.0.0.0/16
    PublicOne:
      CIDR: 10.0.0.0/24
    PrivateOne:
      CIDR: 10.0.1.0/24
    PrivateTwo:
      CIDR: 10.0.2.0/24
    PrivateThree:
      CIDR: 10.0.3.0/24
  RegionAMI:
    us-east-1:
      HVM64: ami-0c6b1d09930fac512
    us-west-2:
      HVM64: ami-0cb72367e98845d43
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      EnableDnsSupport: true
      EnableDnsHostnames: true
      CidrBlock: !FindInMap 
        - SubnetConfig
        - VPC
        - CIDR
      Tags:
        - Key: Name
          Value: MMVPC
  PublicSubnetOne:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 0
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PublicOne
        - CIDR
      MapPublicIpOnLaunch: true
      Tags:
        - Key: Name
          Value: MMPublicSubnet
  PrivateSubnetOne:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 0
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PrivateOne
        - CIDR
      Tags:
        - Key: Name
          Value: MMPrivateSubnetOne
  PrivateSubnetTwo:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 1
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PrivateTwo
        - CIDR
      Tags:
        - Key: Name
          Value: MMPrivateSubnetTwo
  PrivateSubnetThree:
    Type: 'AWS::EC2::Subnet'
    Properties:
      AvailabilityZone: !Select 
        - 2
        - !GetAZs 
          Ref: 'AWS::Region'
      VpcId: !Ref VPC
      CidrBlock: !FindInMap 
        - SubnetConfig
        - PrivateThree
        - CIDR
      Tags:
        - Key: Name
          Value: MMPrivateSubnetThree
  InternetGateway:
    Type: 'AWS::EC2::InternetGateway'
  GatewayAttachement:
    Type: 'AWS::EC2::VPCGatewayAttachment'
    Properties:
      VpcId: !Ref VPC
      InternetGatewayId: !Ref InternetGateway
  PublicRouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref VPC
  PublicRoute:
    Type: 'AWS::EC2::Route'
    DependsOn: GatewayAttachement
    Properties:
      RouteTableId: !Ref PublicRouteTable
      DestinationCidrBlock: 0.0.0.0/0
      GatewayId: !Ref InternetGateway
  PublicSubnetOneRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      SubnetId: !Ref PublicSubnetOne
      RouteTableId: !Ref PublicRouteTable
  PrivateRouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref VPC
  PrivateSubnetOneRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetOne
  PrivateSubnetTwoRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetTwo
  PrivateSubnetThreeRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetThree
  MMInstanceSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access via port 22
      VpcId: !Ref VPC
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 22
          ToPort: 22
          CidrIp: !Ref SSHLocation
  MSKSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access via port 22
      VpcId: !Ref VPC
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 2181
          ToPort: 2181
          SourceSecurityGroupId: !GetAtt 
            - MMInstanceSecurityGroup
            - GroupId
        - IpProtocol: tcp
          FromPort: 9094
          ToPort: 9094
          SourceSecurityGroupId: !GetAtt 
            - MMInstanceSecurityGroup
            - GroupId
        - IpProtocol: tcp
          FromPort: 9092
          ToPort: 9092
          SourceSecurityGroupId: !GetAtt 
            - MMInstanceSecurityGroup
            - GroupId
  MMEC2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: m5.large
      KeyName: !Ref KeyName
      IamInstanceProfile: !Ref EC2InstanceProfile
      AvailabilityZone: !Select 
        - 0
        - !GetAZs 
          Ref: 'AWS::Region'
      SubnetId: !Ref PublicSubnetOne
      SecurityGroupIds:
        - !GetAtt 
          - MMInstanceSecurityGroup
          - GroupId
      ImageId: !FindInMap 
        - RegionAMI
        - !Ref 'AWS::Region'
        - HVM64
      Tags:
        - Key: Name
          Value: MMInstance
      UserData: !Base64 >
        #!/bin/bash

        yum update -y 

        yum install python3.7 -y

        yum install java-1.8.0-openjdk-devel -y

        yum erase awscli -y

        cd /home/ec2-user

        echo "export PATH=.local/bin:$PATH" >> .bash_profile

        mkdir kafka

        mkdir mm

        cd kafka

        wget https://archive.apache.org/dist/kafka/2.2.1/kafka_2.12-2.2.1.tgz

        tar -xzf kafka_2.12-2.2.1.tgz

        cd /home/ec2-user

        wget https://bootstrap.pypa.io/get-pip.py

        su -c "python3.7 get-pip.py --user" -s /bin/sh ec2-user

        su -c "/home/ec2-user/.local/bin/pip3 install boto3 --user" -s /bin/sh
        ec2-user

        su -c "/home/ec2-user/.local/bin/pip3 install awscli --user" -s /bin/sh
        ec2-user

        chown -R ec2-user ./kafka

        chgrp -R ec2-user ./kafka

        chown -R ec2-user ./mm

        chgrp -R ec2-user ./mm
  EC2Role:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: ec2.amazonaws.com
            Action: 'sts:AssumeRole'
      Path: /
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/AmazonMSKFullAccess'
        - 'arn:aws:iam::aws:policy/AWSCloudFormationReadOnlyAccess'
  EC2InstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      InstanceProfileName: EC2MSKCFProfile
      Roles:
        - !Ref EC2Role
  MSKMMCluster1:
    Type: 'AWS::MSK::Cluster'
    Properties:
      BrokerNodeGroupInfo:
        ClientSubnets:
          - !Ref PrivateSubnetOne
          - !Ref PrivateSubnetTwo
          - !Ref PrivateSubnetThree
        InstanceType: kafka.m5.large
        SecurityGroups:
          - !GetAtt 
            - MSKSecurityGroup
            - GroupId
        StorageInfo:
          EBSStorageInfo:
            VolumeSize: 2000
      ClusterName: MSKMMCluster1
      EncryptionInfo:
        EncryptionInTransit:
          ClientBroker: TLS
          InCluster: true
      EnhancedMonitoring: PER_TOPIC_PER_BROKER
      KafkaVersion: 2.2.1
      NumberOfBrokerNodes: 3
  MSKMMCluster2:
    Type: 'AWS::MSK::Cluster'
    Properties:
      BrokerNodeGroupInfo:
        ClientSubnets:
          - !Ref PrivateSubnetOne
          - !Ref PrivateSubnetTwo
          - !Ref PrivateSubnetThree
        InstanceType: kafka.m5.large
        SecurityGroups:
          - !GetAtt 
            - MSKSecurityGroup
            - GroupId
        StorageInfo:
          EBSStorageInfo:
            VolumeSize: 2000
      ClusterName: MSKMMCluster2
      EncryptionInfo:
        EncryptionInTransit:
          ClientBroker: TLS
          InCluster: true
      EnhancedMonitoring: PER_TOPIC_PER_BROKER
      KafkaVersion: 2.2.1
      NumberOfBrokerNodes: 3
Outputs:
  VPCId:
    Description: The ID of the VPC created
    Value: !Ref VPC
  PublicSubnetOne:
    Description: The name of the public subnet created
    Value: !Ref PublicSubnetOne
  PrivateSubnetOne:
    Description: The ID of private subnet one created
    Value: !Ref PrivateSubnetOne
  PrivateSubnetTwo:
    Description: The ID of private subnet two created
    Value: !Ref PrivateSubnetTwo
  PrivateSubnetThree:
    Description: The ID of private subnet three created
    Value: !Ref PrivateSubnetThree
  MSKSecurityGroupID:
    Description: The ID of the security group created for the MSK clusters
    Value: !GetAtt 
      - MSKSecurityGroup
      - GroupId
  MMEC2InstancePublicDNS:
    Description: The Public DNS for the MirrorMaker EC2 instance
    Value: !GetAtt 
      - MMEC2Instance
      - PublicDnsName
  MSKMMCluster1Arn:
    Description: The Arn for the MSKMMCluster1 MSK cluster
    Value: !Ref MSKMMCluster1
  MSKMMCluster2Arn:
    Description: The Arn for the MSKMMCluster2 MSK cluster
    Value: !Ref MSKMMCluster2
```

#### <a name="aws-resource-msk-cluster--examples--Create_Two_MSK_Clusters_To_Use_With_Apache_MirrorMaker--JSON"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "KeyName": {
            "Description": "The name of an existing EC2 KeyPair to enable SSH access to the instance.",
            "Type": "AWS::EC2::KeyPair::KeyName",
            "ConstraintDescription": "Can contain only ASCII characters."
        },
        "SSHLocation": {
            "Description": "The IP address range that can be used to SSH to the EC2 instances.",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "0.0.0.0/0",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "Must be a valid IP CIDR range of the form x.x.x.x/x"
        }
    },
    "Mappings": {
        "SubnetConfig": {
            "VPC": {
                "CIDR": "10.0.0.0/16"
            },
            "PublicOne": {
                "CIDR": "10.0.0.0/24"
            },
            "PrivateOne": {
                "CIDR": "10.0.1.0/24"
            },
            "PrivateTwo": {
                "CIDR": "10.0.2.0/24"
            },
            "PrivateThree": {
                "CIDR": "10.0.3.0/24"
            }
        },
        "RegionAMI": {
            "us-east-1": {
                "HVM64": "ami-0c6b1d09930fac512"
            },
            "us-west-2": {
                "HVM64": "ami-0cb72367e98845d43"
            }
        }
    },
    "Resources": {
        "VPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "EnableDnsSupport": true,
                "EnableDnsHostnames": true,
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "VPC",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMVPC"
                    }
                ]
            }
        },
        "PublicSubnetOne": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        0,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PublicOne",
                        "CIDR"
                    ]
                },
                "MapPublicIpOnLaunch": true,
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPublicSubnet"
                    }
                ]
            }
        },
        "PrivateSubnetOne": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        0,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PrivateOne",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPrivateSubnetOne"
                    }
                ]
            }
        },
        "PrivateSubnetTwo": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        1,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PrivateTwo",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPrivateSubnetTwo"
                    }
                ]
            }
        },
        "PrivateSubnetThree": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "AvailabilityZone": {
                    "Fn::Select": [
                        2,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "VpcId": {
                    "Ref": "VPC"
                },
                "CidrBlock": {
                    "Fn::FindInMap": [
                        "SubnetConfig",
                        "PrivateThree",
                        "CIDR"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMPrivateSubnetThree"
                    }
                ]
            }
        },
        "InternetGateway": {
            "Type": "AWS::EC2::InternetGateway"
        },
        "GatewayAttachement": {
            "Type": "AWS::EC2::VPCGatewayAttachment",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                },
                "InternetGatewayId": {
                    "Ref": "InternetGateway"
                }
            }
        },
        "PublicRouteTable": {
            "Type": "AWS::EC2::RouteTable",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            }
        },
        "PublicRoute": {
            "Type": "AWS::EC2::Route",
            "DependsOn": "GatewayAttachement",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PublicRouteTable"
                },
                "DestinationCidrBlock": "0.0.0.0/0",
                "GatewayId": {
                    "Ref": "InternetGateway"
                }
            }
        },
        "PublicSubnetOneRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "SubnetId": {
                    "Ref": "PublicSubnetOne"
                },
                "RouteTableId": {
                    "Ref": "PublicRouteTable"
                }
            }
        },
        "PrivateRouteTable": {
            "Type": "AWS::EC2::RouteTable",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            }
        },
        "PrivateSubnetOneRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PrivateRouteTable"
                },
                "SubnetId": {
                    "Ref": "PrivateSubnetOne"
                }
            }
        },
        "PrivateSubnetTwoRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PrivateRouteTable"
                },
                "SubnetId": {
                    "Ref": "PrivateSubnetTwo"
                }
            }
        },
        "PrivateSubnetThreeRouteTableAssociation": {
            "Type": "AWS::EC2::SubnetRouteTableAssociation",
            "Properties": {
                "RouteTableId": {
                    "Ref": "PrivateRouteTable"
                },
                "SubnetId": {
                    "Ref": "PrivateSubnetThree"
                }
            }
        },
        "MMInstanceSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable SSH access via port 22",
                "VpcId": {
                    "Ref": "VPC"
                },
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 22,
                        "ToPort": 22,
                        "CidrIp": {
                            "Ref": "SSHLocation"
                        }
                    }
                ]
            }
        },
        "MSKSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable SSH access via port 22",
                "VpcId": {
                    "Ref": "VPC"
                },
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 2181,
                        "ToPort": 2181,
                        "SourceSecurityGroupId": {
                            "Fn::GetAtt": [
                                "MMInstanceSecurityGroup",
                                "GroupId"
                            ]
                        }
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 9094,
                        "ToPort": 9094,
                        "SourceSecurityGroupId": {
                            "Fn::GetAtt": [
                                "MMInstanceSecurityGroup",
                                "GroupId"
                            ]
                        }
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 9092,
                        "ToPort": 9092,
                        "SourceSecurityGroupId": {
                            "Fn::GetAtt": [
                                "MMInstanceSecurityGroup",
                                "GroupId"
                            ]
                        }
                    }
                ]
            }
        },
        "MMEC2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "InstanceType": "m5.large",
                "KeyName": {
                    "Ref": "KeyName"
                },
                "IamInstanceProfile": {
                    "Ref": "EC2InstanceProfile"
                },
                "AvailabilityZone": {
                    "Fn::Select": [
                        0,
                        {
                            "Fn::GetAZs": {
                                "Ref": "AWS::Region"
                            }
                        }
                    ]
                },
                "SubnetId": {
                    "Ref": "PublicSubnetOne"
                },
                "SecurityGroupIds": [
                    {
                        "Fn::GetAtt": [
                            "MMInstanceSecurityGroup",
                            "GroupId"
                        ]
                    }
                ],
                "ImageId": {
                    "Fn::FindInMap": [
                        "RegionAMI",
                        {
                            "Ref": "AWS::Region"
                        },
                        "HVM64"
                    ]
                },
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "MMInstance"
                    }
                ],
                "UserData": {
                    "Fn::Base64": "#!/bin/bash\nyum update -y \nyum install python3.7 -y\nyum install java-1.8.0-openjdk-devel -y\nyum erase awscli -y\ncd /home/ec2-user\necho \"export PATH=.local/bin:$PATH\" >> .bash_profile\nmkdir kafka\nmkdir mm\ncd kafka\nwget https://archive.apache.org/dist/kafka/2.2.1/kafka_2.12-2.2.1.tgz\ntar -xzf kafka_2.12-2.2.1.tgz\ncd /home/ec2-user\nwget https://bootstrap.pypa.io/get-pip.py\nsu -c \"python3.7 get-pip.py --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install boto3 --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install awscli --user\" -s /bin/sh ec2-user\nchown -R ec2-user ./kafka\nchgrp -R ec2-user ./kafka\nchown -R ec2-user ./mm\nchgrp -R ec2-user ./mm\n"
                }
            }
        },
        "EC2Role": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Sid": "",
                            "Effect": "Allow",
                            "Principal": {
                                "Service": "ec2.amazonaws.com"
                            },
                            "Action": "sts:AssumeRole"
                        }
                    ]
                },
                "Path": "/",
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/AmazonMSKFullAccess",
                    "arn:aws:iam::aws:policy/AWSCloudFormationReadOnlyAccess"
                ]
            }
        },
        "EC2InstanceProfile": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "InstanceProfileName": "EC2MSKCFProfile",
                "Roles": [
                    {
                        "Ref": "EC2Role"
                    }
                ]
            }
        },
        "MSKMMCluster1": {
            "Type": "AWS::MSK::Cluster",
            "Properties": {
                "BrokerNodeGroupInfo": {
                    "ClientSubnets": [
                        {
                            "Ref": "PrivateSubnetOne"
                        },
                        {
                            "Ref": "PrivateSubnetTwo"
                        },
                        {
                            "Ref": "PrivateSubnetThree"
                        }
                    ],
                    "InstanceType": "kafka.m5.large",
                    "SecurityGroups": [
                        {
                            "Fn::GetAtt": [
                                "MSKSecurityGroup",
                                "GroupId"
                            ]
                        }
                    ],
                    "StorageInfo": {
                        "EBSStorageInfo": {
                            "VolumeSize": 2000
                        }
                    }
                },
                "ClusterName": "MSKMMCluster1",
                "EncryptionInfo": {
                    "EncryptionInTransit": {
                        "ClientBroker": "TLS",
                        "InCluster": true
                    }
                },
                "EnhancedMonitoring": "PER_TOPIC_PER_BROKER",
                "KafkaVersion": "2.2.1",
                "NumberOfBrokerNodes": 3
            }
        },
        "MSKMMCluster2": {
            "Type": "AWS::MSK::Cluster",
            "Properties": {
                "BrokerNodeGroupInfo": {
                    "ClientSubnets": [
                        {
                            "Ref": "PrivateSubnetOne"
                        },
                        {
                            "Ref": "PrivateSubnetTwo"
                        },
                        {
                            "Ref": "PrivateSubnetThree"
                        }
                    ],
                    "InstanceType": "kafka.m5.large",
                    "SecurityGroups": [
                        {
                            "Fn::GetAtt": [
                                "MSKSecurityGroup",
                                "GroupId"
                            ]
                        }
                    ],
                    "StorageInfo": {
                        "EBSStorageInfo": {
                            "VolumeSize": 2000
                        }
                    }
                },
                "ClusterName": "MSKMMCluster2",
                "EncryptionInfo": {
                    "EncryptionInTransit": {
                        "ClientBroker": "TLS",
                        "InCluster": true
                    }
                },
                "EnhancedMonitoring": "PER_TOPIC_PER_BROKER",
                "KafkaVersion": "2.2.1",
                "NumberOfBrokerNodes": 3
            }
        }
    },
    "Outputs": {
        "VPCId": {
            "Description": "The ID of the VPC created",
            "Value": {
                "Ref": "VPC"
            }
        },
        "PublicSubnetOne": {
            "Description": "The name of the public subnet created",
            "Value": {
                "Ref": "PublicSubnetOne"
            }
        },
        "PrivateSubnetOne": {
            "Description": "The ID of private subnet one created",
            "Value": {
                "Ref": "PrivateSubnetOne"
            }
        },
        "PrivateSubnetTwo": {
            "Description": "The ID of private subnet two created",
            "Value": {
                "Ref": "PrivateSubnetTwo"
            }
        },
        "PrivateSubnetThree": {
            "Description": "The ID of private subnet three created",
            "Value": {
                "Ref": "PrivateSubnetThree"
            }
        },
        "MSKSecurityGroupID": {
            "Description": "The ID of the security group created for the MSK clusters",
            "Value": {
                "Fn::GetAtt": [
                    "MSKSecurityGroup",
                    "GroupId"
                ]
            }
        },
        "MMEC2InstancePublicDNS": {
            "Description": "The Public DNS for the MirrorMaker EC2 instance",
            "Value": {
                "Fn::GetAtt": [
                    "MMEC2Instance",
                    "PublicDnsName"
                ]
            }
        },
        "MSKMMCluster1Arn": {
            "Description": "The Arn for the MSKMMCluster1 MSK cluster",
            "Value": {
                "Ref": "MSKMMCluster1"
            }
        },
        "MSKMMCluster2Arn": {
            "Description": "The Arn for the MSKMMCluster2 MSK cluster",
            "Value": {
                "Ref": "MSKMMCluster2"
            }
        }
    }
}
```
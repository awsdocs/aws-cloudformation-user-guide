# AWS::MSK::Cluster<a name="aws-resource-msk-cluster"></a>

The `AWS::MSK::Cluster` resource creates an Amazon MSK cluster\. For more information, see [What Is Amazon MSK?](https://docs.aws.amazon.com/msk/latest/developerguide/what-is-msk.html) in the *Amazon MSK Developer Guide*\.

## Syntax<a name="aws-resource-msk-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::Cluster",
  "Properties" : {
      "[BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo)" : [BrokerNodeGroupInfo](aws-properties-msk-cluster-brokernodegroupinfo.md),
      "[ClientAuthentication](#cfn-msk-cluster-clientauthentication)" : [ClientAuthentication](aws-properties-msk-cluster-clientauthentication.md),
      "[ClusterName](#cfn-msk-cluster-clustername)" : String,
      "[ConfigurationInfo](#cfn-msk-cluster-configurationinfo)" : [ConfigurationInfo](aws-properties-msk-cluster-configurationinfo.md),
      "[EncryptionInfo](#cfn-msk-cluster-encryptioninfo)" : [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md),
      "[EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring)" : String,
      "[KafkaVersion](#cfn-msk-cluster-kafkaversion)" : String,
      "[NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes)" : Integer,
      "[Tags](#cfn-msk-cluster-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-msk-cluster-syntax.yaml"></a>

```
Type: AWS::MSK::Cluster
Properties: 
  [BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo): 
    [BrokerNodeGroupInfo](aws-properties-msk-cluster-brokernodegroupinfo.md)
  [ClientAuthentication](#cfn-msk-cluster-clientauthentication): 
    [ClientAuthentication](aws-properties-msk-cluster-clientauthentication.md)
  [ClusterName](#cfn-msk-cluster-clustername): String
  [ConfigurationInfo](#cfn-msk-cluster-configurationinfo): 
    [ConfigurationInfo](aws-properties-msk-cluster-configurationinfo.md)
  [EncryptionInfo](#cfn-msk-cluster-encryptioninfo): 
    [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md)
  [EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring): String
  [KafkaVersion](#cfn-msk-cluster-kafkaversion): String
  [NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes): Integer
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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EncryptionInfo`  <a name="cfn-msk-cluster-encryptioninfo"></a>
Includes all encryption\-related information\.  
*Required*: No  
*Type*: [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnhancedMonitoring`  <a name="cfn-msk-cluster-enhancedmonitoring"></a>
Specifies the level of monitoring for the MSK cluster\. The possible values are `DEFAULT`, `PER_BROKER`, and `PER_TOPIC_PER_BROKER`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KafkaVersion`  <a name="cfn-msk-cluster-kafkaversion"></a>
The version of Apache Kafka\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NumberOfBrokerNodes`  <a name="cfn-msk-cluster-numberofbrokernodes"></a>
The number of broker nodes you want in the Amazon MSK cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-msk-cluster-tags"></a>
An array of key\-value pairs to apply to this resource\. You can specify tags in JSON or in YAML, depending on which format you use for your template\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-msk-cluster-return-values"></a>

### Ref<a name="aws-resource-msk-cluster-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon MSK cluster ARN\. For example:

 `REF MyTestCluster` 

For the Amazon MSK cluster `MyTestCluster`, Ref returns the ARN of the cluster\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-msk-cluster--examples"></a>

In the following examples you can find the YAML for each template, followed by the equivalent JSON. You can use either language.

## Get Started With Amazon MSK

This example template creates an MSK cluster in a simple architecture to help you get started.

#### YAML

```
---
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: e191108b-e241-404a-bed2-b2863bcd5235
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 90cff42d-8429-4a50-b584-5a2ba16651ea
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: be121547-ef38-4d55-a9a9-f67eb35c9cd0
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 1a1c22e5-745b-443d-93d6-78c3572de3c4
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 69ad49b5-ffb5-4019-82dd-1b5433531511
  InternetGateway:
    Type: 'AWS::EC2::InternetGateway'
    Metadata:
      'AWS::CloudFormation::Designer':
        id: d2a821e3-5c45-46a4-92fd-09268f72f679
  GatewayAttachement:
    Type: 'AWS::EC2::VPCGatewayAttachment'
    Properties:
      VpcId: !Ref VPC
      InternetGatewayId: !Ref InternetGateway
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 988bff04-9cdd-4ce1-8b5d-59fc3291eae1
  PublicRouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref VPC
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 93747341-451f-4c6e-8265-6873b110ae9e
  PublicRoute:
    Type: 'AWS::EC2::Route'
    DependsOn: GatewayAttachement
    Properties:
      RouteTableId: !Ref PublicRouteTable
      DestinationCidrBlock: 0.0.0.0/0
      GatewayId: !Ref InternetGateway
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 412c8444-e8b8-43eb-8c07-3f822c921e34
  PublicSubnetOneRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      SubnetId: !Ref PublicSubnetOne
      RouteTableId: !Ref PublicRouteTable
    Metadata:
      'AWS::CloudFormation::Designer':
        id: c2c64928-4fe4-4640-a449-08cdc9e50d84
  PrivateRouteTable:
    Type: 'AWS::EC2::RouteTable'
    Properties:
      VpcId: !Ref VPC
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 7a45b627-d06a-4956-9f4b-a79b5e65bc7d
  PrivateSubnetOneRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetOne
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 912ef118-eda5-437f-afd7-3f92d83fd70b
  PrivateSubnetTwoRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetTwo
    Metadata:
      'AWS::CloudFormation::Designer':
        id: d345d815-288f-4446-add0-dd637cc6c57f
  PrivateSubnetThreeRouteTableAssociation:
    Type: 'AWS::EC2::SubnetRouteTableAssociation'
    Properties:
      RouteTableId: !Ref PrivateRouteTable
      SubnetId: !Ref PrivateSubnetThree
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 4f6ec5cd-f063-4163-8494-31bd55bcb27f
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 758d2702-7bfd-470e-84a0-5101471dd251
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 20d8d324-9da6-49f9-9e37-4bd433625c47
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

        wget https://archive.apache.org/dist/kafka/2.1.0/kafka_2.12-2.1.0.tgz

        tar -xzf kafka_2.12-2.1.0.tgz

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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 25e7995f-31fc-45b0-b790-42bcb519905a
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
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 268a951d-285d-438a-a365-d135a51bd01c
  EC2InstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      InstanceProfileName: EC2MSKCFProfile
      Roles:
        - !Ref EC2Role
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 01de5e28-2175-45f1-a37f-65e5bd7d9356
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
      KafkaVersion: 2.1.0
      NumberOfBrokerNodes: 3
    Metadata:
      'AWS::CloudFormation::Designer':
        id: 56f5417a-ddff-49c4-9f30-8041824a0601
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
Metadata:
  'AWS::CloudFormation::Designer':
    268a951d-285d-438a-a365-d135a51bd01c:
      size:
        width: 60
        height: 60
      position:
        x: 60
        'y': 930
      z: 1
      embeds: []
    01de5e28-2175-45f1-a37f-65e5bd7d9356:
      size:
        width: 60
        height: 60
      position:
        x: 180
        'y': 930
      z: 1
      embeds: []
      isassociatedwith:
        - 268a951d-285d-438a-a365-d135a51bd01c
    d2a821e3-5c45-46a4-92fd-09268f72f679:
      size:
        width: 60
        height: 60
      position:
        x: 300
        'y': 930
      z: 1
      embeds: []
    e191108b-e241-404a-bed2-b2863bcd5235:
      size:
        width: 870
        height: 780
      position:
        x: 320
        'y': 40
      z: 1
      embeds:
        - 758d2702-7bfd-470e-84a0-5101471dd251
        - 20d8d324-9da6-49f9-9e37-4bd433625c47
        - 7a45b627-d06a-4956-9f4b-a79b5e65bc7d
        - 93747341-451f-4c6e-8265-6873b110ae9e
        - 69ad49b5-ffb5-4019-82dd-1b5433531511
        - 1a1c22e5-745b-443d-93d6-78c3572de3c4
        - be121547-ef38-4d55-a9a9-f67eb35c9cd0
        - 90cff42d-8429-4a50-b584-5a2ba16651ea
    758d2702-7bfd-470e-84a0-5101471dd251:
      size:
        width: 60
        height: 60
      position:
        x: 980
        'y': 310
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds: []
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    20d8d324-9da6-49f9-9e37-4bd433625c47:
      size:
        width: 60
        height: 60
      position:
        x: 980
        'y': 430
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds: []
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    7a45b627-d06a-4956-9f4b-a79b5e65bc7d:
      size:
        width: 150
        height: 150
      position:
        x: 950
        'y': 100
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds: []
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    93747341-451f-4c6e-8265-6873b110ae9e:
      size:
        width: 240
        height: 240
      position:
        x: 650
        'y': 100
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds:
        - 412c8444-e8b8-43eb-8c07-3f822c921e34
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    988bff04-9cdd-4ce1-8b5d-59fc3291eae1:
      source:
        id: e191108b-e241-404a-bed2-b2863bcd5235
      target:
        id: d2a821e3-5c45-46a4-92fd-09268f72f679
    412c8444-e8b8-43eb-8c07-3f822c921e34:
      size:
        width: 60
        height: 60
      position:
        x: 680
        'y': 160
      z: 3
      parent: 93747341-451f-4c6e-8265-6873b110ae9e
      embeds: []
      isassociatedwith:
        - d2a821e3-5c45-46a4-92fd-09268f72f679
      iscontainedinside:
        - 93747341-451f-4c6e-8265-6873b110ae9e
      dependson:
        - 988bff04-9cdd-4ce1-8b5d-59fc3291eae1
    69ad49b5-ffb5-4019-82dd-1b5433531511:
      size:
        width: 150
        height: 150
      position:
        x: 770
        'y': 400
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds: []
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    4f6ec5cd-f063-4163-8494-31bd55bcb27f:
      source:
        id: 7a45b627-d06a-4956-9f4b-a79b5e65bc7d
      target:
        id: 69ad49b5-ffb5-4019-82dd-1b5433531511
    1a1c22e5-745b-443d-93d6-78c3572de3c4:
      size:
        width: 150
        height: 150
      position:
        x: 560
        'y': 400
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds: []
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    d345d815-288f-4446-add0-dd637cc6c57f:
      source:
        id: 7a45b627-d06a-4956-9f4b-a79b5e65bc7d
      target:
        id: 1a1c22e5-745b-443d-93d6-78c3572de3c4
    be121547-ef38-4d55-a9a9-f67eb35c9cd0:
      size:
        width: 150
        height: 150
      position:
        x: 350
        'y': 400
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds: []
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    56f5417a-ddff-49c4-9f30-8041824a0601:
      size:
        width: 60
        height: 60
      position:
        x: 420
        'y': 930
      z: 1
      embeds: []
    912ef118-eda5-437f-afd7-3f92d83fd70b:
      source:
        id: 7a45b627-d06a-4956-9f4b-a79b5e65bc7d
      target:
        id: be121547-ef38-4d55-a9a9-f67eb35c9cd0
    90cff42d-8429-4a50-b584-5a2ba16651ea:
      size:
        width: 240
        height: 240
      position:
        x: 350
        'y': 100
      z: 2
      parent: e191108b-e241-404a-bed2-b2863bcd5235
      embeds:
        - 25e7995f-31fc-45b0-b790-42bcb519905a
      iscontainedinside:
        - e191108b-e241-404a-bed2-b2863bcd5235
    25e7995f-31fc-45b0-b790-42bcb519905a:
      size:
        width: 60
        height: 60
      position:
        x: 380
        'y': 160
      z: 3
      parent: 90cff42d-8429-4a50-b584-5a2ba16651ea
      embeds: []
      isassociatedwith:
        - 758d2702-7bfd-470e-84a0-5101471dd251
      iscontainedinside:
        - 90cff42d-8429-4a50-b584-5a2ba16651ea
    c2c64928-4fe4-4640-a449-08cdc9e50d84:
      source:
        id: 93747341-451f-4c6e-8265-6873b110ae9e
      target:
        id: 90cff42d-8429-4a50-b584-5a2ba16651ea
```

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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "e191108b-e241-404a-bed2-b2863bcd5235"
                }
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "90cff42d-8429-4a50-b584-5a2ba16651ea"
                }
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "be121547-ef38-4d55-a9a9-f67eb35c9cd0"
                }
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "1a1c22e5-745b-443d-93d6-78c3572de3c4"
                }
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "69ad49b5-ffb5-4019-82dd-1b5433531511"
                }
            }
        },
        "InternetGateway": {
            "Type": "AWS::EC2::InternetGateway",
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "d2a821e3-5c45-46a4-92fd-09268f72f679"
                }
            }
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "988bff04-9cdd-4ce1-8b5d-59fc3291eae1"
                }
            }
        },
        "PublicRouteTable": {
            "Type": "AWS::EC2::RouteTable",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "93747341-451f-4c6e-8265-6873b110ae9e"
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "412c8444-e8b8-43eb-8c07-3f822c921e34"
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "c2c64928-4fe4-4640-a449-08cdc9e50d84"
                }
            }
        },
        "PrivateRouteTable": {
            "Type": "AWS::EC2::RouteTable",
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "7a45b627-d06a-4956-9f4b-a79b5e65bc7d"
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "912ef118-eda5-437f-afd7-3f92d83fd70b"
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "d345d815-288f-4446-add0-dd637cc6c57f"
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "4f6ec5cd-f063-4163-8494-31bd55bcb27f"
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "758d2702-7bfd-470e-84a0-5101471dd251"
                }
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "20d8d324-9da6-49f9-9e37-4bd433625c47"
                }
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
                    "Fn::Base64": "#!/bin/bash\nyum update -y \nyum install python3.7 -y\nyum install java-1.8.0-openjdk-devel -y\nyum erase awscli -y\ncd /home/ec2-user\necho \"export PATH=.local/bin:$PATH\" >> .bash_profile\nmkdir kafka\nmkdir mm\ncd kafka\nwget https://archive.apache.org/dist/kafka/2.1.0/kafka_2.12-2.1.0.tgz\ntar -xzf kafka_2.12-2.1.0.tgz\ncd /home/ec2-user\nwget https://bootstrap.pypa.io/get-pip.py\nsu -c \"python3.7 get-pip.py --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install boto3 --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install awscli --user\" -s /bin/sh ec2-user\nchown -R ec2-user ./kafka\nchgrp -R ec2-user ./kafka\nchown -R ec2-user ./mm\nchgrp -R ec2-user ./mm\n"
                }
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "25e7995f-31fc-45b0-b790-42bcb519905a"
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "268a951d-285d-438a-a365-d135a51bd01c"
                }
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
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "01de5e28-2175-45f1-a37f-65e5bd7d9356"
                }
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
                "KafkaVersion": "2.1.0",
                "NumberOfBrokerNodes": 3
            },
            "Metadata": {
                "AWS::CloudFormation::Designer": {
                    "id": "56f5417a-ddff-49c4-9f30-8041824a0601"
                }
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
    },
    "Metadata": {
        "AWS::CloudFormation::Designer": {
            "268a951d-285d-438a-a365-d135a51bd01c": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 60,
                    "y": 930
                },
                "z": 1,
                "embeds": []
            },
            "01de5e28-2175-45f1-a37f-65e5bd7d9356": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 180,
                    "y": 930
                },
                "z": 1,
                "embeds": [],
                "isassociatedwith": [
                    "268a951d-285d-438a-a365-d135a51bd01c"
                ]
            },
            "d2a821e3-5c45-46a4-92fd-09268f72f679": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 300,
                    "y": 930
                },
                "z": 1,
                "embeds": []
            },
            "e191108b-e241-404a-bed2-b2863bcd5235": {
                "size": {
                    "width": 870,
                    "height": 780
                },
                "position": {
                    "x": 60,
                    "y": -140
                },
                "z": 1,
                "embeds": [
                    "758d2702-7bfd-470e-84a0-5101471dd251",
                    "20d8d324-9da6-49f9-9e37-4bd433625c47",
                    "7a45b627-d06a-4956-9f4b-a79b5e65bc7d",
                    "93747341-451f-4c6e-8265-6873b110ae9e",
                    "69ad49b5-ffb5-4019-82dd-1b5433531511",
                    "1a1c22e5-745b-443d-93d6-78c3572de3c4",
                    "be121547-ef38-4d55-a9a9-f67eb35c9cd0",
                    "90cff42d-8429-4a50-b584-5a2ba16651ea"
                ]
            },
            "758d2702-7bfd-470e-84a0-5101471dd251": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 720,
                    "y": 130
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "20d8d324-9da6-49f9-9e37-4bd433625c47": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 720,
                    "y": 250
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "7a45b627-d06a-4956-9f4b-a79b5e65bc7d": {
                "size": {
                    "width": 150,
                    "height": 150
                },
                "position": {
                    "x": 690,
                    "y": -80
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "93747341-451f-4c6e-8265-6873b110ae9e": {
                "size": {
                    "width": 240,
                    "height": 240
                },
                "position": {
                    "x": 390,
                    "y": -80
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [
                    "412c8444-e8b8-43eb-8c07-3f822c921e34"
                ],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "988bff04-9cdd-4ce1-8b5d-59fc3291eae1": {
                "source": {
                    "id": "e191108b-e241-404a-bed2-b2863bcd5235"
                },
                "target": {
                    "id": "d2a821e3-5c45-46a4-92fd-09268f72f679"
                }
            },
            "412c8444-e8b8-43eb-8c07-3f822c921e34": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 420,
                    "y": -20
                },
                "z": 3,
                "parent": "93747341-451f-4c6e-8265-6873b110ae9e",
                "embeds": [],
                "isassociatedwith": [
                    "d2a821e3-5c45-46a4-92fd-09268f72f679"
                ],
                "iscontainedinside": [
                    "93747341-451f-4c6e-8265-6873b110ae9e"
                ],
                "dependson": [
                    "988bff04-9cdd-4ce1-8b5d-59fc3291eae1"
                ]
            },
            "69ad49b5-ffb5-4019-82dd-1b5433531511": {
                "size": {
                    "width": 150,
                    "height": 150
                },
                "position": {
                    "x": 510,
                    "y": 220
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "4f6ec5cd-f063-4163-8494-31bd55bcb27f": {
                "source": {
                    "id": "7a45b627-d06a-4956-9f4b-a79b5e65bc7d"
                },
                "target": {
                    "id": "69ad49b5-ffb5-4019-82dd-1b5433531511"
                }
            },
            "1a1c22e5-745b-443d-93d6-78c3572de3c4": {
                "size": {
                    "width": 150,
                    "height": 150
                },
                "position": {
                    "x": 300,
                    "y": 220
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "d345d815-288f-4446-add0-dd637cc6c57f": {
                "source": {
                    "id": "7a45b627-d06a-4956-9f4b-a79b5e65bc7d"
                },
                "target": {
                    "id": "1a1c22e5-745b-443d-93d6-78c3572de3c4"
                }
            },
            "be121547-ef38-4d55-a9a9-f67eb35c9cd0": {
                "size": {
                    "width": 150,
                    "height": 150
                },
                "position": {
                    "x": 90,
                    "y": 220
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "56f5417a-ddff-49c4-9f30-8041824a0601": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 420,
                    "y": 930
                },
                "z": 1,
                "embeds": []
            },
            "912ef118-eda5-437f-afd7-3f92d83fd70b": {
                "source": {
                    "id": "7a45b627-d06a-4956-9f4b-a79b5e65bc7d"
                },
                "target": {
                    "id": "be121547-ef38-4d55-a9a9-f67eb35c9cd0"
                }
            },
            "90cff42d-8429-4a50-b584-5a2ba16651ea": {
                "size": {
                    "width": 240,
                    "height": 240
                },
                "position": {
                    "x": 90,
                    "y": -80
                },
                "z": 2,
                "parent": "e191108b-e241-404a-bed2-b2863bcd5235",
                "embeds": [
                    "25e7995f-31fc-45b0-b790-42bcb519905a"
                ],
                "iscontainedinside": [
                    "e191108b-e241-404a-bed2-b2863bcd5235"
                ]
            },
            "25e7995f-31fc-45b0-b790-42bcb519905a": {
                "size": {
                    "width": 60,
                    "height": 60
                },
                "position": {
                    "x": 120,
                    "y": -20
                },
                "z": 3,
                "parent": "90cff42d-8429-4a50-b584-5a2ba16651ea",
                "embeds": [],
                "isassociatedwith": [
                    "758d2702-7bfd-470e-84a0-5101471dd251"
                ],
                "iscontainedinside": [
                    "90cff42d-8429-4a50-b584-5a2ba16651ea"
                ]
            },
            "c2c64928-4fe4-4640-a449-08cdc9e50d84": {
                "source": {
                    "id": "93747341-451f-4c6e-8265-6873b110ae9e"
                },
                "target": {
                    "id": "90cff42d-8429-4a50-b584-5a2ba16651ea"
                }
            }
        }
    }
}
```

### Create an MSK Cluster Where You Only Specify Values for the Required Properties<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Only_Specify_Values_for_the_Required_Properties"></a>

#### YAML<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Only_Specify_Values_for_the_Required_Properties--yaml"></a>

```
---
Description: "MSK Cluster with required properties."
Resources:
  TestCluster:
    Type: "AWS::MSK::Cluster"
    Properties:
      ClusterName: "ClusterWithRequiredProperties"
      KafkaVersion: "2.1.0"
      NumberOfBrokerNodes: 3
      BrokerNodeGroupInfo:
        InstanceType: "kafka.m5.large"
        ClientSubnets:
        - "ReplaceWithSubnetId1"
        - "ReplaceWithSubnetId2"
        - "ReplaceWithSubnetId3"
```

```
{
    "Description": "MSK Cluster with required properties.",
    "Resources": {
        "TestCluster": {
            "Type": "AWS::MSK::Cluster",
            "Properties": {
                "ClusterName": "ClusterWithRequiredProperties",
                "KafkaVersion": "2.1.0",
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
---
Description: "MSK Cluster with all properties"
Resources:
  TestCluster:
    Type: "AWS::MSK::Cluster"
    Properties:
      ClusterName: "ClusterWithAllProperties"
      KafkaVersion: "2.1.0"
      NumberOfBrokerNodes: 3
      EnhancedMonitoring: "PER_BROKER"
      EncryptionInfo:
        EncryptionAtRest:
          DataVolumeKMSKeyId: "ReplaceWithKmsKeyArn"
        EncryptionInTransit:
          ClientBroker: "TLS"
          InCluster: true
      ConfigurationInfo:
        Arn: "ReplaceWithConfigurationArn"
        Revision: 1
      ClientAuthentication:
        Tls:
          CertificateAuthorityArnList:
          - "ReplaceWithCAArn"
      Tags:
        MyTagName: "MyTagValue"
      BrokerNodeGroupInfo:
        BrokerAZDistribution: "DEFAULT"
        InstanceType: "kafka.m5.large"
        SecurityGroups:
        - "ReplaceWithSecurityGroupId"
        StorageInfo:
          EBSStorageInfo:
            VolumeSize: 100
        ClientSubnets:
        - "ReplaceWithSubnetId1"
        - "ReplaceWithSubnetId2"
        - "ReplaceWithSubnetId3"
```

```
{
    "Description": "MSK Cluster with all properties",
    "Resources": {
        "TestCluster": {
            "Type": "AWS::MSK::Cluster",
            "Properties": {
                "ClusterName": "ClusterWithAllProperties",
                "KafkaVersion": "2.1.0",
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
                    "MyTagName": "MyTagValue"
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

### Create Two MSK Clusters To Use With Apache MirrorMaker

This YAML shows how to set up two MSK clusters for MirrorMaker. It also sets up the Amazon VPC, subnets, security groups, and IAM roles that are necessary for this example. In addition, it creates an EC2 instance that has Apache Kafka, Java, and the AWS CLI. You can use this EC2 instance to run Apache Kafka tools, including MirrorMaker. You must manually create the MirrorMaker configuration files.

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

        wget https://archive.apache.org/dist/kafka/2.1.0/kafka_2.12-2.1.0.tgz

        tar -xzf kafka_2.12-2.1.0.tgz

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
      KafkaVersion: 2.1.0
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
      KafkaVersion: 2.1.0
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
                    "Fn::Base64": "#!/bin/bash\nyum update -y \nyum install python3.7 -y\nyum install java-1.8.0-openjdk-devel -y\nyum erase awscli -y\ncd /home/ec2-user\necho \"export PATH=.local/bin:$PATH\" >> .bash_profile\nmkdir kafka\nmkdir mm\ncd kafka\nwget https://archive.apache.org/dist/kafka/2.1.0/kafka_2.12-2.1.0.tgz\ntar -xzf kafka_2.12-2.1.0.tgz\ncd /home/ec2-user\nwget https://bootstrap.pypa.io/get-pip.py\nsu -c \"python3.7 get-pip.py --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install boto3 --user\" -s /bin/sh ec2-user\nsu -c \"/home/ec2-user/.local/bin/pip3 install awscli --user\" -s /bin/sh ec2-user\nchown -R ec2-user ./kafka\nchgrp -R ec2-user ./kafka\nchown -R ec2-user ./mm\nchgrp -R ec2-user ./mm\n"
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
                "KafkaVersion": "2.1.0",
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
                "KafkaVersion": "2.1.0",
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
# AWS::EC2::EIPAssociation<a name="aws-properties-ec2-eip-association"></a>

Associates an Elastic IP address with an instance or a network interface\. Before you can use an Elastic IP address, you must allocate it to your account\.

An Elastic IP address is for use in either the EC2\-Classic platform or in a VPC\. For more information, see [Elastic IP Addresses](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html) in the *Amazon Elastic Compute Cloud User Guide*\.

\[EC2\-Classic, VPC in an EC2\-VPC\-only account\] If the Elastic IP address is already associated with a different instance, it is disassociated from that instance and associated with the specified instance\. If you associate an Elastic IP address with an instance that has an existing Elastic IP address, the existing address is disassociated from the instance, but remains allocated to your account\.

\[VPC in an EC2\-Classic account\] If you don't specify a private IP address, the Elastic IP address is associated with the primary IP address\. If the Elastic IP address is already associated with a different instance or a network interface, you get an error unless you allow reassociation\. You cannot associate an Elastic IP address with an instance or network interface that has an existing Elastic IP address\.

## Syntax<a name="aws-properties-ec2-eip-association-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-eip-association-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::EIPAssociation",
  "Properties" : {
      "[AllocationId](#cfn-ec2-eipassociation-allocationid)" : String,
      "[EIP](#cfn-ec2-eipassociation-eip)" : String,
      "[InstanceId](#cfn-ec2-eipassociation-instanceid)" : String,
      "[NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid)" : String,
      "[PrivateIpAddress](#cfn-ec2-eipassociation-PrivateIpAddress)" : String
    }
}
```

### YAML<a name="aws-properties-ec2-eip-association-syntax.yaml"></a>

```
Type: AWS::EC2::EIPAssociation
Properties: 
  [AllocationId](#cfn-ec2-eipassociation-allocationid): String
  [EIP](#cfn-ec2-eipassociation-eip): String
  [InstanceId](#cfn-ec2-eipassociation-instanceid): String
  [NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid): String
  [PrivateIpAddress](#cfn-ec2-eipassociation-PrivateIpAddress): String
```

## Properties<a name="aws-properties-ec2-eip-association-properties"></a>

`AllocationId`  <a name="cfn-ec2-eipassociation-allocationid"></a>
\[EC2\-VPC\] The allocation ID\. This is required for EC2\-VPC\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`EIP`  <a name="cfn-ec2-eipassociation-eip"></a>
The Elastic IP address to associate with the instance\. This is required for EC2\-Classic\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`InstanceId`  <a name="cfn-ec2-eipassociation-instanceid"></a>
The ID of the instance\. This is required for EC2\-Classic\. For EC2\-VPC, you can specify either the instance ID or the network interface ID, but not both\. The operation fails if you specify an instance ID unless exactly one network interface is attached\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-eipassociation-networkinterfaceid"></a>
\[EC2\-VPC\] The ID of the network interface\. If the instance has more than one network interface, you must specify a network interface ID\.  
For EC2\-VPC, you can specify either the instance ID or the network interface ID, but not both\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PrivateIpAddress`  <a name="cfn-ec2-eipassociation-PrivateIpAddress"></a>
\[EC2\-VPC\] The primary or secondary private IP address to associate with the Elastic IP address\. If no private IP address is specified, the Elastic IP address is associated with the primary private IP address\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-ec2-eip-association-return-values"></a>

### Ref<a name="aws-properties-ec2-eip-association-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-ec2-eip-association--examples"></a>

### Associating an Elastic IP address to an instance<a name="aws-properties-ec2-eip-association--examples--Associating_an_Elastic_IP_address_to_an_instance"></a>

The following example creates an instance with two elastic network interfaces \(ENI\)\. The example assumes that you have an existing VPC\.

For additional examples, see [Assigning an Amazon EC2 Elastic IP Using AWS::EC2::EIP Snippet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-ec2.html#scenario-ec2-eip)\.

#### JSON<a name="aws-properties-ec2-eip-association--examples--Associating_an_Elastic_IP_address_to_an_instance--json"></a>

```
  "Resources" : {
    "ControlPortAddress" : {
        "Type" : "AWS::EC2::EIP",
        "Properties" : {
            "Domain" : "vpc"
        }
    },
    "AssociateControlPort" : {
        "Type" : "AWS::EC2::EIPAssociation",
        "Properties" : {
            "AllocationId" : { "Fn::GetAtt" : [ "ControlPortAddress", "AllocationId" ]},
            "NetworkInterfaceId" : { "Ref" : "controlXface" }
        }
    },
    "WebPortAddress" : {
        "Type" : "AWS::EC2::EIP",
        "Properties" : {
            "Domain" : "vpc"
        }
    },
    "AssociateWebPort" : {
        "Type" : "AWS::EC2::EIPAssociation",
        "Properties" : {
            "AllocationId" : { "Fn::GetAtt" : [ "WebPortAddress", "AllocationId" ]},
            "NetworkInterfaceId" : { "Ref" : "webXface" }
        }
    },
    "SSHSecurityGroup" : {
        "Type" : "AWS::EC2::SecurityGroup",
        "Properties" : {
            "VpcId" : { "Ref" : "VpcId" },
            "GroupDescription" : "Enable SSH access via port 22",
            "SecurityGroupIngress" : [ { "IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : "0.0.0.0/0" } ]
        }
    },
    "WebSecurityGroup" : {
        "Type" : "AWS::EC2::SecurityGroup",
        "Properties" : {
            "VpcId" : { "Ref" : "VpcId" },
            "GroupDescription" : "Enable HTTP access via user defined port",
            "SecurityGroupIngress" : [ { "IpProtocol" : "tcp", "FromPort" : 80, "ToPort" : 80, "CidrIp" : "0.0.0.0/0" } ]
        }
    },
    "controlXface" : {
        "Type" : "AWS::EC2::NetworkInterface",
        "Properties" : {
            "SubnetId" : { "Ref" : "SubnetId" },
            "Description" :"Interface for control traffic such as SSH",
            "GroupSet" : [ {"Ref" : "SSHSecurityGroup"} ],
            "SourceDestCheck" : "true",
            "Tags" : [ {"Key" : "Network", "Value" : "Control"}]
        }
    },
    "webXface" : {
        "Type" : "AWS::EC2::NetworkInterface",
        "Properties" : {
            "SubnetId" : { "Ref" : "SubnetId" },
            "Description" :"Interface for web traffic",
            "GroupSet" : [ {"Ref" : "WebSecurityGroup"} ],
            "SourceDestCheck" : "true",
            "Tags" : [ {"Key" : "Network", "Value" : "Web"}]
        }
    },
    "Ec2Instance" : {
        "Type" : "AWS::EC2::Instance",
        "Properties" : {
            "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]},
            "KeyName" : { "Ref" : "KeyName" },
            "NetworkInterfaces" : [ { "NetworkInterfaceId" : {"Ref" : "controlXface"}, "DeviceIndex" : "0" }, { "NetworkInterfaceId" : {"Ref" : "webXface"}, "DeviceIndex" : "1" }],
            "Tags" : [ {"Key" : "Role", "Value" : "Test Instance"}],
            "UserData" : {"Fn::Base64" : { "Fn::Join" : ["",["#!/bin/bash -ex","\n", "\n","yum install ec2-net-utils -y","\n", "ec2ifup eth1","\n", "service httpd start"]]}}
        }
    }
}
```

### <a name="aws-properties-ec2-eip-association--examples--"></a>

#### YAML<a name="aws-properties-ec2-eip-association--examples----yaml"></a>

```
Resources:
  ControlPortAddress:
    Type: AWS::EC2::EIP
    Properties:
      Domain: vpc
  AssociateControlPort:
    Type: AWS::EC2::EIPAssociation
    Properties:
      AllocationId: !GetAtt ControlPortAddress.AllocationId
      NetworkInterfaceId: !Ref controlXface
  WebPortAddress:
    Type: AWS::EC2::EIP
    Properties:
      Domain: vpc
  AssociateWebPort:
    Type: AWS::EC2::EIPAssociation
    Properties:
      AllocationId: !GetAtt WebPortAddress.AllocationId
      NetworkInterfaceId: !Ref webXface
  SSHSecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      VpcId: !Ref VpcId
      GroupDescription: Enable SSH access via port 22
     SecurityGroupIngress:
     - CidrIp: 0.0.0.0/0
       FromPort: 22
       IpProtocol: tcp
       ToPort: 22
  WebSecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      VpcId: !Ref VpcId
      GroupDescription: Enable HTTP access via user defined port
      SecurityGroupIngress:
      - CidrIp: 0.0.0.0/0
        FromPort: 80
        IpProtocol: tcp
        ToPort: 80
  controlXface:
    Type: AWS::EC2::NetworkInterface
    Properties:
      SubnetId: !Ref SubnetId
      Description: Interface for controlling traffic such as SSH
      GroupSet: 
      - !Ref SSHSecurityGroup
      SourceDestCheck: true
      Tags:
      - Key: Network
        Value: Control
  webXface:
    Type: AWS::EC2::NetworkInterface
    Properties:
      SubnetId: !Ref SubnetId
      Description: Interface for controlling traffic such as SSH
      GroupSet: 
      - !Ref WebSecurityGroup
      SourceDestCheck: true
      Tags:
      - Key: Network
        Value: Web
  Ec2Instance:
    Type: AWS::EC2::Instance
    Properties:
      ImageId: !FindInMap [ RegionMap, !Ref 'AWS::Region', AMI ]
      KeyName: !Ref KeyName
      NetworkInterfaces:
      - NetworkInterfaceId: !Ref controlXface
        DeviceIndex: 0
      - NetworkInterfaceId: !Ref webXface
        DeviceIndex: 1
      Tags:
      - Key: Role
        Value: Test Instance
      UserData:
        Fn::Base64: !Sub |
          #!/bin/bash -xe
          yum install ec2-net-utils -y
          ec2ifup eth1
          service httpd start
```
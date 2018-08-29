# AWS::EC2::EIPAssociation<a name="aws-properties-ec2-eip-association"></a>

The AWS::EC2::EIPAssociation resource type associates an Elastic IP address with an Amazon EC2 instance\. The Elastic IP address can be an existing Elastic IP address or an Elastic IP address allocated through an [AWS::EC2::EIP resource](aws-properties-ec2-eip.md)\.

For more information EC2\-Classic and EC2\-VPC, see [AssociateAddress](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AssociateAddress.html) in the *Amazon EC2 API Reference*\.

**Topics**
+ [Syntax](#aws-resource-ec2-eipassociation-syntax)
+ [Properties](#aws-resource-ec2-eip-association-prop)
+ [Return Values](#w3ab2c21c10d396c13)
+ [Examples](#w3ab2c21c10d396c15)

## Syntax<a name="aws-resource-ec2-eipassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-eipassociation-syntax.json"></a>

```
{
   "Type": "AWS::EC2::EIPAssociation",
   "Properties": {
      "[AllocationId](#cfn-ec2-eipassociation-allocationid)": String,
      "[EIP](#cfn-ec2-eipassociation-eip)": String,
      "[InstanceId](#cfn-ec2-eipassociation-instanceid)": String,
      "[NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid)": String,
      "[PrivateIpAddress](#cfn-ec2-eipassociation-PrivateIpAddress)": String
   }
}
```

### YAML<a name="aws-resource-ec2-eipassociation-syntax.yaml"></a>

```
Type: "AWS::EC2::EIPAssociation"
Properties:
  [AllocationId](#cfn-ec2-eipassociation-allocationid): String
  [EIP](#cfn-ec2-eipassociation-eip): String
  [InstanceId](#cfn-ec2-eipassociation-instanceid): String
  [NetworkInterfaceId](#cfn-ec2-eipassociation-networkinterfaceid): String
  [PrivateIpAddress](#cfn-ec2-eipassociation-PrivateIpAddress): String
```

## Properties<a name="aws-resource-ec2-eip-association-prop"></a>

`AllocationId`  <a name="cfn-ec2-eipassociation-allocationid"></a>
\[EC2\-VPC\] Allocation ID for the VPC Elastic IP address you want to associate with an Amazon EC2 instance in your VPC\.  
*Required*: Conditional\. Required for EC2\-VPC\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you also change the `InstanceId` or `NetworkInterfaceId` property\. If not, update requires [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`EIP`  <a name="cfn-ec2-eipassociation-eip"></a>
Elastic IP address that you want to associate with the Amazon EC2 instance specified by the `InstanceId` property\. You can specify an existing Elastic IP address or a reference to an Elastic IP address allocated with a [AWS::EC2::EIP resource](aws-properties-ec2-eip.md)\.  
*Required*: Conditional\. Required for EC2\-Classic\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you also change the `InstanceId` or `NetworkInterfaceId` property\. If not, update requires [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`InstanceId`  <a name="cfn-ec2-eipassociation-instanceid"></a>
Instance ID of the Amazon EC2 instance that you want to associate with the Elastic IP address specified by the EIP property\. If the instance has more than one network interface, you must specify a network interface ID\.  
*Required*: Conditional\. If you specify the `EIP` property, you must specify this property\. If you specify the `AllocationId` property, you must specify this property or the `NetworkInterfaceId` property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you also change the `AllocationId` or `EIP` property\. If not, update requires [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`NetworkInterfaceId`  <a name="cfn-ec2-eipassociation-networkinterfaceid"></a>
\[EC2\-VPC\] The ID of the network interface to associate with the Elastic IP address\. If the instance has more than one network interface, you must specify a network interface ID\.  
*Required*: Conditional\. If you specify the `AllocationId` property, you must specify this property or the `InstanceId` property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you also change the `AllocationId` or `EIP` property\. If not, update requires [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`PrivateIpAddress`  <a name="cfn-ec2-eipassociation-PrivateIpAddress"></a>
\[EC2\-VPC\] The private IP address that you want to associate with the Elastic IP address\. The private IP address is restricted to the primary and secondary private IP addresses that are associated with the network interface\. By default, the private IP address that is associated with the EIP is the primary private IP address of the network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d396c13"></a>

### Ref<a name="w3ab2c21c10d396c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d396c15"></a>

The following example creates an instance with two elastic network interfaces \(ENI\)\. The example assumes that you have an existing VPC\.

For additional examples, see [Assigning an Amazon EC2 Elastic IP Using AWS::EC2::EIP Snippet](quickref-ec2.md#scenario-ec2-eip)\.

### JSON<a name="w3ab2c21c10d396c15b6"></a>

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
        "NetworkInterfaces" : [ { "NetworkInterfaceId" : {"Ref" : "controlXface"}, "DeviceIndex" : "0" },
								{ "NetworkInterfaceId" : {"Ref" : "webXface"}, "DeviceIndex" : "1" }],
        "Tags" : [ {"Key" : "Role", "Value" : "Test Instance"}],
        "UserData" : {"Fn::Base64" : { "Fn::Join" : ["",[
			"#!/bin/bash -ex","\n",
            "\n","yum install ec2-net-utils -y","\n",
			"ec2ifup eth1","\n",
			"service httpd start"]]}
		}
	  }
    }
  }
```

### YAML<a name="w3ab2c21c10d396c15b8"></a>

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
        -
          Key: Network
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
        -
          Key: Network
          Value: Web
  Ec2Instance:
    Type: AWS::EC2::Instance
    Properties:
      ImageId: !FindInMap [ RegionMap, !Ref 'AWS::Region', AMI ]
      KeyName: !Ref KeyName
      NetworkInterfaces:
        -
          NetworkInterfaceId: !Ref controlXface
          DeviceIndex: 0
        -
          NetworkInterfaceId: !Ref webXface
          DeviceIndex: 1
      Tags:
        -
          Key: Role
          Value: Test Instance
      UserData:
        Fn::Base64: !Sub |
          #!/bin/bash -xe
          yum install ec2-net-utils -y
          ec2ifup eth1
          service httpd start
```
# Amazon EC2 template snippets<a name="quickref-ec2"></a>

## EC2 block device mapping examples<a name="scenario-ec2-bdm"></a>

### EC2 instance with block device mapping<a name="w7739ab1c27c22c39b3b2"></a>

#### JSON<a name="quickref-ec2-example-1.json"></a>

```
    "Ec2Instance" : {
      "Type" : "AWS::EC2::Instance", 
      "Properties" : {
        "ImageId" : { "Fn::FindInMap" : [ "AWSRegionArch2AMI", { "Ref" : "AWS::Region" }, 
                                          { "Fn::FindInMap" : [ "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch" ] } ] },
        "KeyName" : { "Ref" : "KeyName" },
        "InstanceType" : { "Ref" : "InstanceType" },
        "SecurityGroups" : [{ "Ref" : "Ec2SecurityGroup" }],
        "BlockDeviceMappings" : [
          {
            "DeviceName" : "/dev/sda1",
            "Ebs" : { "VolumeSize" : "50" } 
          },{
            "DeviceName" : "/dev/sdm",
            "Ebs" : { "VolumeSize" : "100" }
          }
        ]
      }
    }
```

#### YAML<a name="quickref-ec2-example-1.yaml"></a>

```
EC2Instance:
    Type: AWS::EC2::Instance
    Properties:
        ImageId: !FindInMap [ AWSRegionArch2AMI, !Ref 'AWS::Region' , !FindInMap [ AWSInstanceType2Arch, !Ref InstanceType, Arch ] ]
        KeyName: !Ref KeyName
        InstanceType: !Ref InstanceType
        SecurityGroups:
        - !Ref Ec2SecurityGroup
        BlockDeviceMappings:
        -
          DeviceName: /dev/sda1
          Ebs:
            VolumeSize: 50
        -
          DeviceName: /dev/sdm
          Ebs:
            VolumeSize: 100
```

### EC2 instance with ephemeral drives<a name="w7739ab1c27c22c39b3b4"></a>

#### JSON<a name="quickref-ec2-example-2.json"></a>

```
    "Ec2Instance" : {
      "Type" : "AWS::EC2::Instance", 
      "Properties" : {
        "ImageId" : { "Fn::FindInMap" : [ "AWSRegionArch2AMI", { "Ref" : "AWS::Region" }, "PV64" ]},
        "KeyName" : { "Ref" : "KeyName" },
        "InstanceType" : "m1.small",
        "SecurityGroups" : [{ "Ref" : "Ec2SecurityGroup" }],
        "BlockDeviceMappings" : [
          {
            "DeviceName"  : "/dev/sdc",
            "VirtualName" : "ephemeral0"
          }
        ]
      }
    }
```

#### YAML<a name="quickref-ec2-example-2.yaml"></a>

```
EC2Instance:
	Type: AWS::EC2::Instance
	Properties:
	  ImageId: !FindInMap [ AWSRegionArch2AMI, !Ref 'AWS::Region', PV64 ]
	  KeyName: !Ref KeyName
	  InstanceType: m1.small
	  SecurityGroups:
	  - !Ref Ec2SecurityGroup
	  BlockDeviceMappings:
	 	  -
	      DeviceName: /dev/sdc
	      VirtualName: ephemeral0
```

## Assigning an Amazon EC2 elastic IP using AWS::EC2::EIP snippet<a name="scenario-ec2-eip"></a>

This example shows how to allocate an Amazon EC2 Elastic IP address and assign it to an Amazon EC2 instance using a [AWS::EC2::EIP resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html)\.

### JSON<a name="quickref-ec2-example-3.json"></a>

```
1. "MyEIP" : {
2.  "Type" : "AWS::EC2::EIP",
3.  "Properties" : {
4.      "InstanceId" : { "Ref" : "logical name of an AWS::EC2::Instance resource" }
5.  }
6. }
```

### YAML<a name="quickref-ec2-example-3.yaml"></a>

```
1. MyEIP:
2.   Type: AWS::EC2::EIP
3.   Properties:
4.     InstanceId: !Ref Logical name of an AWS::EC2::Instance resource
```

## Assigning an existing elastic IP to an amazon EC2 instance using AWS::EC2::EIPAssociation snippet<a name="scenario-ec2-eip-association"></a>

This example shows how to assign an existing Amazon EC2 Elastic IP address to an Amazon EC2 instance using an [AWS::EC2::EIPAssociation resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip-association.html)\.

### JSON<a name="quickref-ec2-example-4.json"></a>

```
1. "IPAssoc" : {
2.          "Type" : "AWS::EC2::EIPAssociation",
3.          "Properties" : {
4.              "InstanceId" : { "Ref" : "logical name of an AWS::EC2::Instance resource" },
5.              "EIP" : "existing Elastic IP address"
6.          }
7.      }
```

### YAML<a name="quickref-ec2-example-4.yaml"></a>

```
1. IPAssoc:
2.   Type: AWS::EC2::EIPAssociation
3.   Properties:
4.     InstanceId: !Ref Logical name of an AWS::EC2::Instance resource
5.     EIP: existing Elastic IP Address
```

## Assigning an existing VPC elastic IP to an Amazon EC2 instance using AWS::EC2::EIPAssociation snippet<a name="scenario-ec2-eip-association-vpc"></a>

This example shows how to assign an existing VPC Elastic IP address to an Amazon EC2 instance using an [AWS::EC2::EIPAssociation resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip-association.html)\.

### JSON<a name="quickref-ec2-example-5.json"></a>

```
1. "VpcIPAssoc" : {
2.          "Type" : "AWS::EC2::EIPAssociation",
3.          "Properties" : {
4.              "InstanceId" : { "Ref" : "logical name of an AWS::EC2::Instance resource" },
5.              "AllocationId" : "existing VPC Elastic IP allocation ID"
6.          }
7.      }
```

### YAML<a name="quickref-ec2-example-5.yaml"></a>

```
1. VpcIPAssoc:
2.   Type: AWS::EC2::EIPAssociation
3.   Properties:
4.     InstanceId: !Ref Logical name of an AWS::EC2::Instance resource
5.     AllocationId: Existing VPC Elastic IP allocation ID
```

## Elastic network interface \(ENI\) template snippets<a name="cfn-template-snippets-eni"></a>

### VPC\_EC2\_Instance\_With\_ENI<a name="w7739ab1c27c22c39c13b3"></a>

Sample template showing how to create an instance with two elastic network interface \(ENI\)\. The sample assumes you have already created a VPC\. 

#### JSON<a name="cfn-template-snippets-eni-example-1.json"></a>

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

#### YAML<a name="cfn-template-snippets-eni-example-1.yaml"></a>

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

## Amazon EC2 instance resource<a name="scenario-ec2-instance"></a>

This snippet shows a simple AWS::EC2::Instance resource\.

### JSON<a name="quickref-ec2-example-6.json"></a>

```
1. "MyInstance" : {
2.  "Type" : "AWS::EC2::Instance",
3.  "Properties" : {
4.      "AvailabilityZone" : "us-east-1a",
5.      "ImageId" : "ami-0ff8a91507f77f867"
6.  }
7. }
```

### YAML<a name="quickref-ec2-example-6.yaml"></a>

```
1. MyInstance:
2.   Type: AWS::EC2::Instance
3.   Properties:
4.     AvailabilityZone: us-east-1a
5.     ImageId: ami-0ff8a91507f77f867
```

## Amazon EC2 instance with Volume, Tag, and UserData properties<a name="scenario-ec2-instance-with-vol-and-tags"></a>

This snippet shows an AWS::EC2::Instance resource with one Amazon EC2 volume, one tag, and a user data property\. An AWS::EC2::SecurityGroup resource, an AWS::SNS::Topic resource, and an AWS::EC2::Volume resource all must be defined in the same template\. Also, the reference to `KeyName` is a parameters that must be defined in the Parameters section of the template\.

### JSON<a name="quickref-ec2-example-7.json"></a>

```
 1. "MyInstance" : {
 2.  "Type" : "AWS::EC2::Instance",
 3.  "Properties" : {
 4.      "KeyName" : { "Ref" : "KeyName" },
 5.      "SecurityGroups" : [ {
 6.          "Ref" : "logical name of AWS::EC2::SecurityGroup resource"
 7.      } ],
 8.      "UserData" : {
 9.          "Fn::Base64" : {
10.              "Fn::Join" : [ ":", [
11.                  "PORT=80",
12.                  "TOPIC=", {
13.                      "Ref" : "logical name of an AWS::SNS::Topic resource"
14.                  } ]
15.              ]
16.          }
17.       },
18.      "InstanceType" : "m1.small",
19.      "AvailabilityZone" : "us-east-1a",
20.      "ImageId" : "ami-0ff8a91507f77f867",
21.      "Volumes" : [
22.         { "VolumeId" : {
23.              "Ref" : "logical name of AWS::EC2::Volume resource"
24.         },
25.         "Device" : "/dev/sdk" }
26.      ],
27. 
28.      "Tags" : [ {
29.          "Key" : "Name",
30.          "Value" : "MyTag"
31.      } ]
32.  }
33. }
```

### YAML<a name="quickref-ec2-example-7.yaml"></a>

```
 1. MyInstance:
 2.   Type: AWS::EC2::Instance
 3.   Properties:
 4.     KeyName: !Ref KeyName
 5.     SecurityGroups:
 6.     - !Ref logical name of AWS::EC2::SecurityGroup resource
 7.     UserData:
 8.       Fn::Base64: !Sub |
 9.         PORT=80
10.         TOPIC=${ logical name of an AWS::SNS::Topic resource }
11.     InstanceType: m1.small
12.     AvailabilityZone: us-east-1a
13.     ImageId: ami-0ff8a91507f77f867
14.     Volumes:
15.       -
16.         VolumeId: !Ref logical name of AWS::EC2::Volume resource
17.         Device: /dev/sdk
18.     Tags:
19.       -
20.         Key: Name
21.         Value: MyTag
```

## Amazon EC2 instance resource with an Amazon SimpleDB Domain<a name="scenario-ec2-with-sdb-domain"></a>

This snippet shows an AWS::EC2::Instance resource with an Amazon SimpleDB domain specified in the UserData\.

### JSON<a name="quickref-ec2-example-8.json"></a>

```
 1. "MyInstance" : {
 2.  "Type" : "AWS::EC2::Instance",
 3.  "Properties" : {
 4.      "UserData" : {
 5.          "Fn::Base64" : {
 6.              "Fn::Join" : [ "",
 7.                  [ "Domain=", {
 8.                      "Ref" : "logical name of an AWS::SDB::Domain resource"
 9.                  } ]
10.              ]
11.          }
12.       },
13.      "AvailabilityZone" : "us-east-1a",
14.      "ImageId" : "ami-0ff8a91507f77f867"
15.  }
16. }
```

### YAML<a name="quickref-ec2-example-8.yaml"></a>

```
1. MyInstance:
2.   Type: AWS::EC2::Instance
3.   Properties:
4.     UserData:
5.       Fn::Base64: !Sub |
6.         Domain=${ logical name of an AWS::SDB::Domain resource }
7.     AvailabilityZone: us-east-1a
8.     ImageId: ami-0ff8a91507f77f867
```

## Amazon EC2 security group resource with two CIDR range ingress rules<a name="scenario-ec2-security-group-two-ports"></a>

This snippet shows an AWS::EC2::SecurityGroup resource that describes two ingress rules giving access to a specified CIDR range for the TCP protocol on the specified ports\.

### JSON<a name="quickref-ec2-example-9.json"></a>

```
 1. "ServerSecurityGroup" : {
 2.  "Type" : "AWS::EC2::SecurityGroup",
 3.  "Properties" : {
 4.      "GroupDescription" : "allow connections from specified CIDR ranges",
 5.      "SecurityGroupIngress" : [
 6.          {
 7.              "IpProtocol" : "tcp",
 8.              "FromPort" : "80",
 9.              "ToPort" : "80",
10.              "CidrIp" : "0.0.0.0/0"
11.          },{
12.              "IpProtocol" : "tcp",
13.              "FromPort" : "22",
14.              "ToPort" : "22",
15.              "CidrIp" : "192.168.1.1/32"
16.          }
17.      ]
18.  }
19. }
```

### YAML<a name="quickref-ec2-example-9.yaml"></a>

```
 1. ServerSecurityGroup:
 2.   Type: AWS::EC2::SecurityGroup
 3.   Properties:
 4.     GroupDescription: allow connections from specified CIDR ranges
 5.     SecurityGroupIngress:
 6.     - IpProtocol: tcp
 7.       FromPort: 80
 8.       ToPort: 80
 9.       CidrIp: 0.0.0.0/0
10.     - IpProtocol: tcp
11.       FromPort: 22
12.       ToPort: 22
13.       CidrIp: 192.168.1.1/32
```

## Amazon EC2 security group resource with two security group ingress rules<a name="scenario-ec2-security-group-rule"></a>

This snippet shows an AWS::EC2::SecurityGroup resource that describes two security group ingress rules\. The first ingress rule grants access to the existing security group myadminsecuritygroup, which is owned by the 1234\-5678\-9012 AWS account, for the TCP protocol on port 22\. The second ingress rule grants access to the security group mysecuritygroupcreatedincfn for TCP on port 80\. This ingress rule uses the Ref intrinsic function to refer to a security group \(whose logical name is mysecuritygroupcreatedincfn\) created in the same template\. You must declare a value for both the `SourceSecurityGroupName` and `SourceSecurityGroupOwnerId` properties\.

### JSON<a name="quickref-ec2-example-10.json"></a>

```
 1. "ServerSecurityGroupBySG" : {
 2.  "Type" : "AWS::EC2::SecurityGroup",
 3.  "Properties" : {
 4.      "GroupDescription" : "allow connections from specified source security group",
 5.      "SecurityGroupIngress" : [
 6.          {
 7.             "IpProtocol" : "tcp",
 8.             "FromPort" : "22",
 9.             "ToPort" : "22",
10.             "SourceSecurityGroupName" : "myadminsecuritygroup",
11.             "SourceSecurityGroupOwnerId" : "123456789012"
12.          },
13.          {
14.             "IpProtocol" : "tcp",
15.             "FromPort" : "80",
16.             "ToPort" : "80",
17.             "SourceSecurityGroupName" : {"Ref" : "mysecuritygroupcreatedincfn"}
18.          }
19.      ]
20.  }
21. }
```

### YAML<a name="quickref-ec2-example-10.yaml"></a>

```
 1. ServerSecurityGroupBySG:
 2.   Type: AWS::EC2::SecurityGroup
 3.   Properties:
 4.     GroupDescription: allow connections from specified source security group
 5.     SecurityGroupIngress:
 6.     - IpProtocol: tcp
 7.       FromPort: 80
 8.       ToPort: 80
 9.       SourceSecurityGroupName: myadminsecuritygroup
10.       SourceSecurityGroupOwnerId: 123456789012
11.     - IpProtocol: tcp
12.       FromPort: 80
13.       ToPort: 80
14.       SourceSecurityGroupName: !Ref mysecuritygroupcreatedincfn
```

## Amazon EC2 security group resource with LoadBalancer ingress rule<a name="scenario-ec2-security-group-elbingress"></a>

This template shows an AWS::EC2::SecurityGroup resource that contains a security group ingress rule that grants access to the LoadBalancer myELB for TCP on port 80\. Note that the rule uses the `SourceSecurityGroup.OwnerAlias` and `SourceSecurityGroup.GroupName` properties of the myELB resource to specify the source security group of the LoadBalancer\.

### JSON<a name="quickref-ec2-example-11.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "myELB": {
            "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
            "Properties": {
                "AvailabilityZones": [
                    "eu-west-1a"
                ],
                "Listeners": [
                    {
                        "LoadBalancerPort": "80",
                        "InstancePort": "80",
                        "Protocol": "HTTP"
                    }
                ]
            }
        },
        "myELBIngressGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "ELB ingress group",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 80,
                        "ToPort": 80,
                        "SourceSecurityGroupOwnerId": {
                            "Fn::GetAtt": [
                                "myELB",
                                "SourceSecurityGroup.OwnerAlias"
                            ]
                        },
                        "SourceSecurityGroupName": {
                            "Fn::GetAtt": [
                                "myELB",
                                "SourceSecurityGroup.GroupName"
                            ]
                        }
                    }
                ]
            }
        }
    }
}
```

### YAML<a name="quickref-ec2-example-11.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myELB:
    Type: AWS::ElasticLoadBalancing::LoadBalancer
    Properties:
      AvailabilityZones:
        - eu-west-1a
      Listeners:
        - LoadBalancerPort: '80'
          InstancePort: '80'
          Protocol: HTTP
  myELBIngressGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: ELB ingress group
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          SourceSecurityGroupOwnerId: !GetAtt myELB.SourceSecurityGroup.OwnerAlias
          SourceSecurityGroupName: !GetAtt myELB.SourceSecurityGroup.GroupName
```

## Using AWS::EC2::SecurityGroupIngress to create mutually referencing Amazon EC2 security group resources<a name="scenario-ec2-security-group-ingress"></a>

This snippet shows two AWS::EC2::SecurityGroupIngress resources that add mutual ingress rules to the EC2 security groups SGroup1 and SGroup2\. The SGroup1Ingress resource enables ingress from SGroup2 through TCP/IP port 80 to SGroup1\. The SGroup2Ingress resource enables ingress from SGroup1 through TCP/IP port 80 to SGroup2\. 

**Note**  
If you are using an Amazon VPC, use the `AWS::EC2::SecurityGroup` resource and specify the `VpcId` property\.

### JSON<a name="quickref-ec2-example-12.json"></a>

```
 1.         "SGroup1" : {
 2.          "Type" : "AWS::EC2::SecurityGroup",
 3.          "Properties" : {
 4.              "GroupDescription" : "EC2 Instance access"
 5.          }
 6.      },
 7.      "SGroup2" : {
 8.          "Type" : "AWS::EC2::SecurityGroup",
 9.          "Properties" : {
10.              "GroupDescription" : "EC2 Instance access"
11.          }
12.      },
13.      "SGroup1Ingress" : {
14.          "Type" : "AWS::EC2::SecurityGroupIngress",
15.          "Properties" : {
16.              "GroupName" : { "Ref" : "SGroup1" },
17.              "IpProtocol" : "tcp",
18.              "ToPort" : "80",
19.              "FromPort" : "80",
20.              "SourceSecurityGroupName" : { "Ref" : "SGroup2" }
21.          }
22.      },
23.      "SGroup2Ingress" : {
24.          "Type" : "AWS::EC2::SecurityGroupIngress",
25.          "Properties" : {
26.              "GroupName" : { "Ref" : "SGroup2" },
27.              "IpProtocol" : "tcp",
28.              "ToPort" : "80",
29.              "FromPort" : "80",
30.              "SourceSecurityGroupName" : { "Ref" : "SGroup1" }
31.          }
32.      }
```

### YAML<a name="quickref-ec2-example-12.yaml"></a>

```
 1. SGroup1:
 2.   Type: AWS::EC2::SecurityGroup
 3.   Properties:
 4.     GroupDescription: EC2 Instance access
 5. SGroup2:
 6.   Type: AWS::EC2::SecurityGroup
 7.   Properties:
 8.     GroupDescription: EC2 Instance access
 9. SGroup1Ingress:
10.   Type: AWS::EC2::SecurityGroupIngress
11.   Properties:
12.     GroupName: !Ref SGroup1
13.     IpProtocol: tcp
14.     ToPort: 80
15.     FromPort: 80
16.     SourceSecurityGroupName: !Ref SGroup2
17. SGroup2Ingress:
18.   Type: AWS::EC2::SecurityGroupIngress
19.   Properties:
20.     GroupName: !Ref SGroup2
21.     IpProtocol: tcp
22.     ToPort: 80
23.     FromPort: 80
24.     SourceSecurityGroupName: !Ref SGroup1
```

## Amazon EC2 volume resource<a name="scenario-ec2-volume"></a>

This snippet shows a simple Amazon EC2 volume resource with a DeletionPolicy attribute set to Snapshot\. With the Snapshot DeletionPolicy set, AWS CloudFormation will take a snapshot of this volume before deleting it during stack deletion\. Make sure you specify a value for `SnapShotId`, or a value for `Size`, but not both\. Remove the one you don't need\.

### JSON<a name="quickref-ec2-example-13.json"></a>

```
1. "MyEBSVolume" : {
2.  "Type" : "AWS::EC2::Volume",
3.  "Properties" : {
4.      "Size" : "specify a size if no SnapShotId",
5.      "SnapshotId" : "specify a SnapShotId if no Size",
6.      "AvailabilityZone" : { "Ref" : "AvailabilityZone" }
7.  },
8.  "DeletionPolicy" : "Snapshot"
9. }
```

### YAML<a name="quickref-ec2-example-13.yaml"></a>

```
1. MyEBSVolume:
2.   Type: AWS::EC2::Volume
3.   Properties:
4.     Size: specify a size if no SnapshotId
5.     SnapshotId: specify a SnapShotId if no Size
6.     AvailabilityZone: !Ref AvailabilityZone
7.   DeletionPolicy: Snapshot
```

## Amazon EC2 VolumeAttachment resource<a name="scenario-ec2-volumeattachment"></a>

This snippet shows the following resources: an Amazon EC2 instance using an Amazon Linux AMI from the US\-East \(Northern Virginia\) Region, an EC2 security group that allows SSH access to IP addresses, a new Amazon EBS volume sized at 100 GB and in the same Availability Zone as the EC2 instance, and a volume attachment that attaches the new volume to the EC2 instance\. 

### JSON<a name="quickref-ec2-example-14.json"></a>

```
 1. "Resources" : {
 2.  "Ec2Instance" : {
 3.    "Type" : "AWS::EC2::Instance",
 4.    "Properties" : {
 5.      "SecurityGroups" : [ { "Ref" : "InstanceSecurityGroup" } ],
 6.      "ImageId" : "ami-0ff8a91507f77f867"
 7.    }
 8.  },
 9. 
10.  "InstanceSecurityGroup" : {
11.    "Type" : "AWS::EC2::SecurityGroup",
12.    "Properties" : {
13.      "GroupDescription" : "Enable SSH access via port 22",
14.      "SecurityGroupIngress" : [ {
15.        "IpProtocol" : "tcp",
16.        "FromPort" : "22",
17.        "ToPort" : "22",
18.        "CidrIp" : "0.0.0.0/0"
19.      } ]
20.    }
21.  },
22. 
23.  "NewVolume" : {
24.    "Type" : "AWS::EC2::Volume",
25.    "Properties" : {
26.      "Size" : "100",
27.      "AvailabilityZone" : { "Fn::GetAtt" : [ "Ec2Instance", "AvailabilityZone" ]}
28.    }
29.  },
30. 
31.  "MountPoint" : {
32.    "Type" : "AWS::EC2::VolumeAttachment",
33.    "Properties" : {
34.      "InstanceId" : { "Ref" : "Ec2Instance" },
35.      "VolumeId"  : { "Ref" : "NewVolume" },
36.      "Device" : "/dev/sdh"
37.    }
38.  }
39. }
```

### YAML<a name="quickref-ec2-example-14.yaml"></a>

```
 1. Resources:
 2.   Ec2Instance:
 3.     Type: AWS::EC2::Instance
 4.     Properties:
 5.       SecurityGroups:
 6.       - !Ref InstanceSecurityGroup
 7.       ImageId: ami-0ff8a91507f77f867
 8.   InstanceSecurityGroup:
 9.     Type: AWS::EC2::SecurityGroup
10.     Properties:
11.       GroupDescription: Enable SSH access via port 22
12.       SecurityGroupIngress:
13.       - IpProtocol: tcp
14.         FromPort: 22
15.         ToPort: 22
16.         CidrIp: 0.0.0.0/0
17.   NewVolume:
18.     Type: AWS::EC2::Volume
19.     Properties:
20.       Size: 100
21.       AvailabilityZone: !GetAtt Ec2Instance.AvailabilityZone
22.   MountPoint:
23.     Type: AWS::EC2::VolumeAttachment
24.     Properties:
25.       InstanceId: !Ref Ec2Instance
26.       VolumeId: !Ref NewVolume
27.       Device: /dev/sdh
```

## Amazon EC2 instance in a default VPC security group<a name="using-cfn-getatt-default-values"></a>

Whenever you create a VPC, AWS automatically creates default resources for that VPC, such as a security group\. However, when you define a VPC in AWS CloudFormation templates, you don't yet have the physical IDs of those default resources\. To obtain the IDs, use the [`Fn::GetAtt`](intrinsic-function-reference-getatt.md) intrinsic function\. That way, you can use the default resources instead of creating new ones in your template\. For example, the following template snippet associates the default security group of the `myVPC` VPC with the `myInstance` Amazon EC2 instance\.

### JSON<a name="quickref-ec2-example-15.json"></a>

```
"myVPC": {
  "Type": "AWS::EC2::VPC",
  "Properties": {
    "CidrBlock": {"Ref": "myVPCCIDRRange"},
    "EnableDnsSupport": false,
    "EnableDnsHostnames": false,
    "InstanceTenancy": "default"
  }
},
"myInstance" : {
  "Type" : "AWS::EC2::Instance",
  "Properties" : {
    "ImageId": {
      "Fn::FindInMap": ["AWSRegionToAMI",{"Ref": "AWS::Region"},"64"]
    },
    "SecurityGroupIds" : [{"Fn::GetAtt": ["myVPC", "DefaultSecurityGroup"]}],
    "SubnetId" : {"Ref" : "mySubnet"}
  }
}
```

### YAML<a name="quickref-ec2-example-15.yaml"></a>

```
myVPC:
  Type: AWS::EC2::VPC
  Properties:
    CidrBlock: !Ref myVPCCIDRRange
    EnableDnsSupport: false
    EnableDnsHostnames: false
    InstanceTenancy: default
myInstance:
  Type: AWS::EC2::Instance
  Properties:
    ImageId: !FindInMap [ AWSRegionToAMI , !Ref 'AWS::Region', 64 ]
    SecurityGroupIds:
    - !GetAtt myVPC.DefaultSecurityGroup
    SubnetId: !Ref mySubnet
```

## Amazon EC2 route with egress\-only Internet gateway<a name="quickref-ec2-route-egressonlyinternetgateway"></a>

The following template sets up an egress\-only Internet gateway that's used with an EC2 route\.

### JSON<a name="quickref-ec2-example-16.json"></a>

```
{
    "Resources": {
        "DefaultIpv6Route": {
            "Properties": {
                "DestinationIpv6CidrBlock": "::/0",
                "EgressOnlyInternetGatewayId": {
                    "Ref": "EgressOnlyInternetGateway"
                },
                "RouteTableId": {
                    "Ref": "RouteTable"
                }
            },
            "Type": "AWS::EC2::Route"
        },
        "EgressOnlyInternetGateway": {
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            },
            "Type": "AWS::EC2::EgressOnlyInternetGateway"
        },
        "RouteTable": {
            "Properties": {
                "VpcId": {
                    "Ref": "VPC"
                }
            },
            "Type": "AWS::EC2::RouteTable"
        },
        "VPC": {
            "Properties": {
                "CidrBlock": "10.0.0.0/16"
            },
            "Type": "AWS::EC2::VPC"
        }
    }
}
```

### YAML<a name="quickref-ec2-example-16.yaml"></a>

```
Resources:
  DefaultIpv6Route:
    Type: AWS::EC2::Route
    Properties:
      DestinationIpv6CidrBlock: "::/0"
      EgressOnlyInternetGatewayId: !Ref EgressOnlyInternetGateway
      RouteTableId: !Ref RouteTable
  EgressOnlyInternetGateway:
    Type: AWS::EC2::EgressOnlyInternetGateway
    Properties:
      VpcId: !Ref VPC
  RouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId: !Ref VPC
  VPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/16
```
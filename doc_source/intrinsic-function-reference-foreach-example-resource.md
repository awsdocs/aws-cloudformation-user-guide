# `Fn::ForEach` in the `Resources` section<a name="intrinsic-function-reference-foreach-example-resource"></a>

These examples demonstrate using the `Fn::ForEach` intrinsic function in the [Resources](resources-section-structure.md) section\.

**Topics**
+ [Replicate an Amazon SNS resource](#intrinsic-function-reference-foreach-example-replicate-resource)
+ [Replicate an Amazon DynamoDB resource](#intrinsic-function-reference-foreach-example-replicate-ddb-resource)
+ [Replicate multiple resources](#intrinsic-function-reference-foreach-example-replicate-multiple-resources)
+ [Replicate multiple resources using a nested `Fn::ForEach` loops](#intrinsic-function-reference-foreach-example-nested-loop-resources)
+ [Reference replicated properties for an Amazon EC2 resource](#intrinsic-function-reference-foreach-example-reference-replicated-resource)
+ [Replicate properties for an Amazon EC2 resource](#intrinsic-function-reference-foreach-example-replicate-resource-properties)

## Replicate an Amazon SNS resource<a name="intrinsic-function-reference-foreach-example-replicate-resource"></a>

This example snippet returns a list of four Amazon SNS topics, with the logical ID corresponding to the items in the collection \(`Success`, `Failure`, `Timeout`, `Unknown`\), with a matching `TopicName` and `FifoTopic` set to `true`\.

### JSON<a name="intrinsic-function-reference-foreach-example-replicate-resource.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Transform": "AWS::LanguageExtensions",
    "Resources": {
        "Fn::ForEach::Topics": [
            "TopicName",
            ["Success", "Failure", "Timeout", "Unknown"],
            {
                "SnsTopic${TopicName}": {
                    "Type": "AWS::SNS::Topic",
                    "Properties": {
                        "TopicName": {
                            "Ref": "TopicName"
                        },
                        "FifoTopic": true
                    }
                }
            }
        ]
    }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-replicate-resource.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  'Fn::ForEach::Topics':
    - TopicName
    - - Success
      - Failure
      - Timeout
      - Unknown
    - 'SnsTopic${TopicName}':
        Type: 'AWS::SNS::Topic'
        Properties:
          TopicName: !Ref TopicName
          FifoTopic: true
```

The transformed template will be equivalent to the following template:

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "SnsTopicSuccess": {
            "Type": "AWS::SNS::Topic",
            "Properties": {
                "TopicName": "Success",
                "FifoTopic": true
            }
        },
        "SnsTopicFailure": {
            "Type": "AWS::SNS::Topic",
            "Properties": {
                "TopicName": "Failure",
                "FifoTopic": true
            }
        },
        "SnsTopicTimeout": {
            "Type": "AWS::SNS::Topic",
            "Properties": {
                "TopicName": "Timeout",
                "FifoTopic": true
            }
        },
        "SnsTopicUnknown": {
            "Type": "AWS::SNS::Topic",
            "Properties": {
                "TopicName": "Unknown",
                "FifoTopic": true
            }
        }
    }
}
```

## Replicate an Amazon DynamoDB resource<a name="intrinsic-function-reference-foreach-example-replicate-ddb-resource"></a>

This example snippet creates four [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html) resources with names such as `Points`, `Score`, etc\.

### JSON<a name="intrinsic-function-reference-foreach-example-replicate-ddb-resource.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Transform": "AWS::LanguageExtensions",
    "Resources": {
        "Fn::ForEach::Tables": [
            "TableName",
            ["Points", "Score", "Name", "Leaderboard"],
            {
                "DynamoDB${TableName}": {
                    "Type": "AWS::DynamoDB::Table",
                    "Properties": {
                        "TableName": {
                            "Ref": "TableName"
                        },
                        "AttributeDefinitions": [
                            {
                                "AttributeName": "id",
                                "AttributeType": "S"
                            }
                        ],
                        "KeySchema": [
                            {
                                "AttributeName": "id",
                                "KeyType": "HASH"
                            }
                        ],
                        "ProvisionedThroughput": {
                            "ReadCapacityUnits": "5",
                            "WriteCapacityUnits": "5"
                        }
                    }
                }
            }
        ]
    }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-replicate-ddb-resource.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  'Fn::ForEach::Tables':
    - TableName
    - [Points, Score, Name, Leaderboard]
    - 'DynamoDB${TableName}':
        Type: 'AWS::DynamoDB::Table'
        Properties:
          TableName: !Ref TableName
          AttributeDefinitions:
            - AttributeName: id
              AttributeType: S
          KeySchema:
            - AttributeName: id
              KeyType: HASH
          ProvisionedThroughput:
            ReadCapacityUnits: '5'
            WriteCapacityUnits: '5'
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  DynamoDBPoints:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Points
      AttributeDefinitions:
        - AttributeName: id
          AttributeType: S
      KeySchema:
        - AttributeName: id
          KeyType: HASH
      ProvisionedThroughput:
        ReadCapacityUnits: '5'
        WriteCapacityUnits: '5'
  DynamoDBScore:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Score
      AttributeDefinitions:
        - AttributeName: id
          AttributeType: S
      KeySchema:
        - AttributeName: id
          KeyType: HASH
      ProvisionedThroughput:
        ReadCapacityUnits: '5'
        WriteCapacityUnits: '5'
  DynamoDBName:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Name
      AttributeDefinitions:
        - AttributeName: id
          AttributeType: S
      KeySchema:
        - AttributeName: id
          KeyType: HASH
      ProvisionedThroughput:
        ReadCapacityUnits: '5'
        WriteCapacityUnits: '5'
  DynamoDBLeaderboard:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Leaderboard
      AttributeDefinitions:
        - AttributeName: id
          AttributeType: S
      KeySchema:
        - AttributeName: id
          KeyType: HASH
      ProvisionedThroughput:
        ReadCapacityUnits: '5'
        WriteCapacityUnits: '5'
```

## Replicate multiple resources<a name="intrinsic-function-reference-foreach-example-replicate-multiple-resources"></a>

This example creates multtiple instances of [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-natgateway.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-natgateway.html) and [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-eip.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-eip.html) using a naming convention of "\{ResourceType\}$\{Identifier\}"\. You can declare multiple resource types under one `Fn::ForEach` loop to take advantage of a single identifier\.

**Note**  
The example below assumes the `TwoNatGateways` and `ThreeNatGateways` Conditions exist, and `PublicSubnetA`, `PublicSubnetB`, and `PublicSubnetC` Resources are defined\.

**Note**  
Unique values for each element in the Collection are defined within the Mappings section, where the [`Fn::FindInMap`](intrinsic-function-reference-findinmap.md) intrinsic function is used to reference the corresponding value\. If `Fn::FindInMap` is unable to find the corresponding identifier, the Condition property will not be set resolving to `!Ref ‘AWS:::NoValue`\.

### JSON<a name="intrinsic-function-reference-foreach-example-replicate-multiple-resources.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Transform": "AWS::LanguageExtensions",
  "Mappings": {
    "NatGateway": {
      "Condition": {
        "B": "TwoNatGateways",
        "C": "ThreeNatGateways"
      }
    }
  },
  "Resources": {
    "Fn::ForEach::NatGatewayAndEIP": [
      "Identifier",
      [ "A", "B", "C" ],
      {
        "NatGateway${Identifier}": {
          "Type": "AWS::EC2::NatGateway",
          "Properties": {
            "AllocationId": {
              "Fn::GetAtt": [
                {
                  "Fn::Sub": "NatGatewayAttachment${Identifier}"
                },
                "AllocationId"
              ]
            },
            "SubnetId": {
              "Ref": {
                "Fn::Sub": "PublicSubnet${Identifier}"
              }
            }
          },
          "Condition": {
            "Fn::FindInMap": [
              "NatGateway",
              "Condition",
              {
                "Ref": "Identifier"
              },
              {
                "DefaultValue": {
                  "Ref": "AWS::NoValue"
                }
              }
            ]
          }
        },
        "NatGatewayAttachment${Identifier}": {
          "Type": "AWS::EC2::EIP",
          "Properties": {
            "Domain": "vpc"
          },
          "Condition": {
            "Fn::FindInMap": [
              "NatGateway",
              "Condition",
              {
                "Ref": "Identifier"
              },
              {
                "DefaultValue": {
                  "Ref": "AWS::NoValue"
                }
              }
            ]
          }
        }
      }
    ]
  }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-replicate-multiple-resources.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: AWS::LanguageExtensions
Mappings:
  NatGateway:
    Condition:
      B: TwoNatGateways
      C: ThreeNatGateways
Resources:
  Fn::ForEach::NatGatewayAndEIP:
    - Identifier
    - - A
      - B
      - C
    - NatGateway${Identifier}:
        Type: AWS::EC2::NatGateway
        Properties:
          AllocationId: !GetAtt
            - !Sub NatGatewayAttachment${Identifier}
            - AllocationId
          SubnetId: !Ref
            Fn::Sub: PublicSubnet${Identifier}
        Condition: !FindInMap
          - NatGateway
          - Condition
          - !Ref Identifier
          - DefaultValue: !Ref AWS::NoValue
      NatGatewayAttachment${Identifier}:
        Type: AWS::EC2::EIP
        Properties:
          Domain: vpc
        Condition: !FindInMap
          - NatGateway
          - Condition
          - !Ref Identifier
          - DefaultValue: !Ref AWS::NoValue
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Transform: AWS::LanguageExtensions
Resources:
  NatGatewayA:
    Type: AWS::EC2::NatGateway
    Properties:
      AllocationId: !GetAtt
        - NatGatewayAttachmentA
        - AllocationId
      SubnetId: !Ref PublicSubnetA
  NatGatewayB:
    Type: AWS::EC2::NatGateway
    Properties:
      AllocationId: !GetAtt
        - NatGatewayAttachmentB
        - AllocationId
      SubnetId: !Ref PublicSubnetB
    Condition: TwoNatGateways
  NatGatewayC:
    Type: AWS::EC2::NatGateway
    Properties:
      AllocationId: !GetAtt
        - NatGatewayAttachmentC
        - AllocationId
      SubnetId: !Ref PublicSubnetC
    Condition: ThreeNatGateways
  NatGatewayAttachmentA:
    Type: AWS::EC2::EIP
    Properties:
      Domain: vpc
  NatGatewayAttachmentB:
    Type: AWS::EC2::EIP
    Properties:
      Domain: vpc
    Condition: TwoNatGateways
  NatGatewayAttachmentC:
    Type: AWS::EC2::EIP
    Properties:
      Domain: vpc
    Condition: ThreeNatGateways
```

## Replicate multiple resources using a nested `Fn::ForEach` loops<a name="intrinsic-function-reference-foreach-example-nested-loop-resources"></a>

This example uses nested `Fn::ForEach` loops to map three resources \( [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-natgateway.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-natgateway.html), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html), and [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet-network-acl-assoc.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet-network-acl-assoc.html)\) with each other\.

### JSON<a name="intrinsic-function-reference-foreach-example-nested-loop-resources.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Transform": "AWS::LanguageExtensions",
  "Resources": {
    "VPC": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": "10.0.0.0/16",
        "EnableDnsSupport": "true",
        "EnableDnsHostnames": "true"
      }
    },
    "Fn::ForEach::SubnetResources": [
      "Prefix",
      [
        "Transit",
        "Public"
      ],
      {
        "Nacl${Prefix}Subnet": {
          "Type": "AWS::EC2::NetworkAcl",
          "Properties": {
            "VpcId": {
              "Ref": "VPC"
            }
          }
        },
        "Fn::ForEach::LoopInner": [
          "Suffix",
          [
            "A",
            "B",
            "C"
          ],
          {
            "${Prefix}Subnet${Suffix}": {
              "Type": "AWS::EC2::Subnet",
              "Properties": {
                "VpcId": {
                  "Ref": "VPC"
                }
              }
            },
            "Nacl${Prefix}Subnet${Suffix}Association": {
              "Type": "AWS::EC2::SubnetNetworkAclAssociation",
              "Properties": {
                "SubnetId": {
                  "Ref": {
                    "Fn::Sub": "${Prefix}Subnet${Suffix}"
                  }
                },
                "NetworkAclId": {
                  "Ref": {
                    "Fn::Sub": "Nacl${Prefix}Subnet"
                  }
                }
              }
            }
          }
        ]
      }
    ]
  }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-nested-loop-resources.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: 10.0.0.0/16
      EnableDnsSupport: 'true'
      EnableDnsHostnames: 'true'
  'Fn::ForEach::SubnetResources':
  - Prefix
  - [Transit, Public]
  - 'Nacl${Prefix}Subnet':
      Type: 'AWS::EC2::NetworkAcl'
      Properties:
        VpcId: !Ref 'VPC'
    'Fn::ForEach::LoopInner':
    - Suffix
    - [A, B, C]
    - '${Prefix}Subnet${Suffix}':
        Type: 'AWS::EC2::Subnet'
        Properties:
          VpcId: !Ref 'VPC'
      'Nacl${Prefix}Subnet${Suffix}Association':
        Type: 'AWS::EC2::SubnetNetworkAclAssociation'
        Properties:
          SubnetId: !Ref
            'Fn::Sub': '${Prefix}Subnet${Suffix}'
          NetworkAclId: !Ref
            'Fn::Sub': 'Nacl${Prefix}Subnet'
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: 10.0.0.0/16
      EnableDnsSupport: 'true'
      EnableDnsHostnames: 'true'
  NaclTransitSubnet:
    Type: 'AWS::EC2::NetworkAcl'
    Properties:
      VpcId: !Ref VPC
  TransitSubnetA:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
  NaclTransitSubnetAAssociation:
    Type: 'AWS::EC2::SubnetNetworkAclAssociation'
    Properties:
      SubnetId: !Ref TransitSubnetA
      NetworkAclId: !Ref NaclTransitSubnet
  TransitSubnetB:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
  NaclTransitSubnetBAssociation:
    Type: 'AWS::EC2::SubnetNetworkAclAssociation'
    Properties:
      SubnetId: !Ref TransitSubnetB
      NetworkAclId: !Ref NaclTransitSubnet
  TransitSubnetC:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
  NaclTransitSubnetCAssociation:
    Type: 'AWS::EC2::SubnetNetworkAclAssociation'
    Properties:
      SubnetId: !Ref TransitSubnetC
      NetworkAclId: !Ref NaclTransitSubnet
  NaclPublicSubnet:
    Type: 'AWS::EC2::NetworkAcl'
    Properties:
      VpcId: !Ref VPC
  PublicSubnetA:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
  NaclPublicSubnetAAssociation:
    Type: 'AWS::EC2::SubnetNetworkAclAssociation'
    Properties:
      SubnetId: !Ref PublicSubnetA
      NetworkAclId: !Ref NaclPublicSubnet
  PublicSubnetB:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
  NaclPublicSubnetBAssociation:
    Type: 'AWS::EC2::SubnetNetworkAclAssociation'
    Properties:
      SubnetId: !Ref PublicSubnetB
      NetworkAclId: !Ref NaclPublicSubnet
  PublicSubnetC:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
  NaclPublicSubnetCAssociation:
    Type: 'AWS::EC2::SubnetNetworkAclAssociation'
    Properties:
      SubnetId: !Ref PublicSubnetC
      NetworkAclId: !Ref NaclPublicSubnet
```

## Reference replicated properties for an Amazon EC2 resource<a name="intrinsic-function-reference-foreach-example-reference-replicated-resource"></a>

This example uses the `Fn::ForEach` intrinsic function to reference replicated [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resources\.

### JSON<a name="intrinsic-function-reference-foreach-example-reference-replicated-resource.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Transform": "AWS::LanguageExtensions",
  "Mappings": {
    "Instances": {
      "InstanceType": {
        "B": "m5.4xlarge",
        "C": "c5.2xlarge"
      },
      "ImageId": {"A": "ami-id1"}
    }
  },
  "Resources": {
    "Fn::ForEach::Instances": [
      "Identifier",
      [
        "A",
        "B",
        "C"
      ],
      {
        "Instance${Identifier}": {
          "Type": "AWS::EC2::Instance",
          "Properties": {
            "InstanceType": {
              "Fn::FindInMap": [
                "Instances",
                "InstanceType",
                {"Ref": "Identifier"},
                {"DefaultValue": "m5.xlarge"}
              ]
            },
            "ImageId": {
              "Fn::FindInMap": [
                "Instances",
                "ImageId",
                {"Ref": "Identifier"},
                {"DefaultValue": "ami-id-default"}
              ]
            }
          }
        }
      }
    ]
  },
  "Outputs": {
    "SecondInstanceId": {
      "Description": "Instance Id for InstanceB",
      "Value": {"Ref": "InstanceB"}
    },
    "SecondPrivateIp": {
      "Description": "Private IP for InstanceB",
      "Value": {
        "Fn::GetAtt": [
          "InstanceB",
          "PrivateIp"
        ]
      }
    }
  }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-reference-replicated-resource.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Mappings:
  Instances:
    InstanceType:
      B: m5.4xlarge
      C: c5.2xlarge
    ImageId:
      A: ami-id1
Resources:
  'Fn::ForEach::Instances':
  - Identifier
  - [A, B, C]
  - 'Instance${Identifier}':
      Type: 'AWS::EC2::Instance'
      Properties:
        InstanceType: !FindInMap [Instances, InstanceType, !Ref 'Identifier', {DefaultValue: m5.xlarge}]
        ImageId: !FindInMap [Instances, ImageId, !Ref 'Identifier', {DefaultValue: ami-id-default}]
Outputs:
  SecondInstanceId:
    Description: Instance Id for InstanceB
    Value: !Ref 'InstanceB'
  SecondPrivateIp:
    Description: Private IP for InstanceB
    Value: !GetAtt [InstanceB, PrivateIp]
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  InstanceA:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: m5.xlarge
      ImageId: ami-id1
  InstanceB:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: m5.4xlarge
      ImageId: ami-id-default
  InstanceC:
    Type: 'AWS::EC2::Instance'
    Properties:
      InstanceType: c5.2xlarge
      ImageId: ami-id-default
Outputs:
  SecondInstanceId:
    Description: Instance Id for InstanceB
    Value: !Ref InstanceB
  SecondPrivateIp:
    Description: Private IP for InstanceB
    Value: !GetAtt [InstanceB, PrivateIp]
```

## Replicate properties for an Amazon EC2 resource<a name="intrinsic-function-reference-foreach-example-replicate-resource-properties"></a>

This example uses the `Fn::ForEach` intrinsic function to repeat some properties like `ImageId`, `InstanceType`, and `AvailabilityZone` to an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

### JSON<a name="intrinsic-function-reference-foreach-example-replicate-resource-properties.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Transform": "AWS::LanguageExtensions",
  "Mappings": {
    "InstanceA": {
      "Properties": {
        "ImageId": "ami-id1",
        "InstanceType": "m5.xlarge"
      }
    },
    "InstanceB": {
      "Properties": {
        "ImageId": "ami-id2"
      }
    },
    "InstanceC": {
      "Properties": {
        "ImageId": "ami-id3",
        "InstanceType": "m5.2xlarge",
        "AvailabilityZone": "us-east-1a"
      }
    }
  },
  "Resources": {
    "Fn::ForEach::Instances": [
      "InstanceLogicalId",
      [ "InstanceA", "InstanceB", "InstanceC" ],
      {
        "${InstanceLogicalId}": {
          "Type": "AWS::EC2::Instance",
          "Properties": {
            "DisableApiTermination": true,
            "UserData": {
              "Fn::Base64": {
                "Fn::Join": [
                  "",
                  [
                    "#!/bin/bash\n",
                    "yum update -y\n",
                    "yum install -y httpd.x86_64\n",
                    "systemctl start httpd.service\n",
                    "systemctl enable httpd.service\n",
                    "echo \"Hello World from $(hostname -f)\" > /var/www/html/index.html\n"
                  ]
                ]
              }
            },
            "Fn::ForEach::Properties": [
              "PropertyName",
              [ "ImageId", "InstanceType", "AvailabilityZone" ],
              {
                "${PropertyName}": {
                  "Fn::FindInMap": [
                    { "Ref": "InstanceLogicalId" },
                    "Properties",
                    { "Ref": "PropertyName"},
                    {
                      "DefaultValue": { "Ref": "AWS::NoValue" }
                    }
                  ]
                }
              }
            ]
          }
        }
      }
    ]
  }
}
```

### YAML<a name="intrinsic-function-reference-foreach-example-replicate-resource-properties.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Mappings:
  InstanceA:
    Properties:
      ImageId: ami-id1
      InstanceType: m5.xlarge
  InstanceB:
    Properties:
      ImageId: ami-id2
  InstanceC:
    Properties:
      ImageId: ami-id3
      InstanceType: m5.2xlarge
      AvailabilityZone: us-east-1a
Resources:
  'Fn::ForEach::Instances':
  - InstanceLogicalId
  - [InstanceA, InstanceB, InstanceC]
  - '${InstanceLogicalId}':
      Type: 'AWS::EC2::Instance'
      Properties:
        DisableApiTermination: true
        UserData:
          Fn::Base64: !Sub |
            #!/bin/bash
            yum update -y
            yum install -y httpd.x86_64
            systemctl start httpd.service
            systemctl enable httpd.service
            echo "Hello World from $(hostname -f)" > /var/www/html/index.html
        'Fn::ForEach::Properties':
          - PropertyName
          - [ImageId, InstanceType, AvailabilityZone]
          - '${PropertyName}':
             'Fn::FindInMap':
               - Ref: 'InstanceLogicalId'
               - Properties
               - Ref: 'PropertyName'
               - {DefaultValue: !Ref 'AWS::NoValue'}
```

The transformed template will be equivalent to the following template:

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Resources:
  InstanceA:
    Type: 'AWS::EC2::Instance'
    Properties:
      DisableApiTermination: true
      UserData:
        Fn::Base64: 
          !Sub |
            #!/bin/bash
            yum update -y
            yum install -y httpd.x86_64
            systemctl start httpd.service
            systemctl enable httpd.service
            echo "Hello World from $(hostname -f)" > /var/www/html/index.html
      ImageId: ami-id1
      InstanceType: m5.xlarge
  InstanceB:
    Type: 'AWS::EC2::Instance'
    Properties:
      DisableApiTermination: true
      UserData:
        Fn::Base64: 
          !Sub |
            #!/bin/bash
            yum update -y
            yum install -y httpd.x86_64
            systemctl start httpd.service
            systemctl enable httpd.service
            echo "Hello World from $(hostname -f)" > /var/www/html/index.html
      ImageId: ami-id2
  InstanceC:
    Type: 'AWS::EC2::Instance'
    Properties:
      DisableApiTermination: true
      UserData:
        Fn::Base64: 
          !Sub |
            #!/bin/bash
            yum update -y
            yum install -y httpd.x86_64
            systemctl start httpd.service
            systemctl enable httpd.service
            echo "Hello World from $(hostname -f)" > /var/www/html/index.html
      ImageId: ami-id3
      InstanceType: m5.2xlarge
      AvailabilityZone: us-east-1a
```
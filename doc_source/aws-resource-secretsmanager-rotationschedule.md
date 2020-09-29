# AWS::SecretsManager::RotationSchedule<a name="aws-resource-secretsmanager-rotationschedule"></a>

The `AWS::SecretsManager::RotationSchedule` resource configures rotation for a secret\. You must already configure the secret with the details of the database or service\. If you define both the secret and the database or service in an AWS CloudFormation template, then define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource to populate the secret with the connection details of the database or service before you attempt to configure rotation\.

**Important**  
When you configure rotation for a secret, AWS CloudFormation automatically rotates the secret one time\. Be sure you configure all your clients to retrieve the secret using Secrets Manager before configuring rotation to prevent breaking them\.

## Syntax<a name="aws-resource-secretsmanager-rotationschedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-rotationschedule-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::RotationSchedule",
  "Properties" : {
      "[HostedRotationLambda](#cfn-secretsmanager-rotationschedule-hostedrotationlambda)" : HostedRotationLambda,
      "[RotationLambdaARN](#cfn-secretsmanager-rotationschedule-rotationlambdaarn)" : String,
      "[RotationRules](#cfn-secretsmanager-rotationschedule-rotationrules)" : RotationRules,
      "[SecretId](#cfn-secretsmanager-rotationschedule-secretid)" : String
    }
}
```

### YAML<a name="aws-resource-secretsmanager-rotationschedule-syntax.yaml"></a>

```
Type: AWS::SecretsManager::RotationSchedule
Properties: 
  [HostedRotationLambda](#cfn-secretsmanager-rotationschedule-hostedrotationlambda): 
    HostedRotationLambda
  [RotationLambdaARN](#cfn-secretsmanager-rotationschedule-rotationlambdaarn): String
  [RotationRules](#cfn-secretsmanager-rotationschedule-rotationrules): 
    RotationRules
  [SecretId](#cfn-secretsmanager-rotationschedule-secretid): String
```

## Properties<a name="aws-resource-secretsmanager-rotationschedule-properties"></a>

`HostedRotationLambda`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda"></a>
To use these values, you must specify `Transform: AWS::SecretsManager-2020-07-23` at the beginning of the CloudFormation template\.  
When you enter valid values for `RotationSchedule.HostedRotationLambda`, Secrets Manager launches a Lambda that performs rotation on the secret specified in the `secret-id` property\. The template creates a Lambda as part of a nested stack within the current stack\.   
*Required*: No  
*Type*: [HostedRotationLambda](aws-properties-secretsmanager-rotationschedule-hostedrotationlambda.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationLambdaARN`  <a name="cfn-secretsmanager-rotationschedule-rotationlambdaarn"></a>
Specifies the ARN of the Lambda function that can rotate the secret\. If you don't specify this parameter, then the secret must already have the ARN of a Lambda function configured\. To reference a Lambda function also created in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the function's logical ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationRules`  <a name="cfn-secretsmanager-rotationschedule-rotationrules"></a>
Specifies a structure that defines the rotation schedule for this secret\.  
*Required*: No  
*Type*: [RotationRules](aws-properties-secretsmanager-rotationschedule-rotationrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretId`  <a name="cfn-secretsmanager-rotationschedule-secretid"></a>
Specifies the ARN or the friendly name of the secret that you want to rotate\. To reference a secret also created in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the secret's logical ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-secretsmanager-rotationschedule-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-rotationschedule-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::RotationSchedule` resource to the intrinsic `Ref` function, the function returns the ARN of the secret being configured, such as:

*arn:aws:secretsmanager: us\-west\-2*:*123456789012*:secret:*my\-path/my\-secret\-name*\-*1a2b3c* 

This enables you to reference a secret you create in one part of the stack template from within the definition of another resource later, in the same template\. You typically do this when you define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-secretsmanager-rotationschedule--examples"></a>

The following examples display complete examples of creating a secret, creating an RDS database instance associated with the secret and configuring rotation\. The example shows how to define a Lambda rotation function, attach the required trust and permissions policies, and associate the function with the secret on a defined schedule\.

RDS Secret Rotation

### Configuring RDS DB Secret Rotation<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_RDS_DB_Secret_Rotation"></a>

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_RDS_DB_Secret_Rotation--json"></a>

```
{
        "AWSTemplateFormatVersion": "2010-09-09",
        "Transform": "AWS::SecretsManager-2020-07-23",
        "Description": "This is an example template to demonstrate CloudFormation resources for Secrets Manager",
        "Resources": {
            "TestVPC": {
                "Type": "AWS::EC2::VPC",
                "Properties": {
                    "CidrBlock": "10.0.0.0/16",
                    "EnableDnsHostnames": true,
                    "EnableDnsSupport": true
                }
            },
            "TestSubnet01": {
                "Type": "AWS::EC2::Subnet",
                "Properties": {
                    "CidrBlock": "10.0.96.0/19",
                    "AvailabilityZone": {
                        "Fn::Select": [
                            "0",
                            {
                                "Fn::GetAZs": {
                                    "Ref": "AWS::Region"
                                }
                            }
                        ]
                    },
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "TestSubnet02": {
                "Type": "AWS::EC2::Subnet",
                "Properties": {
                    "CidrBlock": "10.0.128.0/19",
                    "AvailabilityZone": {
                        "Fn::Select": [
                            "1",
                            {
                                "Fn::GetAZs": {
                                    "Ref": "AWS::Region"
                                }
                            }
                        ]
                    },
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "SecretsManagerVPCEndpoint": {
                "Type": "AWS::EC2::VPCEndpoint",
                "Properties": {
                    "SubnetIds": [
                        {
                            "Ref": "TestSubnet01"
                        },
                        {
                            "Ref": "TestSubnet02"
                        }
                    ],
                    "SecurityGroupIds": [
                        {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        }
                    ],
                    "VpcEndpointType": "Interface",
                    "ServiceName": {
                        "Fn::Sub": "com.amazonaws.${AWS::Region}.secretsmanager"
                    },
                    "PrivateDnsEnabled": true,
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "MyRDSInstanceRotationSecret": {
                "Type": "AWS::SecretsManager::Secret",
                "Properties": {
                    "Description": "This is my rds instance secret",
                    "GenerateSecretString": {
                        "SecretStringTemplate": "{\"username\": \"admin\"}",
                        "GenerateStringKey": "password",
                        "PasswordLength": 16,
                        "ExcludeCharacters": "\"@/\\"
                    },
                    "Tags": [
                        {
                            "Key": "AppName",
                            "Value": "MyApp"
                        }
                    ]
                }
            },
            "MyDBInstance": {
                "Type": "AWS::RDS::DBInstance",
                "Properties": {
                    "AllocatedStorage": 20,
                    "DBInstanceClass": "db.t3.micro",
                    "Engine": "mysql",
                    "DBSubnetGroupName": {
                        "Ref": "MyDBSubnetGroup"
                    },
                    "MasterUsername": {
                        "Fn::Sub": "{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::username}}"
                    },
                    "MasterUserPassword": {
                        "Fn::Sub": "{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::password}}"
                    },
                    "BackupRetentionPeriod": 0,
                    "VPCSecurityGroups": [
                        {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        }
                    ]
                }
            },
            "MyDBSubnetGroup": {
                "Type": "AWS::RDS::DBSubnetGroup",
                "Properties": {
                    "DBSubnetGroupDescription": "Test Group",
                    "SubnetIds": [
                        {
                            "Ref": "TestSubnet01"
                        },
                        {
                            "Ref": "TestSubnet02"
                        }
                    ]
                }
            },
            "SecretRDSInstanceAttachment": {
                "Type": "AWS::SecretsManager::SecretTargetAttachment",
                "Properties": {
                    "SecretId": {
                        "Ref": "MyRDSInstanceRotationSecret"
                    },
                    "TargetId": {
                        "Ref": "MyDBInstance"
                    },
                    "TargetType": "AWS::RDS::DBInstance"
                }
            },
            "MySecretRotationSchedule": {
                "Type": "AWS::SecretsManager::RotationSchedule",
                "DependsOn": "SecretRDSInstanceAttachment",
                "Properties": {
                    "SecretId": {
                        "Ref": "MyRDSInstanceRotationSecret"
                    },
                    "HostedRotationLambda": {
                        "RotationType": "MySQLSingleUser",
                        "RotationLambdaName": "SecretsManagerRotation",
                        "VpcSecurityGroupIds": {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        },
                        "VpcSubnetIds": {
                            "Fn::Join": [
                                ",",
                                [
                                    {
                                        "Ref": "TestSubnet01"
                                    },
                                    {
                                        "Ref": "TestSubnet02"
                                    }
                                ]
                            ]
                        }
                    },
                    "RotationRules": {
                        "AutomaticallyAfterDays": 30
                    }
                }
            }
        }
    }
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Configuring_RDS_DB_Secret_Rotation--yaml"></a>

```
 AWSTemplateFormatVersion: 2010-09-09
 Transform: AWS::SecretsManager-2020-07-23
 Description: "This is an example template to demonstrate CloudFormation resources for Secrets Manager"
 Resources:

      #This is the VPC that the rotation Lambda and the RDS instance will be placed in
      TestVPC: 
        Type: AWS::EC2::VPC
        Properties: 
          CidrBlock: 10.0.0.0/16
          EnableDnsHostnames: true
          EnableDnsSupport: true 

      # Subnet that the rotation Lambda and the RDS instance will be placed in 
      TestSubnet01:
        Type: AWS::EC2::Subnet
        Properties:
          CidrBlock: 10.0.96.0/19
          AvailabilityZone:
            Fn::Select:
              - '0'
              - Fn::GetAZs: {Ref: 'AWS::Region'}
          VpcId:
            Ref: TestVPC

      TestSubnet02:
        Type: AWS::EC2::Subnet
        Properties:
          CidrBlock: 10.0.128.0/19
          AvailabilityZone:
            Fn::Select:
              - '1'
              - Fn::GetAZs: {Ref: 'AWS::Region'}
          VpcId:
            Ref: TestVPC

      #VPC endpoint that will enable the rotation Lambda to make api calls to Secrets Manager 
      SecretsManagerVPCEndpoint:
        Type: AWS::EC2::VPCEndpoint
        Properties:
          SubnetIds:
            - Ref: TestSubnet01
            - Ref: TestSubnet02
          SecurityGroupIds:
            - !GetAtt TestVPC.DefaultSecurityGroup
          VpcEndpointType: 'Interface'
          ServiceName: !Sub "com.amazonaws.${AWS::Region}.secretsmanager"
          PrivateDnsEnabled: true
          VpcId:
            Ref: TestVPC

      #This is a Secret resource with a randomly generated password in its SecretString JSON.
      MyRDSInstanceRotationSecret:
        Type: AWS::SecretsManager::Secret
        Properties:
          Description: 'This is my rds instance secret'
          GenerateSecretString:
            SecretStringTemplate: '{"username": "admin"}'
            GenerateStringKey: 'password'
            PasswordLength: 16
            ExcludeCharacters: '"@/\'
          Tags:
            -
              Key: AppName
              Value: MyApp

      #This is an RDS instance resource. Its master username and password use dynamic references to resolve values from 
      #SecretsManager. The dynamic reference guarantees that CloudFormation will not log or persist the resolved value 
      #We sub the Secret resource's logical id in order to construct the dynamic reference, since the Secret's name is being #generated by CloudFormation
      MyDBInstance:
        Type: AWS::RDS::DBInstance
        Properties:
          AllocatedStorage: 20
          DBInstanceClass: db.t3.micro
          Engine: mysql
          DBSubnetGroupName:
            Ref: MyDBSubnetGroup
          MasterUsername: !Sub '{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::username}}'
          MasterUserPassword: !Sub '{{resolve:secretsmanager:${MyRDSInstanceRotationSecret}::password}}'
          BackupRetentionPeriod: 0
          VPCSecurityGroups:
            - !GetAtt TestVPC.DefaultSecurityGroup

      #Database subnet group for the RDS instance 
      MyDBSubnetGroup: 
        Type: AWS::RDS::DBSubnetGroup
        Properties: 
          DBSubnetGroupDescription: "Test Group"
          SubnetIds: 
             - Ref: TestSubnet01
             - Ref: TestSubnet02
    
      #This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about
      #the referenced RDS instance
      SecretRDSInstanceAttachment:
        Type: AWS::SecretsManager::SecretTargetAttachment
        Properties:
          SecretId: !Ref MyRDSRotationSecret
          TargetId: !Ref MyDBInstance
          TargetType: AWS::RDS::DBInstance
     
      #This is a RotationSchedule resource. It configures rotation of password for the referenced secret using a rotation lambda
      #The first rotation happens at resource creation time, with subsequent rotations scheduled according to the rotation rules
      #We explicitly depend on the SecretTargetAttachment resource being created to ensure that the secret contains all the
      #information necessary for rotation to succeed
      MySecretRotationSchedule:
        Type: AWS::SecretsManager::RotationSchedule
        DependsOn: SecretRDSInstanceAttachment 
        Properties:
          SecretId: !Ref MyRDSInstanceRotationSecret
          HostedRotationLambda:
            RotationType: MySQLSingleUser
            RotationLambdaName: SecretsManagerRotation
            VpcSecurityGroupIds: !GetAtt TestVPC.DefaultSecurityGroup
            VpcSubnetIds:
              Fn::Join:
                - ","
                - - Ref: TestSubnet01
                  - Ref: TestSubnet02
          RotationRules:
            AutomaticallyAfterDays: 30
```

### Redshift Cluster Secret Rotation Example<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_Cluster_Secret_Rotation_Example"></a>

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_Cluster_Secret_Rotation_Example--json"></a>

```
{
        "AWSTemplateFormatVersion": "2010-09-09",
        "Transform": "AWS::SecretsManager-2020-07-23",
        "Description": "This is an example template to demonstrate CloudFormation resources for Secrets Manager",
        "Resources": {
            "TestVPC": {
                "Type": "AWS::EC2::VPC",
                "Properties": {
                    "CidrBlock": "10.0.0.0/16",
                    "EnableDnsHostnames": true,
                    "EnableDnsSupport": true
                }
            },
            "TestSubnet01": {
                "Type": "AWS::EC2::Subnet",
                "Properties": {
                    "CidrBlock": "10.0.96.0/19",
                    "AvailabilityZone": {
                        "Fn::Select": [
                            "0",
                            {
                                "Fn::GetAZs": {
                                    "Ref": "AWS::Region"
                                }
                            }
                        ]
                    },
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "TestSubnet02": {
                "Type": "AWS::EC2::Subnet",
                "Properties": {
                    "CidrBlock": "10.0.128.0/19",
                    "AvailabilityZone": {
                        "Fn::Select": [
                            "1",
                            {
                                "Fn::GetAZs": {
                                    "Ref": "AWS::Region"
                                }
                            }
                        ]
                    },
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "SecretsManagerVPCEndpoint": {
                "Type": "AWS::EC2::VPCEndpoint",
                "Properties": {
                    "SubnetIds": [
                        {
                            "Ref": "TestSubnet01"
                        },
                        {
                            "Ref": "TestSubnet02"
                        }
                    ],
                    "SecurityGroupIds": [
                        {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        }
                    ],
                    "VpcEndpointType": "Interface",
                    "ServiceName": {
                        "Fn::Sub": "com.amazonaws.${AWS::Region}.secretsmanager"
                    },
                    "PrivateDnsEnabled": true,
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "MyRedshiftSecret": {
                "Type": "AWS::SecretsManager::Secret",
                "Properties": {
                    "Description": "This is my rds instance secret",
                    "GenerateSecretString": {
                        "SecretStringTemplate": "{\"username\": \"admin\"}",
                        "GenerateStringKey": "password",
                        "PasswordLength": 16,
                        "ExcludeCharacters": "\"@/\\"
                    },
                    "Tags": [
                        {
                            "Key": "AppName",
                            "Value": "MyApp"
                        }
                    ]
                }
            },
            "MyRedshiftCluster": {
                "Type": "AWS::Redshift::Cluster",
                "Properties": {
                    "DBName": "myyamldb",
                    "NodeType": "ds2.xlarge",
                    "ClusterType": "single-node",
                    "ClusterSubnetGroupName": {
                        "Ref": "ResdshiftSubnetGroup"
                    },
                    "MasterUsername": {
                        "Fn::Sub": "{{resolve:secretsmanager:${MyRedshiftSecret}::username}}"
                    },
                    "MasterUserPassword": {
                        "Fn::Sub": "{{resolve:secretsmanager:${MyRedshiftSecret}::password}}"
                    },
                    "PubliclyAccessible": false,
                    "VpcSecurityGroupIds": [
                        {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        }
                    ]
                }
            },
            "ResdshiftSubnetGroup": {
                "Type": "AWS::Redshift::ClusterSubnetGroup",
                "Properties": {
                    "Description": "Test Group",
                    "SubnetIds": [
                        {
                            "Ref": "TestSubnet01"
                        },
                        {
                            "Ref": "TestSubnet02"
                        }
                    ]
                }
            },
            "SecretRedshiftAttachment": {
                "Type": "AWS::SecretsManager::SecretTargetAttachment",
                "Properties": {
                    "SecretId": {
                        "Ref": "MyRedshiftSecret"
                    },
                    "TargetId": {
                        "Ref": "MyRedshiftCluster"
                    },
                    "TargetType": "AWS::Redshift::Cluster"
                }
            },
            "MySecretRotationSchedule": {
                "Type": "AWS::SecretsManager::RotationSchedule",
                "DependsOn": "SecretRedshiftAttachment",
                "Properties": {
                    "SecretId": {
                        "Ref": "MyRedshiftSecret"
                    },
                    "HostedRotationLambda": {
                        "RotationType": "RedshiftSingleUser",
                        "RotationLambdaName": "SecretsManagerRotationRedshift",
                        "VpcSecurityGroupIds": {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        },
                        "VpcSubnetIds": {
                            "Fn::Join": [
                                ",",
                                [
                                    {
                                        "Ref": "TestSubnet01"
                                    },
                                    {
                                        "Ref": "TestSubnet02"
                                    }
                                ]
                            ]
                        }
                    },
                    "RotationRules": {
                        "AutomaticallyAfterDays": 30
                    }
                }
            }
        }
    }
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_Cluster_Secret_Rotation_Example--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: AWS::SecretsManager-2020-07-23
Description: "This is an example template to demonstrate CloudFormation resources for Secrets Manager" 
Resources:

      #This is the VPC that the rotation Lambda and the Redshift cluster will be placed in 
      TestVPC: 
        Type: AWS::EC2::VPC
        Properties: 
          CidrBlock: 10.0.0.0/16
          EnableDnsHostnames: true
          EnableDnsSupport: true 

      # Subnet that the rotation Lambda and the Redshift cluster will be placed in 
      TestSubnet01:
        Type: AWS::EC2::Subnet
        Properties:
          CidrBlock: 10.0.96.0/19
          AvailabilityZone:
            Fn::Select:
              - '0'
              - Fn::GetAZs: {Ref: 'AWS::Region'}
          VpcId:
            Ref: TestVPC

      TestSubnet02:
        Type: AWS::EC2::Subnet
        Properties:
          CidrBlock: 10.0.128.0/19
          AvailabilityZone:
            Fn::Select:
              - '1'
              - Fn::GetAZs: {Ref: 'AWS::Region'}
          VpcId:
            Ref: TestVPC

      #VPC endpoint that will enable the rotation Lambda to make api calls to Secrets Manager 
      SecretsManagerVPCEndpoint:
        Type: AWS::EC2::VPCEndpoint
        Properties:
          SubnetIds:
            - Ref: TestSubnet01
            - Ref: TestSubnet02
          SecurityGroupIds:
            - !GetAtt TestVPC.DefaultSecurityGroup
          VpcEndpointType: 'Interface'
          ServiceName: !Sub "com.amazonaws.${AWS::Region}.secretsmanager"
          PrivateDnsEnabled: true
          VpcId:
            Ref: TestVPC

      #This is a Secret resource with a randomly generated password in its SecretString JSON.
      MyRedshiftSecret:
        Type: AWS::SecretsManager::Secret
        Properties:
          Description: 'This is my rds instance secret'
          GenerateSecretString:
            SecretStringTemplate: '{"username": "admin"}'
            GenerateStringKey: 'password'
            PasswordLength: 16
            ExcludeCharacters: '"@/\'
          Tags:
            -
              Key: AppName
              Value: MyApp
     
      # This is a Redshift cluster resource. The master username and password use dynamic references
      # to resolve values from Secrets Manager. The dynamic reference guarantees that CloudFormation 
      # will not log or persist the resolved value. We use a Ref to the secret resource's logical id
      # to construct the dynamic reference, since the secret name is generated by CloudFormation. 
      MyRedshiftCluster:
        Type: AWS::Redshift::Cluster
        Properties:
          DBName: "myyamldb"
          NodeType: "ds2.xlarge"
          ClusterType: "single-node"
          ClusterSubnetGroupName:
            Ref: ResdshiftSubnetGroup
          MasterUsername: !Sub '{{resolve:secretsmanager:${MyRedshiftSecret}::username}}'
          MasterUserPassword: !Sub '{{resolve:secretsmanager:${MyRedshiftSecret}::password}}'
          PubliclyAccessible: false
          VpcSecurityGroupIds:
            - !GetAtt TestVPC.DefaultSecurityGroup

      #Database subnet group for the Redshift cluster 
      ResdshiftSubnetGroup: 
        Type: AWS::Redshift::ClusterSubnetGroup
        Properties: 
          Description: "Test Group"
          SubnetIds: 
             - Ref: TestSubnet01
             - Ref: TestSubnet02
    
      # This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about 
      # the referenced Redshift cluster
      SecretRedshiftAttachment:
        Type: AWS::SecretsManager::SecretTargetAttachment
        Properties:
          SecretId: !Ref MyRedshiftSecret
          TargetId: !Ref MyRedshiftCluster
          TargetType: AWS::Redshift::Cluster
     
      #This is a RotationSchedule resource. It configures rotation of password for the referenced secret using a rotation lambda
      #The first rotation happens at resource creation time, with subsequent rotations scheduled according to the rotation rules
      #We explicitly depend on the SecretTargetAttachment resource being created to ensure that the secret contains all the
      #information necessary for rotation to succeed
      MySecretRotationSchedule:
        Type: AWS::SecretsManager::RotationSchedule
        DependsOn: SecretRedshiftAttachment
        Properties:
          SecretId: !Ref MyRedshiftSecret
          HostedRotationLambda:
            RotationType: RedshiftSingleUser
            RotationLambdaName: SecretsManagerRotationRedshift
            VpcSecurityGroupIds: !GetAtt TestVPC.DefaultSecurityGroup
            VpcSubnetIds:
              Fn::Join:
                - ","
                - - Ref: TestSubnet01
                  - Ref: TestSubnet02
          RotationRules:
            AutomaticallyAfterDays: 30
```

### DocumentDB Cluster Secret Rotation Example<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_Cluster_Secret_Rotation_Example"></a>

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_Cluster_Secret_Rotation_Example--json"></a>

```
{
        "AWSTemplateFormatVersion": "2010-09-09",
        "Transform": "AWS::SecretsManager-2020-07-23",
        "Description": "This is an example template to demonstrate CloudFormation resources for Secrets Manager",
        "Resources": {
            "TestVPC": {
                "Type": "AWS::EC2::VPC",
                "Properties": {
                    "CidrBlock": "10.0.0.0/16",
                    "EnableDnsHostnames": true,
                    "EnableDnsSupport": true
                }
            },
            "TestSubnet01": {
                "Type": "AWS::EC2::Subnet",
                "Properties": {
                    "CidrBlock": "10.0.96.0/19",
                    "AvailabilityZone": {
                        "Fn::Select": [
                            "0",
                            {
                                "Fn::GetAZs": {
                                    "Ref": "AWS::Region"
                                }
                            }
                        ]
                    },
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "TestSubnet02": {
                "Type": "AWS::EC2::Subnet",
                "Properties": {
                    "CidrBlock": "10.0.128.0/19",
                    "AvailabilityZone": {
                        "Fn::Select": [
                            "1",
                            {
                                "Fn::GetAZs": {
                                    "Ref": "AWS::Region"
                                }
                            }
                        ]
                    },
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "SecretsManagerVPCEndpoint": {
                "Type": "AWS::EC2::VPCEndpoint",
                "Properties": {
                    "SubnetIds": [
                        {
                            "Ref": "TestSubnet01"
                        },
                        {
                            "Ref": "TestSubnet02"
                        }
                    ],
                    "SecurityGroupIds": [
                        {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        }
                    ],
                    "VpcEndpointType": "Interface",
                    "ServiceName": {
                        "Fn::Sub": "com.amazonaws.${AWS::Region}.secretsmanager"
                    },
                    "PrivateDnsEnabled": true,
                    "VpcId": {
                        "Ref": "TestVPC"
                    }
                }
            },
            "MyDocDBClusterRotationSecret": {
                "Type": "AWS::SecretsManager::Secret",
                "Properties": {
                    "Description": "This is my rds instance secret",
                    "GenerateSecretString": {
                        "SecretStringTemplate": "{\"username\": \"someadmin\", \"ssl\": true}",
                        "GenerateStringKey": "password",
                        "PasswordLength": 16,
                        "ExcludeCharacters": "\"@/\\"
                    },
                    "Tags": [
                        {
                            "Key": "AppName",
                            "Value": "MyApp"
                        }
                    ]
                }
            },
            "MyDocDBCluster": {
                "Type": "AWS::DocDB::DBCluster",
                "Properties": {
                    "DBSubnetGroupName": {
                        "Ref": "MyDBSubnetGroup"
                    },
                    "MasterUsername": {
                        "Fn::Sub": "{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::username}}"
                    },
                    "MasterUserPassword": {
                        "Fn::Sub": "{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::password}}"
                    },
                    "VpcSecurityGroupIds": [
                        {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        }
                    ]
                }
            },
            "DocDBInstance": {
                "Type": "AWS::DocDB::DBInstance",
                "Properties": {
                    "DBClusterIdentifier": {
                        "Ref": "MyDocDBCluster"
                    },
                    "DBInstanceClass": "db.r5.large"
                }
            },
            "MyDBSubnetGroup": {
                "Type": "AWS::DocDB::DBSubnetGroup",
                "Properties": {
                    "DBSubnetGroupDescription": "Test Group",
                    "SubnetIds": [
                        {
                            "Ref": "TestSubnet01"
                        },
                        {
                            "Ref": "TestSubnet02"
                        }
                    ]
                }
            },
            "SecretDocDBClusterAttachment": {
                "Type": "AWS::SecretsManager::SecretTargetAttachment",
                "Properties": {
                    "SecretId": {
                        "Ref": "MyDocDBClusterRotationSecret"
                    },
                    "TargetId": {
                        "Ref": "MyDocDBCluster"
                    },
                    "TargetType": "AWS::DocDB::DBCluster"
                }
            },
            "MySecretRotationSchedule": {
                "Type": "AWS::SecretsManager::RotationSchedule",
                "DependsOn": "SecretDocDBClusterAttachment",
                "Properties": {
                    "SecretId": {
                        "Ref": "MyDocDBClusterRotationSecret"
                    },
                    "HostedRotationLambda": {
                        "RotationType": "MongoDBSingleUser",
                        "RotationLambdaName": "MongoDBSingleUser",
                        "VpcSecurityGroupIds": {
                            "Fn::GetAtt": [
                                "TestVPC",
                                "DefaultSecurityGroup"
                            ]
                        },
                        "VpcSubnetIds": {
                            "Fn::Join": [
                                ",",
                                [
                                    {
                                        "Ref": "TestSubnet01"
                                    },
                                    {
                                        "Ref": "TestSubnet02"
                                    }
                                ]
                            ]
                        }
                    },
                    "RotationRules": {
                        "AutomaticallyAfterDays": 30
                    }
                }
            }
        }
    }
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_Cluster_Secret_Rotation_Example--yaml"></a>

```
 
        Transform: AWS::SecretsManager-2020-07-23
        Description: "This is an example template to demonstrate CloudFormation resources for Secrets Manager"
        Resources:
        
        #This is the VPC that the rotation Lambda and the DocDB cluster will be placed in 
        TestVPC: 
        Type: AWS::EC2::VPC
        Properties: 
        CidrBlock: 10.0.0.0/16
        EnableDnsHostnames: true
        EnableDnsSupport: true 
        
        # Subnet that the rotation Lambda and the DocDB cluster will be placed in 
        TestSubnet01:
        Type: AWS::EC2::Subnet
        Properties:
        CidrBlock: 10.0.96.0/19
        AvailabilityZone:
        Fn::Select:
        - '0'
        - Fn::GetAZs: {Ref: 'AWS::Region'}
        VpcId:
        Ref: TestVPC
        
        TestSubnet02:
        Type: AWS::EC2::Subnet
        Properties:
        CidrBlock: 10.0.128.0/19
        AvailabilityZone:
        Fn::Select:
        - '1'
        - Fn::GetAZs: {Ref: 'AWS::Region'}
        VpcId:
        Ref: TestVPC
        
        #VPC endpoint that will enable the rotation Lambda to make api calls to Secrets Manager 
        SecretsManagerVPCEndpoint:
        Type: AWS::EC2::VPCEndpoint
        Properties:
        SubnetIds:
        - Ref: TestSubnet01
        - Ref: TestSubnet02
        SecurityGroupIds:
        - !GetAtt TestVPC.DefaultSecurityGroup
        VpcEndpointType: 'Interface'
        ServiceName: !Sub "com.amazonaws.${AWS::Region}.secretsmanager"
        PrivateDnsEnabled: true
        VpcId:
        Ref: TestVPC
        
        #This is a Secret resource with a randomly generated password in its SecretString JSON.
        MyDocDBClusterRotationSecret:
        Type: AWS::SecretsManager::Secret
        Properties:
        Description: 'This is my rds instance secret'
        GenerateSecretString:
        SecretStringTemplate: '{"username": "someadmin", "ssl": true}'
        GenerateStringKey: 'password'
        PasswordLength: 16
        ExcludeCharacters: '"@/\'
        Tags:
        -
        Key: AppName
        Value: MyApp
        
        #This is an DocDB cluster resource. Its master username and password use dynamic references to resolve values from 
        #SecretsManager. The dynamic reference guarantees that CloudFormation will not log or persist the resolved value
        #We sub the Secret resource's logical id in order to construct the dynamic reference, since the Secret's name is being #generated by CloudFormation
        MyDocDBCluster:
        Type: AWS::DocDB::DBCluster
        Properties:
        DBSubnetGroupName:
        Ref: MyDBSubnetGroup 
        MasterUsername: !Sub '{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::username}}'
        MasterUserPassword: !Sub '{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::password}}'
        VpcSecurityGroupIds:
        - !GetAtt TestVPC.DefaultSecurityGroup
        
        DocDBInstance:
        Type: AWS::DocDB::DBInstance
        Properties:
        DBClusterIdentifier: !Ref MyDocDBCluster
        DBInstanceClass: "db.r5.large" 
        
        #Database subnet group for the DocDB cluster 
        MyDBSubnetGroup: 
        Type: AWS::DocDB::DBSubnetGroup
        Properties: 
        DBSubnetGroupDescription: "Test Group"
        SubnetIds: 
        - Ref: TestSubnet01
        - Ref: TestSubnet02
        
        #This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about
        #the referenced DocDB cluster
        SecretDocDBClusterAttachment:
        Type: AWS::SecretsManager::SecretTargetAttachment
        Properties:
        SecretId: !Ref MyDocDBClusterRotationSecret
        TargetId: !Ref MyDocDBCluster
        TargetType: AWS::DocDB::DBCluster
        
        #This is a RotationSchedule resource. It configures rotation of password for the referenced secret using a rotation lambda
        #The first rotation happens at resource creation time, with subsequent rotations scheduled according to the rotation rules
        #We explicitly depend on the SecretTargetAttachment resource being created to ensure that the secret contains all the
        #information necessary for rotation to succeed
        MySecretRotationSchedule:
        Type: AWS::SecretsManager::RotationSchedule
        DependsOn: SecretDocDBClusterAttachment
        DependsOn: DocDBInstance
        Properties:
        SecretId: !Ref MyDocDBClusterRotationSecret
        HostedRotationLambda:
        RotationType: MongoDBSingleUser
        RotationLambdaName: MongoDBSingleUser
        VpcSecurityGroupIds: !GetAtt TestVPC.DefaultSecurityGroup
        VpcSubnetIds:
        Fn::Join:
        - ","
        - - Ref: TestSubnet01
        - Ref: TestSubnet02
        RotationRules:
        AutomaticallyAfterDays: 30
```

## See also<a name="aws-resource-secretsmanager-rotationschedule--seealso"></a>
+  [RotateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_RotateSecret.html) in the AWS Secrets Manager API Reference
+  [Rotating Your AWS Secrets Manager Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide
+ [AWS::SecretsManager::RotationSchedule HostedRotationLambda](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-rotationschedule-hostedrotationlambda.html)
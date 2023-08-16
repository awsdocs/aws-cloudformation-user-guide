# AWS::SecretsManager::RotationSchedule<a name="aws-resource-secretsmanager-rotationschedule"></a>

Sets the rotation schedule and Lambda rotation function for a secret\. For more information, see [How rotation works](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotate-secrets_how.html)\. 

For Amazon RDS master user credentials, see [AWS::RDS::DBCluster MasterUserSecret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbcluster-masterusersecret.html)\.

For the rotation function, you have two options:
+ You can create a new rotation function based on one of the [ Secrets Manager rotation function templates](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html) by using `HostedRotationLambda`\.
+ You can choose an existing rotation function by using `RotationLambdaARN`\.

For database secrets, if you define both the secret and the database or service in the AWS CloudFormation template, then you need to define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource to populate the secret with the connection details of the database or service before you attempt to configure rotation\.

## Syntax<a name="aws-resource-secretsmanager-rotationschedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-rotationschedule-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::RotationSchedule",
  "Properties" : {
      "[HostedRotationLambda](#cfn-secretsmanager-rotationschedule-hostedrotationlambda)" : HostedRotationLambda,
      "[RotateImmediatelyOnUpdate](#cfn-secretsmanager-rotationschedule-rotateimmediatelyonupdate)" : Boolean,
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
  [RotateImmediatelyOnUpdate](#cfn-secretsmanager-rotationschedule-rotateimmediatelyonupdate): Boolean
  [RotationLambdaARN](#cfn-secretsmanager-rotationschedule-rotationlambdaarn): String
  [RotationRules](#cfn-secretsmanager-rotationschedule-rotationrules): 
    RotationRules
  [SecretId](#cfn-secretsmanager-rotationschedule-secretid): String
```

## Properties<a name="aws-resource-secretsmanager-rotationschedule-properties"></a>

`HostedRotationLambda`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda"></a>
Creates a new Lambda rotation function based on one of the [ Secrets Manager rotation function templates](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html)\. To use a rotation function that already exists, specify `RotationLambdaARN` instead\.  
For Amazon RDS master user credentials, see [AWS::RDS::DBCluster MasterUserSecret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbcluster-masterusersecret.html)\.  
*Required*: No  
*Type*: [HostedRotationLambda](aws-properties-secretsmanager-rotationschedule-hostedrotationlambda.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotateImmediatelyOnUpdate`  <a name="cfn-secretsmanager-rotationschedule-rotateimmediatelyonupdate"></a>
Specifies whether to rotate the secret immediately or wait until the next scheduled rotation window\. The rotation schedule is defined in `RotationRules`\.  
If you don't immediately rotate the secret, Secrets Manager tests the rotation configuration by running the [`testSecret` step](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotate-secrets_how.html) of the Lambda rotation function\. The test creates an `AWSPENDING` version of the secret and then removes it\.  
If you don't specify this value, then by default, Secrets Manager rotates the secret immediately\.  
Rotation is an asynchronous process\. For more information, see [How rotation works](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotate-secrets_how.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationLambdaARN`  <a name="cfn-secretsmanager-rotationschedule-rotationlambdaarn"></a>
The ARN of an existing Lambda rotation function\. To specify a rotation function that is also defined in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function\.  
For Amazon RDS master user credentials, see [AWS::RDS::DBCluster MasterUserSecret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbcluster-masterusersecret.html)\.  
To create a new rotation function based on one of the [ Secrets Manager rotation function templates](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html), specify `HostedRotationLambda` instead\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationRules`  <a name="cfn-secretsmanager-rotationschedule-rotationrules"></a>
A structure that defines the rotation configuration for this secret\.  
*Required*: No  
*Type*: [RotationRules](aws-properties-secretsmanager-rotationschedule-rotationrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretId`  <a name="cfn-secretsmanager-rotationschedule-secretid"></a>
The ARN or name of the secret to rotate\.   
To reference a secret also created in this template, use the [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the secret's logical ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-secretsmanager-rotationschedule-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-rotationschedule-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::RotationSchedule` resource to the intrinsic `Ref` function, the function returns the ARN of the secret being configured, such as:

*arn:aws:secretsmanager: us\-west\-2*:*123456789012*:secret:*my\-path/my\-secret\-name*\-*1a2b3c* 

You can use the ARN to reference a secret you create in one part of the stack template from within the definition of another resource later, in the same template\. You typically do this when you define the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-secretsmanager-rotationschedule--examples"></a>

### Automatic rotation with a cron expression<a name="aws-resource-secretsmanager-rotationschedule--examples--Automatic_rotation_with_a_cron_expression"></a>

The following example rotates a secret every day between 1:00 AM and 3:00 AM UTC\.

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Automatic_rotation_with_a_cron_expression--json"></a>

```
"MySecretRotationSchedule": {
  "Type": "AWS::SecretsManager::RotationSchedule",
  "DependsOn": "MyRotationLambda",
  "Properties": {
    "SecretId": {"Ref": "MySecret"},
    "RotationLambdaARN": {"Fn::GetAtt": "MyRotationLambda.Arn"},
    "RotationRules": {
      "Duration": "2h",
      "ScheduleExpression": "cron(0 1 * * ? *)"
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Automatic_rotation_with_a_cron_expression--yaml"></a>

```
MySecretRotationSchedule:
  Type: AWS::SecretsManager::RotationSchedule
  DependsOn: MyRotationLambda 
  Properties:
    SecretId: !Ref MySecret
    RotationLambdaARN: !GetAtt MyRotationLambda.Arn
    RotationRules:
      Duration: 2h
      ScheduleExpression: 'cron(0 1 * * ? *)'
```

### Automatic rotation with a rate expression<a name="aws-resource-secretsmanager-rotationschedule--examples--Automatic_rotation_with_a_rate_expression"></a>

The following example rotates a secret between midnight and 6:00 AM UTC every 10 days\.

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Automatic_rotation_with_a_rate_expression--json"></a>

```
"MySecretRotationSchedule": {
  "Type": "AWS::SecretsManager::RotationSchedule",
  "DependsOn": "MyRotationLambda",
  "Properties": {
  "SecretId": {"Ref": "MySecret"},
    "RotationLambdaARN": {"Fn::GetAtt": "MyRotationLambda.Arn"},
    "RotationRules": {
      "Duration": "6h",
      "ScheduleExpression": "rate(10 days)"
      }
    }
  }
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Automatic_rotation_with_a_rate_expression--yaml"></a>

```
MySecretRotationSchedule:
  Type: AWS::SecretsManager::RotationSchedule
  DependsOn: MyRotationLambda 
  Properties:
    SecretId: !Ref MySecret
    RotationLambdaARN: !GetAtt MyRotationLambda.Arn
    RotationRules:
      Duration: 6h
      ScheduleExpression: 'rate(10 days)'
```

### Redshift cluster secret rotation example<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_cluster_secret_rotation_example"></a>

The following example creates a Redshift cluster and a secret with credentials\. The secret is configured to rotate on the first Sunday of every month between 4:00 AM and 6:00 AM UTC\.

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_cluster_secret_rotation_example--json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Transform":"AWS::SecretsManager-2020-07-23",
   "Resources":{
      "TestVPC":{
         "Type":"AWS::EC2::VPC",
         "Properties":{
            "CidrBlock":"10.0.0.0/16",
            "EnableDnsHostnames":true,
            "EnableDnsSupport":true
         }
      },
      "TestSubnet01":{
         "Type":"AWS::EC2::Subnet",
         "Properties":{
            "CidrBlock":"10.0.96.0/19",
            "AvailabilityZone":{
               "Fn::Select":[
                  "0",
                  {
                     "Fn::GetAZs":{
                        "Ref":"AWS::Region"
                     }
                  }
               ]
            },
            "VpcId":{
               "Ref":"TestVPC"
            }
         }
      },
      "TestSubnet02":{
         "Type":"AWS::EC2::Subnet",
         "Properties":{
            "CidrBlock":"10.0.128.0/19",
            "AvailabilityZone":{
               "Fn::Select":[
                  "1",
                  {
                     "Fn::GetAZs":{
                        "Ref":"AWS::Region"
                     }
                  }
               ]
            },
            "VpcId":{
               "Ref":"TestVPC"
            }
         }
      },
      "SecretsManagerVPCEndpoint":{
         "Type":"AWS::EC2::VPCEndpoint",
         "Properties":{
            "SubnetIds":[
               {
                  "Ref":"TestSubnet01"
               },
               {
                  "Ref":"TestSubnet02"
               }
            ],
            "SecurityGroupIds":[
               {
                  "Fn::GetAtt":[
                     "TestVPC",
                     "DefaultSecurityGroup"
                  ]
               }
            ],
            "VpcEndpointType":"Interface",
            "ServiceName":{
               "Fn::Sub":"com.amazonaws.${AWS::Region}.secretsmanager"
            },
            "PrivateDnsEnabled":true,
            "VpcId":{
               "Ref":"TestVPC"
            }
         }
      },
      "MyRedshiftSecret":{
         "Type":"AWS::SecretsManager::Secret",
         "Properties":{
            "Description":"This is my secret",
            "GenerateSecretString":{
               "SecretStringTemplate":"{\"username\": \"admin\"}",
               "GenerateStringKey":"password",
               "PasswordLength":16,
               "ExcludeCharacters":"\"@/\\"
            },
            "Tags":[
               {
                  "Key":"AppName",
                  "Value":"MyApp"
               }
            ]
         }
      },
      "MyRedshiftCluster":{
         "Type":"AWS::Redshift::Cluster",
         "Properties":{
            "DBName":"myyamldb",
            "NodeType":"ds2.xlarge",
            "ClusterType":"single-node",
            "ClusterSubnetGroupName":{
               "Ref":"ResdshiftSubnetGroup"
            },
            "MasterUsername":{
               "Fn::Sub":"{{resolve:secretsmanager:${MyRedshiftSecret}::username}}"
            },
            "MasterUserPassword":{
               "Fn::Sub":"{{resolve:secretsmanager:${MyRedshiftSecret}::password}}"
            },
            "PubliclyAccessible":false,
            "VpcSecurityGroupIds":[
               {
                  "Fn::GetAtt":[
                     "TestVPC",
                     "DefaultSecurityGroup"
                  ]
               }
            ]
         }
      },
      "ResdshiftSubnetGroup":{
         "Type":"AWS::Redshift::ClusterSubnetGroup",
         "Properties":{
            "Description":"Test Group",
            "SubnetIds":[
               {
                  "Ref":"TestSubnet01"
               },
               {
                  "Ref":"TestSubnet02"
               }
            ]
         }
      },
      "SecretRedshiftAttachment":{
         "Type":"AWS::SecretsManager::SecretTargetAttachment",
         "Properties":{
            "SecretId":{
               "Ref":"MyRedshiftSecret"
            },
            "TargetId":{
               "Ref":"MyRedshiftCluster"
            },
            "TargetType":"AWS::Redshift::Cluster"
         }
      },
      "MySecretRotationSchedule":{
         "Type":"AWS::SecretsManager::RotationSchedule",
         "DependsOn":"SecretRedshiftAttachment",
         "Properties":{
            "SecretId":{
               "Ref":"MyRedshiftSecret"
            },
            "HostedRotationLambda":{
               "RotationType":"RedshiftSingleUser",
               "RotationLambdaName":"SecretsManagerRotationRedshift",
               "VpcSecurityGroupIds":{
                  "Fn::GetAtt":[
                     "TestVPC",
                     "DefaultSecurityGroup"
                  ]
               },
               "VpcSubnetIds":{
                  "Fn::Join":[
                     ",",
                     [
                        {
                           "Ref":"TestSubnet01"
                        },
                        {
                           "Ref":"TestSubnet02"
                        }
                     ]
                  ]
               }
            },
            "RotationRules":{
               "Duration": "2h",
               "ScheduleExpression": "cron(0 4 ? * SUN#1 *)"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--Redshift_cluster_secret_rotation_example--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Transform: AWS::SecretsManager-2020-07-23
Resources:
  TestVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/16
      EnableDnsHostnames: true
      EnableDnsSupport: true
  TestSubnet01:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 10.0.96.0/19
      AvailabilityZone:
        Fn::Select:
        - '0'
        - Fn::GetAZs:
            Ref: AWS::Region
      VpcId:
        Ref: TestVPC
  TestSubnet02:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 10.0.128.0/19
      AvailabilityZone:
        Fn::Select:
        - '1'
        - Fn::GetAZs:
            Ref: AWS::Region
      VpcId:
        Ref: TestVPC
  SecretsManagerVPCEndpoint:
    Type: AWS::EC2::VPCEndpoint
    Properties:
      SubnetIds:
      - Ref: TestSubnet01
      - Ref: TestSubnet02
      SecurityGroupIds:
      - Fn::GetAtt:
        - TestVPC
        - DefaultSecurityGroup
      VpcEndpointType: Interface
      ServiceName:
        Fn::Sub: com.amazonaws.${AWS::Region}.secretsmanager
      PrivateDnsEnabled: true
      VpcId:
        Ref: TestVPC
  MyRedshiftSecret:
    Type: AWS::SecretsManager::Secret
    Properties:
      Description: This is my secret
      GenerateSecretString:
        SecretStringTemplate: '{"username": "admin"}'
        GenerateStringKey: password
        PasswordLength: 16
        ExcludeCharacters: "\"@/\\"
      Tags:
      - Key: AppName
        Value: MyApp
  MyRedshiftCluster:
    Type: AWS::Redshift::Cluster
    Properties:
      DBName: myyamldb
      NodeType: ds2.xlarge
      ClusterType: single-node
      ClusterSubnetGroupName:
        Ref: ResdshiftSubnetGroup
      MasterUsername:
        Fn::Sub: "{{resolve:secretsmanager:${MyRedshiftSecret}::username}}"
      MasterUserPassword:
        Fn::Sub: "{{resolve:secretsmanager:${MyRedshiftSecret}::password}}"
      PubliclyAccessible: false
      VpcSecurityGroupIds:
      - Fn::GetAtt:
        - TestVPC
        - DefaultSecurityGroup
  ResdshiftSubnetGroup:
    Type: AWS::Redshift::ClusterSubnetGroup
    Properties:
      Description: Test Group
      SubnetIds:
      - Ref: TestSubnet01
      - Ref: TestSubnet02
  SecretRedshiftAttachment:
    Type: AWS::SecretsManager::SecretTargetAttachment
    Properties:
      SecretId:
        Ref: MyRedshiftSecret
      TargetId:
        Ref: MyRedshiftCluster
      TargetType: AWS::Redshift::Cluster
  MySecretRotationSchedule:
    Type: AWS::SecretsManager::RotationSchedule
    DependsOn: SecretRedshiftAttachment
    Properties:
      SecretId:
        Ref: MyRedshiftSecret
      HostedRotationLambda:
        RotationType: RedshiftSingleUser
        RotationLambdaName: SecretsManagerRotationRedshift
        VpcSecurityGroupIds:
          Fn::GetAtt:
          - TestVPC
          - DefaultSecurityGroup
        VpcSubnetIds:
          Fn::Join:
          - ","
          - - Ref: TestSubnet01
            - Ref: TestSubnet02
      RotationRules:
        Duration: 2h
        ScheduleExpression: 'cron(0 4 ? * SUN#1 *)'
```

### DocumentDB secret rotation example<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_secret_rotation_example"></a>

The following example creates a DocumentDB database instance and a secret with credentials\. The secret is configured to rotate on the first Sunday of every month between 4:00 AM and 6:00 AM UTC\.

#### JSON<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_secret_rotation_example--json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Transform":"AWS::SecretsManager-2020-07-23",
   "Resources":{
      "TestVPC":{
         "Type":"AWS::EC2::VPC",
         "Properties":{
            "CidrBlock":"10.0.0.0/16",
            "EnableDnsHostnames":true,
            "EnableDnsSupport":true
         }
      },
      "TestSubnet01":{
         "Type":"AWS::EC2::Subnet",
         "Properties":{
            "CidrBlock":"10.0.96.0/19",
            "AvailabilityZone":{
               "Fn::Select":[
                  "0",
                  {
                     "Fn::GetAZs":{
                        "Ref":"AWS::Region"
                     }
                  }
               ]
            },
            "VpcId":{
               "Ref":"TestVPC"
            }
         }
      },
      "TestSubnet02":{
         "Type":"AWS::EC2::Subnet",
         "Properties":{
            "CidrBlock":"10.0.128.0/19",
            "AvailabilityZone":{
               "Fn::Select":[
                  "1",
                  {
                     "Fn::GetAZs":{
                        "Ref":"AWS::Region"
                     }
                  }
               ]
            },
            "VpcId":{
               "Ref":"TestVPC"
            }
         }
      },
      "SecretsManagerVPCEndpoint":{
         "Type":"AWS::EC2::VPCEndpoint",
         "Properties":{
            "SubnetIds":[
               {
                  "Ref":"TestSubnet01"
               },
               {
                  "Ref":"TestSubnet02"
               }
            ],
            "SecurityGroupIds":[
               {
                  "Fn::GetAtt":[
                     "TestVPC",
                     "DefaultSecurityGroup"
                  ]
               }
            ],
            "VpcEndpointType":"Interface",
            "ServiceName":{
               "Fn::Sub":"com.amazonaws.${AWS::Region}.secretsmanager"
            },
            "PrivateDnsEnabled":true,
            "VpcId":{
               "Ref":"TestVPC"
            }
         }
      },
      "MyDocDBClusterRotationSecret":{
         "Type":"AWS::SecretsManager::Secret",
         "Properties":{
            "GenerateSecretString":{
        "SecretStringTemplate":"{\"username\": \"someadmin\",\"ssl\": true}",
               "GenerateStringKey":"password",
               "PasswordLength":16,
               "ExcludeCharacters":"\"@/\\"
            },
            "Tags":[
               {
                  "Key":"AppName",
                  "Value":"MyApp"
               }
            ]
         }
      },
      "MyDocDBCluster":{
         "Type":"AWS::DocDB::DBCluster",
         "Properties":{
            "DBSubnetGroupName":{
               "Ref":"MyDBSubnetGroup"
            },
            "MasterUsername":{
               "Fn::Sub":"{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::username}}"
            },
        "MasterUserPassword":{
               "Fn::Sub":"{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::password}}"
            },
            "VpcSecurityGroupIds":[
               {
                  "Fn::GetAtt":[
                     "TestVPC",
                     "DefaultSecurityGroup"
                  ]
               }
            ]
         }
      },
      "DocDBInstance":{
         "Type":"AWS::DocDB::DBInstance",
         "Properties":{
            "DBClusterIdentifier":{
               "Ref":"MyDocDBCluster"
            },
            "DBInstanceClass":"db.r5.large"
         }
      },
      "MyDBSubnetGroup":{
         "Type":"AWS::DocDB::DBSubnetGroup",
         "Properties":{
            "DBSubnetGroupDescription":"",
            "SubnetIds":[
               {
                  "Ref":"TestSubnet01"
               },
               {
                  "Ref":"TestSubnet02"
               }
            ]
         }
      },
      "SecretDocDBClusterAttachment":{
         "Type":"AWS::SecretsManager::SecretTargetAttachment",
         "Properties":{
            "SecretId":{
               "Ref":"MyDocDBClusterRotationSecret"
            },
            "TargetId":{
               "Ref":"MyDocDBCluster"
            },
            "TargetType":"AWS::DocDB::DBCluster"
         }
      },
      "MySecretRotationSchedule":{
         "Type":"AWS::SecretsManager::RotationSchedule",
         "DependsOn":"SecretDocDBClusterAttachment",
         "Properties":{
            "SecretId":{
               "Ref":"MyDocDBClusterRotationSecret"
            },
            "HostedRotationLambda":{
               "RotationType":"MongoDBSingleUser",
               "RotationLambdaName":"MongoDBSingleUser",
               "VpcSecurityGroupIds":{
                  "Fn::GetAtt":[
                     "TestVPC",
                     "DefaultSecurityGroup"
                  ]
               },
               "VpcSubnetIds":{
                  "Fn::Join":[
                     ",",
                     [
                        {
                           "Ref":"TestSubnet01"
                        },
                        {
                           "Ref":"TestSubnet02"
                        }
                     ]
                  ]
               }
            },
            "RotationRules":{
              "Duration": "2h",
              "ScheduleExpression": "cron(0 4 ? * SUN#1 *)"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-secretsmanager-rotationschedule--examples--DocumentDB_secret_rotation_example--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Transform: AWS::SecretsManager-2020-07-23
Resources:
  TestVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/16
      EnableDnsHostnames: true
      EnableDnsSupport: true
  TestSubnet01:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 10.0.96.0/19
      AvailabilityZone:
        Fn::Select:
        - '0'
        - Fn::GetAZs:
            Ref: AWS::Region
      VpcId:
        Ref: TestVPC
  TestSubnet02:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 10.0.128.0/19
      AvailabilityZone:
        Fn::Select:
        - '1'
        - Fn::GetAZs:
            Ref: AWS::Region
      VpcId:
        Ref: TestVPC
  SecretsManagerVPCEndpoint:
    Type: AWS::EC2::VPCEndpoint
    Properties:
      SubnetIds:
      - Ref: TestSubnet01
      - Ref: TestSubnet02
      SecurityGroupIds:
      - Fn::GetAtt:
        - TestVPC
        - DefaultSecurityGroup
      VpcEndpointType: Interface
      ServiceName:
        Fn::Sub: com.amazonaws.${AWS::Region}.secretsmanager
      PrivateDnsEnabled: true
      VpcId:
        Ref: TestVPC
  MyDocDBClusterRotationSecret:
    Type: AWS::SecretsManager::Secret
    Properties:
      GenerateSecretString:
        SecretStringTemplate: '{\"username\": \"someadmin\",\"ssl\": true}'
        GenerateStringKey: password
        PasswordLength: 16
        ExcludeCharacters: "\"@/\\"
      Tags:
      - Key: AppName
        Value: MyApp
  MyDocDBCluster:
    Type: AWS::DocDB::DBCluster
    Properties:
      DBSubnetGroupName:
        Ref: MyDBSubnetGroup
      MasterUsername:
        Fn::Sub: "{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::username}}"
      MasterUserPassword:
        Fn::Sub: "{{resolve:secretsmanager:${MyDocDBClusterRotationSecret}::password}}"
      VpcSecurityGroupIds:
      - Fn::GetAtt:
        - TestVPC
        - DefaultSecurityGroup
  DocDBInstance:
    Type: AWS::DocDB::DBInstance
    Properties:
      DBClusterIdentifier:
        Ref: MyDocDBCluster
      DBInstanceClass: db.r5.large
  MyDBSubnetGroup:
    Type: AWS::DocDB::DBSubnetGroup
    Properties:
      DBSubnetGroupDescription: ''
      SubnetIds:
      - Ref: TestSubnet01
      - Ref: TestSubnet02
  SecretDocDBClusterAttachment:
    Type: AWS::SecretsManager::SecretTargetAttachment
    Properties:
      SecretId:
        Ref: MyDocDBClusterRotationSecret
      TargetId:
        Ref: MyDocDBCluster
      TargetType: AWS::DocDB::DBCluster
  MySecretRotationSchedule:
    Type: AWS::SecretsManager::RotationSchedule
    DependsOn: SecretDocDBClusterAttachment
    Properties:
      SecretId:
        Ref: MyDocDBClusterRotationSecret
      HostedRotationLambda:
        RotationType: MongoDBSingleUser
        RotationLambdaName: MongoDBSingleUser
        VpcSecurityGroupIds:
          Fn::GetAtt:
          - TestVPC
          - DefaultSecurityGroup
        VpcSubnetIds:
          Fn::Join:
          - ","
          - - Ref: TestSubnet01
            - Ref: TestSubnet02
      RotationRules:
        Duration: 2h
        ScheduleExpression: 'cron(0 4 ? * SUN#1 *)'
```

## See also<a name="aws-resource-secretsmanager-rotationschedule--seealso"></a>
+  [RotateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_RotateSecret.html) in the AWS Secrets Manager API Reference
+  [Rotate secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User Guide
+ [AWS::SecretsManager::RotationSchedule HostedRotationLambda](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-rotationschedule-hostedrotationlambda.html)
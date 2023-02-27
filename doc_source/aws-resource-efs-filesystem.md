# AWS::EFS::FileSystem<a name="aws-resource-efs-filesystem"></a>

The `AWS::EFS::FileSystem` resource creates a new, empty file system in Amazon Elastic File System \(Amazon EFS\)\. You must create a mount target \([AWS::EFS::MountTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-mounttarget.html)\) to mount your EFS file system on an Amazon EC2 or other AWS cloud compute resource\. 

## Syntax<a name="aws-resource-efs-filesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-efs-filesystem-syntax.json"></a>

```
{
  "Type" : "AWS::EFS::FileSystem",
  "Properties" : {
      "[AvailabilityZoneName](#cfn-efs-filesystem-availabilityzonename)" : String,
      "[BackupPolicy](#cfn-efs-filesystem-backuppolicy)" : BackupPolicy,
      "[BypassPolicyLockoutSafetyCheck](#cfn-efs-filesystem-bypasspolicylockoutsafetycheck)" : Boolean,
      "[Encrypted](#cfn-efs-filesystem-encrypted)" : Boolean,
      "[FileSystemPolicy](#cfn-efs-filesystem-filesystempolicy)" : Json,
      "[FileSystemTags](#cfn-efs-filesystem-filesystemtags)" : [ ElasticFileSystemTag, ... ],
      "[KmsKeyId](#cfn-efs-filesystem-kmskeyid)" : String,
      "[LifecyclePolicies](#cfn-efs-filesystem-lifecyclepolicies)" : [ LifecyclePolicy, ... ],
      "[PerformanceMode](#cfn-efs-filesystem-performancemode)" : String,
      "[ProvisionedThroughputInMibps](#cfn-efs-filesystem-provisionedthroughputinmibps)" : Double,
      "[ThroughputMode](#cfn-efs-filesystem-throughputmode)" : String
    }
}
```

### YAML<a name="aws-resource-efs-filesystem-syntax.yaml"></a>

```
Type: AWS::EFS::FileSystem
Properties: 
  [AvailabilityZoneName](#cfn-efs-filesystem-availabilityzonename): String
  [BackupPolicy](#cfn-efs-filesystem-backuppolicy): 
    BackupPolicy
  [BypassPolicyLockoutSafetyCheck](#cfn-efs-filesystem-bypasspolicylockoutsafetycheck): Boolean
  [Encrypted](#cfn-efs-filesystem-encrypted): Boolean
  [FileSystemPolicy](#cfn-efs-filesystem-filesystempolicy): Json
  [FileSystemTags](#cfn-efs-filesystem-filesystemtags): 
    - ElasticFileSystemTag
  [KmsKeyId](#cfn-efs-filesystem-kmskeyid): String
  [LifecyclePolicies](#cfn-efs-filesystem-lifecyclepolicies): 
    - LifecyclePolicy
  [PerformanceMode](#cfn-efs-filesystem-performancemode): String
  [ProvisionedThroughputInMibps](#cfn-efs-filesystem-provisionedthroughputinmibps): Double
  [ThroughputMode](#cfn-efs-filesystem-throughputmode): String
```

## Properties<a name="aws-resource-efs-filesystem-properties"></a>

`AvailabilityZoneName`  <a name="cfn-efs-filesystem-availabilityzonename"></a>
Used to create a file system that uses One Zone storage classes\. It specifies the AWS Availability Zone in which to create the file system\. Use the format `us-east-1a` to specify the Availability Zone\. For more information about One Zone storage classes, see [Using EFS storage classes](https://docs.aws.amazon.com/efs/latest/ug/storage-classes.html) in the *Amazon EFS User Guide*\.  
One Zone storage classes are not available in all Availability Zones in AWS Regions where Amazon EFS is available\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupPolicy`  <a name="cfn-efs-filesystem-backuppolicy"></a>
Use the `BackupPolicy` to turn automatic backups on or off for the file system\.  
*Required*: No  
*Type*: [BackupPolicy](aws-properties-efs-filesystem-backuppolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BypassPolicyLockoutSafetyCheck`  <a name="cfn-efs-filesystem-bypasspolicylockoutsafetycheck"></a>
\(Optional\) A boolean that specifies whether or not to bypass the `FileSystemPolicy` lockout safety check\. The lockout safety check determines whether the policy in the request will lock out, or prevent, the IAM principal that is making the request from making future `PutFileSystemPolicy` requests on this file system\. Set `BypassPolicyLockoutSafetyCheck` to `True` only when you intend to prevent the IAM principal that is making the request from making subsequent `PutFileSystemPolicy` requests on this file system\. The default value is `False`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-efs-filesystem-encrypted"></a>
A Boolean value that, if true, creates an encrypted file system\. When creating an encrypted file system, you have the option of specifying a KmsKeyId for an existing AWS KMS key\. If you don't specify a KMS key, then the default KMS key for Amazon EFS, `/aws/elasticfilesystem`, is used to protect the encrypted file system\.   
*Required*: Conditional  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemPolicy`  <a name="cfn-efs-filesystem-filesystempolicy"></a>
The `FileSystemPolicy` for the EFS file system\. A file system policy is an IAM resource policy used to control NFS access to an EFS file system\. For more information, see [Using IAM to control NFS access to Amazon EFS](https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html) in the *Amazon EFS User Guide*\.  
*Required*: No  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `20000`  
*Pattern*: `[\s\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileSystemTags`  <a name="cfn-efs-filesystem-filesystemtags"></a>
Use to create one or more tags associated with the file system\. Each tag is a user\-defined key\-value pair\. Name your file system on creation by including a `"Key":"Name","Value":"{value}"` key\-value pair\. Each key must be unique\. For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) in the * AWS General Reference Guide*\.  
*Required*: No  
*Type*: List of [ElasticFileSystemTag](aws-properties-efs-filesystem-elasticfilesystemtag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-efs-filesystem-kmskeyid"></a>
The ID of the AWS KMS key to be used to protect the encrypted file system\. This parameter is only required if you want to use a nondefault KMS key\. If this parameter is not specified, the default KMS key for Amazon EFS is used\. This ID can be in one of the following formats:  
+ Key ID \- A unique identifier of the key, for example `1234abcd-12ab-34cd-56ef-1234567890ab`\.
+ ARN \- An Amazon Resource Name \(ARN\) for the key, for example `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab`\.
+ Key alias \- A previously created display name for a key, for example `alias/projectKey1`\.
+ Key alias ARN \- An ARN for a key alias, for example `arn:aws:kms:us-west-2:444455556666:alias/projectKey1`\.
If `KmsKeyId` is specified, the `Encrypted` parameter must be set to true\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^([0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}|mrk-[0-9a-f]{32}|alias/[a-zA-Z0-9/_-]+|(arn:aws[-a-z]*:kms:[a-z0-9-]+:\d{12}:((key/[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12})|(key/mrk-[0-9a-f]{32})|(alias/[a-zA-Z0-9/_-]+))))$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LifecyclePolicies`  <a name="cfn-efs-filesystem-lifecyclepolicies"></a>
An array of `LifecyclePolicy` objects that define the file system's `LifecycleConfiguration` object\. A `LifecycleConfiguration` object informs EFS lifecycle management and intelligent tiering of the following:  
+ When to move files in the file system from primary storage to the IA storage class\.
+ When to move files that are in IA storage to primary storage\.
Amazon EFS requires that each `LifecyclePolicy` object have only a single transition\. This means that in a request body, `LifecyclePolicies` needs to be structured as an array of `LifecyclePolicy` objects, one object for each transition, `TransitionToIA`, `TransitionToPrimaryStorageClass`\. See the example requests in the following section for more information\.
*Required*: No  
*Type*: List of [LifecyclePolicy](aws-properties-efs-filesystem-lifecyclepolicy.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceMode`  <a name="cfn-efs-filesystem-performancemode"></a>
The performance mode of the file system\. We recommend `generalPurpose` performance mode for most file systems\. File systems using the `maxIO` performance mode can scale to higher levels of aggregate throughput and operations per second with a tradeoff of slightly higher latencies for most file operations\. The performance mode can't be changed after the file system has been created\.  
The `maxIO` mode is not supported on file systems using One Zone storage classes\.
*Required*: No  
*Type*: String  
*Allowed values*: `generalPurpose | maxIO`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisionedThroughputInMibps`  <a name="cfn-efs-filesystem-provisionedthroughputinmibps"></a>
The throughput, measured in MiB/s, that you want to provision for a file system that you're creating\. Valid values are 1\-1024\. Required if `ThroughputMode` is set to `provisioned`\. The upper limit for throughput is 1024 MiB/s\. To increase this limit, contact AWS Support\. For more information, see [Amazon EFS quotas that you can increase](https://docs.aws.amazon.com/efs/latest/ug/limits.html#soft-limits) in the *Amazon EFS User Guide*\.  
*Required*: Conditional  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThroughputMode`  <a name="cfn-efs-filesystem-throughputmode"></a>
Specifies the throughput mode for the file system\. The mode can be `bursting`, `provisioned`, or `elastic`\. If you set `ThroughputMode` to `provisioned`, you must also set a value for `ProvisionedThroughputInMibps`\. After you create the file system, you can decrease your file system's throughput in Provisioned Throughput mode or change between the throughput modes, with certain time restrictions\. For more information, see [Specifying throughput with provisioned mode](https://docs.aws.amazon.com/efs/latest/ug/performance.html#provisioned-throughput) in the *Amazon EFS User Guide*\.   
Default is `bursting`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `bursting | elastic | provisioned`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-efs-filesystem-return-values"></a>

### Ref<a name="aws-resource-efs-filesystem-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the FileSystem ID\. For example: 

 `{"Ref":"logical_file_system_id"}`

returns `fs-0123456789abcdef2`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-efs-filesystem-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-efs-filesystem-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the EFS file system\.  
Example: `arn:aws:elasticfilesystem:us-west-2:1111333322228888:file-system/fs-0123456789abcdef8`

`FileSystemId`  <a name="FileSystemId-fn::getatt"></a>
The ID of the EFS file system\. For example: `fs-abcdef0123456789a`

## Examples<a name="aws-resource-efs-filesystem--examples"></a>



### Create an encrypted EFS file system using EFS Standard storage classes<a name="aws-resource-efs-filesystem--examples--Create_an_encrypted_EFS_file_system_using_EFS_Standard_storage_classes"></a>

The following example declares an Amazon EFS file system with the following attributes:
+ Uses EFS Standard storage classes\.
+ maxIO performance mode\.
+ Lifecycle management and Intelligent Tiering enabled\.
+ Encrypted at rest\.
+ Automatic daily backups are enabled\.
+ File system policy granting read\-only access to the EfsReadOnly IAM role\.
+ File system access:
  + Mount targets in three Availability Zones\.
  + An access point providing an application\-specific entry point to the file system\.

#### JSON<a name="aws-resource-efs-filesystem--examples--Create_an_encrypted_EFS_file_system_using_EFS_Standard_storage_classes--json"></a>

```
"{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "MountTargetVPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": "172.31.0.0/16"
            }
        },
        "MountTargetSubnetOne": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "CidrBlock": "172.31.1.0/24",
                "VpcId": {
                    "Ref": "MountTargetVPC"
                },
                "AvailabilityZone": "us-east-1a"
            }
        },
        "MountTargetSubnetTwo": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "CidrBlock": "172.31.2.0/24",
                "VpcId": {
                    "Ref": "MountTargetVPC"
                },
                "AvailabilityZone": "us-east-1b"
            }
        },
        "MountTargetSubnetThree": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "CidrBlock": "172.31.3.0/24",
                "VpcId": {
                    "Ref": "MountTargetVPC"
                },
                "AvailabilityZone": "us-east-1c
            }
        },
       "FileSystemResource": {
            "Type": "AWS::EFS::FileSystem",
            "Properties": {
                "PerformanceMode": "maxIO",
                "LifecyclePolicies":[
                    {
                        "TransitionToIA" : "AFTER_30_DAYS"
                    },
                    {
                        "TransitionToPrimaryStorageClass" : "AFTER_1_ACCESS"
                    }
                ],    
                "Encrypted": true,
                "FileSystemTags": [
                    {
                        "Key": "Name",
                        "Value": "TestFileSystem"
                    }
                ],
                "FileSystemPolicy": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Action": [
                                "elasticfilesystem:ClientMount"
                            ],
                            "Principal":  {"AWS": "arn:aws:iam::111122223333:role/EfsReadOnly"}
                        }
                    ]
                },
                "BackupPolicy": {
                    "Status": "ENABLED"
                    },
                "KmsKeyId": {
                    "Fn::GetAtt": [
                        "key",
                        "Arn"
                    ]
                }
            } 
        },
        "key": {
            "Type": "AWS::KMS::Key",
            "Properties": {
                "KeyPolicy": {
                    "Version": "2012-10-17",
                    "Id": "key-default-1",
                    "Statement": [
                        {
                            "Sid": "Allow administration of the key",
                            "Effect": "Allow",
                            "Principal": {
                                "AWS": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "arn:aws:iam::",
                                            {
                                                "Ref": "AWS::AccountId"
                                            },
                                            ":root"
                                        ]
                                    ]
                                }
                            },
                            "Action": [
                                "kms:*"
                            ],
                            "Resource": "*"
                        }
                    ]
                }
            }
        },
        "MountTargetResource1": {
            "Type": "AWS::EFS::MountTarget",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FileSystemResource"
                },
                "SubnetId": {
                    "Ref": "MountTargetSubnetOne"
                },
                "SecurityGroups": [
                    {
                        "Fn::GetAtt": [
                            "MountTargetVPC",
                            "DefaultSecurityGroup"
                        ]
                    }
                ]
            }
        },
        "MountTargetResource2": {
            "Type": "AWS::EFS::MountTarget",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FileSystemResource"
                },
                "SubnetId": {
                    "Ref": "MountTargetSubnetTwo"
                },
                "SecurityGroups": [
                    {
                        "Fn::GetAtt": [
                            "MountTargetVPC",
                            "DefaultSecurityGroup"
                        ]
                    }
                ]
            }
        },
        "MountTargetResource3": {
            "Type": "AWS::EFS::MountTarget",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FileSystemResource"
                },
                "SubnetId": {
                    "Ref": "MountTargetSubnetThree"
                },
                "SecurityGroups": [
                    {
                        "Fn::GetAtt": [
                            "MountTargetVPC",
                            "DefaultSecurityGroup"
                        ]
                    }
                ]
            }
        },
        "AccessPointResource": {
            "Type": "AWS::EFS::AccessPoint",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FileSystemResource"
                },
                "PosixUser": {
                    "Uid": "13234",
                    "Gid": "1322",
                    "SecondaryGids": [
                        "1344",
                        "1452"
                    ]
                },
                "RootDirectory": {
                    "CreationInfo": {
                        "OwnerGid": "708798",
                        "OwnerUid": "7987987",
                        "Permissions": "0755"
                    },
                    "Path": "/testcfn/abc"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-efs-filesystem--examples--Create_an_encrypted_EFS_file_system_using_EFS_Standard_storage_classes--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MountTargetVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 172.31.0.0/16
 
  MountTargetSubnetOne:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 172.31.1.0/24
      VpcId: !Ref MountTargetVPC
     AvailabilityZone: "us-east-1a"

  MountTargetSubnetTwo:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 172.31.2.0/24
      VpcId: !Ref MountTargetVPC
      AvailabilityZone: "us-east-1b"

  MountTargetSubnetThree:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 172.31.3.0/24
      VpcId: !Ref MountTargetVPC
      AvailabilityZone: "us-east-1c"
 
  FileSystemResource:
    Type: 'AWS::EFS::FileSystem'
    Properties:
      BackupPolicy:
        Status: ENABLED
      PerformanceMode: maxIO
      Encrypted: true
      LifecyclePolicies:
        - TransitionToIA: AFTER_30_DAYS
        - TransitionToPrimaryStorageClass: AFTER_1_ACCESS
      FileSystemTags:
        - Key: Name
          Value: TestFileSystem
      FileSystemPolicy:
        Version: "2012-10-17"
        Statement:
          - Effect: "Allow"
            Action:
              - "elasticfilesystem:ClientMount"
            Principal:
                AWS: 'arn:aws:iam::111122223333:role/EfsReadOnly'
      KmsKeyId: !GetAtt 
        - key
        - Arn
  key:
    Type: AWS::KMS::Key
    Properties:
      KeyPolicy:
        Version: 2012-10-17
        Id: key-default-1
        Statement:
          - Sid: Allow administration of the key
            Effect: Allow
            Principal:
              AWS: !Join 
                - ''
                - - 'arn:aws:iam::'
                  - !Ref 'AWS::AccountId'
                  - ':root'
            Action:
              - 'kms:*'
            Resource: 
              - '*'

  MountTargetResource1:
    Type: AWS::EFS::MountTarget
    Properties:
      FileSystemId: !Ref FileSystemResource
      SubnetId: !Ref MountTargetSubnetOne
      SecurityGroups:
      - !GetAtt MountTargetVPC.DefaultSecurityGroup

  MountTargetResource2:
    Type: AWS::EFS::MountTarget
    Properties:
      FileSystemId: !Ref FileSystemResource
      SubnetId: !Ref MountTargetSubnetTwo
      SecurityGroups:
      - !GetAtt MountTargetVPC.DefaultSecurityGroup

  MountTargetResource3:
    Type: AWS::EFS::MountTarget
    Properties:
      FileSystemId: !Ref FileSystemResource
      SubnetId: !Ref MountTargetSubnetThree
      SecurityGroups:
      - !GetAtt MountTargetVPC.DefaultSecurityGroup
 
  AccessPointResource:
    Type: 'AWS::EFS::AccessPoint'
    Properties:
      FileSystemId: !Ref FileSystemResource
      PosixUser:
        Uid: "13234"
        Gid: "1322"
        SecondaryGids:
          - "1344"
          - "1452"
      RootDirectory:
        CreationInfo:
          OwnerGid: "708798"
          OwnerUid: "7987987"
          Permissions: "0755"
        Path: "/testcfn/abc"
```

### Create a file system using EFS One Zone storage classes<a name="aws-resource-efs-filesystem--examples--Create_a_file_system_using_EFS_One_Zone_storage_classes"></a>

The following example declares an encrypted Amazon EFS file system using One Zone storage classes in the us\-east\-1a Availability Zone\.

#### JSON<a name="aws-resource-efs-filesystem--examples--Create_a_file_system_using_EFS_One_Zone_storage_classes--json"></a>

```
"{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "MountTargetVPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": "172.31.0.0/16"
            }
        },
        "MountTargetSubnetOne": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "CidrBlock": "172.31.1.0/24",
                "VpcId": {
                    "Ref": "MountTargetVPC"
                },
                "AvailabilityZone": "us-east-1a"
            }
        },
       "FileSystemResource": {
            "Type": "AWS::EFS::FileSystem",
            "Properties": {
                "AvailabilityZoneName": "us-east-1a",
                "LifecyclePolicies":[
                    {
                        "TransitionToIA" : "AFTER_30_DAYS"
                    },
                    {
                        "TransitionToPrimaryStorageClass" : "AFTER_1_ACCESS"
                    }
                ],
                "Encrypted": true,
                "FileSystemTags": [
                    {
                        "Key": "Name",
                        "Value": "TestFileSystem"
                    }
                ],
                "FileSystemPolicy": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Action": [
                                "elasticfilesystem:ClientMount"
                            ],
                            "Principal":  {"AWS": "arn:aws:iam::111122223333:role/EfsReadOnly"}
                        }
                    ]
                },
                "BackupPolicy": {
                    "Status": "ENABLED"
                    },
                "KmsKeyId": {
                    "Fn::GetAtt": [
                        "key",
                        "Arn"
                    ]
                }
            } 
        },
        "key": {
            "Type": "AWS::KMS::Key",
            "Properties": {
                "KeyPolicy": {
                    "Version": "2012-10-17",
                    "Id": "key-default-1",
                    "Statement": [
                        {
                            "Sid": "Allow administration of the key",
                            "Effect": "Allow",
                            "Principal": {
                                "AWS": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "arn:aws:iam::",
                                            {
                                                "Ref": "AWS::AccountId"
                                            },
                                            ":root"
                                        ]
                                    ]
                                }
                            },
                            "Action": [
                                "kms:*"
                            ],
                            "Resource": "*"
                        }
                    ]
                }
            }
        },
        "MountTargetResource1": {
            "Type": "AWS::EFS::MountTarget",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FileSystemResource"
                },
                "SubnetId": {
                    "Ref": "MountTargetSubnetOne"
                },
                "SecurityGroups": [
                    {
                        "Fn::GetAtt": [
                            "MountTargetVPC",
                            "DefaultSecurityGroup"
                        ]
                    }
                ]
            }
        },
        "AccessPointResource": {
            "Type": "AWS::EFS::AccessPoint",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FileSystemResource"
                },
                "PosixUser": {
                    "Uid": "13234",
                    "Gid": "1322",
                    "SecondaryGids": [
                        "1344",
                        "1452"
                    ]
                },
                "RootDirectory": {
                    "CreationInfo": {
                        "OwnerGid": "708798",
                        "OwnerUid": "7987987",
                        "Permissions": "0755"
                    },
                    "Path": "/testcfn/abc"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-efs-filesystem--examples--Create_a_file_system_using_EFS_One_Zone_storage_classes--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MountTargetVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 172.31.0.0/16
 
  MountTargetSubnetOne:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 172.31.1.0/24
      VpcId: !Ref MountTargetVPC
      AvailabilityZone: "us-east-1a"
 
  FileSystemResource:
    Type: 'AWS::EFS::FileSystem'
    Properties:
      AvailabilityZoneName: us-east-1a
      BackupPolicy:
        Status: ENABLED
      Encrypted: true
      LifecyclePolicies:
        - TransitionToIA: AFTER_30_DAYS
        - TransitionToPrimaryStorageClass: AFTER_1_ACCESS
      FileSystemTags:
        - Key: Name
          Value: TestFileSystem
      FileSystemPolicy:
        Version: "2012-10-17"
        Statement:
          - Effect: "Allow"
            Action:
              - "elasticfilesystem:ClientMount"
            Principal:
                AWS: 'arn:aws:iam::111122223333:role/EfsReadOnly'
      KmsKeyId: !GetAtt 
        - key
        - Arn
  key:
    Type: AWS::KMS::Key
    Properties:
      KeyPolicy:
        Version: 2012-10-17
        Id: key-default-1
        Statement:
          - Sid: Allow administration of the key
            Effect: Allow
            Principal:
              AWS: !Join 
                - ''
                - - 'arn:aws:iam::'
                  - !Ref 'AWS::AccountId'
                  - ':root'
            Action:
              - 'kms:*'
            Resource: 
              - '*'

  MountTargetResource1:
    Type: AWS::EFS::MountTarget
    Properties:
      FileSystemId: !Ref FileSystemResource
      SubnetId: !Ref MountTargetSubnetOne
      SecurityGroups:
      - !GetAtt MountTargetVPC.DefaultSecurityGroup
 
  AccessPointResource:
    Type: 'AWS::EFS::AccessPoint'
    Properties:
      FileSystemId: !Ref FileSystemResource
      PosixUser:
        Uid: "13234"
        Gid: "1322"
        SecondaryGids:
          - "1344"
          - "1452"
      RootDirectory:
        CreationInfo:
          OwnerGid: "708798"
          OwnerUid: "7987987"
          Permissions: "0755"
        Path: "/testcfn/abc"
```

## See also<a name="aws-resource-efs-filesystem--seealso"></a>
+  [Amazon EFS: How it works](https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html) 
+  [Creating an Amazon EFS file system](https://docs.aws.amazon.com/efs/latest/ug/creating-using-fs.html) 


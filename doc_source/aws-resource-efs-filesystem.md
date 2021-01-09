# AWS::EFS::FileSystem<a name="aws-resource-efs-filesystem"></a>

The `AWS::EFS::FileSystem` resource creates a new, empty file system in Amazon Elastic File System \(Amazon EFS\)\. You must create a mount target \([AWS::EFS::MountTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-mounttarget.html)\) to mount your EFS file system on an Amazon Elastic Compute Cloud \(Amazon EC2\) instance or another compute resource\. 

## Syntax<a name="aws-resource-efs-filesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-efs-filesystem-syntax.json"></a>

```
{
  "Type" : "AWS::EFS::FileSystem",
  "Properties" : {
      "[BackupPolicy](#cfn-efs-filesystem-backuppolicy)" : BackupPolicy,
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
  [BackupPolicy](#cfn-efs-filesystem-backuppolicy): 
    BackupPolicy
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

`BackupPolicy`  <a name="cfn-efs-filesystem-backuppolicy"></a>
Use the `BackupPolicy` to turn automatic backups on or off for the file system\.  
*Required*: No  
*Type*: [BackupPolicy](aws-properties-efs-filesystem-backuppolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-efs-filesystem-encrypted"></a>
A Boolean value that, if true, creates an encrypted file system\. When creating an encrypted file system, you have the option of specifying a KmsKeyId for an existing AWS Key Management Service \(AWS KMS\) customer master key \(CMK\)\. If you don't specify a CMK, then the default CMK for Amazon EFS, `/aws/elasticfilesystem`, is used to protect the encrypted file system\.   
*Required*: Conditional  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemPolicy`  <a name="cfn-efs-filesystem-filesystempolicy"></a>
The `FileSystemPolicy` for the EFS file system\. A file system policy is an IAM resource policy used to control NFS access to an EFS file system\. For more information, see [Using IAM to Control NFS Access to Amazon EFS](https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html) in the *Amazon EFS User Guide*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileSystemTags`  <a name="cfn-efs-filesystem-filesystemtags"></a>
A value that specifies to create one or more tags associated with the file system\. Each tag is a user\-defined key\-value pair\. Name your file system on creation by including a `"Key":"Name","Value":"{value}"` key\-value pair\.  
*Required*: No  
*Type*: List of [ElasticFileSystemTag](aws-properties-efs-filesystem-elasticfilesystemtag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-efs-filesystem-kmskeyid"></a>
The ID of the AWS KMS customer master key \(CMK\) to be used to protect the encrypted file system\. This parameter is only required if you want to use a nondefault CMK\. If this parameter is not specified, the default CMK for Amazon EFS is used\. This ID can be in one of the following formats:  
+ Key ID \- A unique identifier of the key, for example `1234abcd-12ab-34cd-56ef-1234567890ab`\.
+ ARN \- An Amazon Resource Name \(ARN\) for the key, for example `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab`\.
+ Key alias \- A previously created display name for a key, for example `alias/projectKey1`\.
+ Key alias ARN \- An ARN for a key alias, for example `arn:aws:kms:us-west-2:444455556666:alias/projectKey1`\.
If `KmsKeyId` is specified, the `Encrypted` parameter must be set to true\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^([0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}|alias/[a-zA-Z0-9/_-]+|(arn:aws[-a-z]*:kms:[a-z0-9-]+:\d{12}:((key/[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12})|(alias/[a-zA-Z0-9/_-]+))))$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LifecyclePolicies`  <a name="cfn-efs-filesystem-lifecyclepolicies"></a>
A list of policies used by EFS lifecycle management to transition files to the Infrequent Access \(IA\) storage class\.  
*Required*: No  
*Type*: List of [LifecyclePolicy](aws-properties-efs-filesystem-lifecyclepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerformanceMode`  <a name="cfn-efs-filesystem-performancemode"></a>
The performance mode of the file system\. We recommend `generalPurpose` performance mode for most file systems\. File systems using the `maxIO` performance mode can scale to higher levels of aggregate throughput and operations per second with a tradeoff of slightly higher latencies for most file operations\. The performance mode can't be changed after the file system has been created\.  
*Required*: No  
*Type*: String  
*Allowed values*: `generalPurpose | maxIO`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisionedThroughputInMibps`  <a name="cfn-efs-filesystem-provisionedthroughputinmibps"></a>
The throughput, measured in MiB/s, that you want to provision for a file system that you're creating\. Valid values are 1\-1024\. Required if `ThroughputMode` is set to `provisioned`\. The upper limit for throughput is 1024 MiB/s\. You can get this limit increased by contacting AWS Support\. For more information, see [Amazon EFS Limits That You Can Increase](https://docs.aws.amazon.com/efs/latest/ug/limits.html#soft-limits) in the *Amazon EFS User Guide\.*   
*Required*: Conditional  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThroughputMode`  <a name="cfn-efs-filesystem-throughputmode"></a>
The throughput mode for the file system to be created\. There are two throughput modes to choose from for your file system: `bursting` and `provisioned`\. If you set `ThroughputMode` to `provisioned`, you must also set a value for `ProvisionedThroughPutInMibps`\. You can decrease your file system's throughput in Provisioned Throughput mode or change between the throughput modes as long as it’s been more than 24 hours since the last decrease or throughput mode change\. For more, see [Specifying Throughput with Provisioned Mode](https://docs.aws.amazon.com/efs/latest/ug/performance.html#provisioned-throughput) in the *Amazon EFS User Guide\.*   
*Required*: No  
*Type*: String  
*Allowed values*: `bursting | provisioned`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-efs-filesystem-return-values"></a>

### Ref<a name="aws-resource-efs-filesystem-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID\. For example: 

 `{"Ref":"fs-12345678"}`\.

For the Amazon EFS file system `fs-12345678`, Ref returns the file system ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-efs-filesystem-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-efs-filesystem-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`FileSystemId`  <a name="FileSystemId-fn::getatt"></a>
The ID of the EFS file system\. For example: `fs-0123456`

## Examples<a name="aws-resource-efs-filesystem--examples"></a>



### Create an Encrypted File System<a name="aws-resource-efs-filesystem--examples--Create_an_Encrypted_File_System"></a>

The following example declares an encrypted Amazon EFS file system\.

#### JSON<a name="aws-resource-efs-filesystem--examples--Create_an_Encrypted_File_System--json"></a>

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
                "AvailabilityZone": "us-east-1a"
            }
        },
        "MountTargetSubnetThree": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "CidrBlock": "172.31.3.0/24",
                "VpcId": {
                    "Ref": "MountTargetVPC"
                },
                "AvailabilityZone": "us-east-1a"
            }
        },
       "FileSystemResource": {
            "Type": "AWS::EFS::FileSystem",
            "Properties": {
                "PerformanceMode": "maxIO",
                "LifecyclePolicies":[
                    {
                        "TransitionToIA" : "AFTER_30_DAYS"
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
                            "Principal":  {"AWS": "arn:aws:iam::111122223333:root"}
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
                            "Resource": "*",
                            "AWS": "*"
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

#### YAML<a name="aws-resource-efs-filesystem--examples--Create_an_Encrypted_File_System--yaml"></a>

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
      AvailabilityZone: "us-east-1a"

  MountTargetSubnetThree:
    Type: AWS::EC2::Subnet
    Properties:
      CidrBlock: 172.31.3.0/24
      VpcId: !Ref MountTargetVPC
      AvailabilityZone: "us-east-1a"
 
  FileSystemResource:
    Type: 'AWS::EFS::FileSystem'
    Properties:
      BackupPolicy:
        Status: ENABLED
      PerformanceMode: maxIO
      Encrypted: true
      LifecyclePolicies:
        - TransitionToIA: AFTER_30_DAYS
      FileSystemTags:
        - Key: Name
          Value: TestFileSystem
      FileSystemPolicy:
        Version: "2012-10-17"
        Statement:
          - Effect: "Allow"
            Action:
              - "elasticfilesystem:ClientMount"
            Principal:'arn:aws:iam::111122223333:root'
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
            Resource: '*'
            AWS: "*"

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

## See also<a name="aws-resource-efs-filesystem--seealso"></a>
+  [Amazon EFS: How It Works](https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html) 
+  [Creating an Amazon Elastic File System](https://docs.aws.amazon.com/efs/latest/ug/creating-using-fs.html) 


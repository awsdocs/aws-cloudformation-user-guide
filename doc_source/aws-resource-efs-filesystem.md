# AWS::EFS::FileSystem<a name="aws-resource-efs-filesystem"></a>

The `AWS::EFS::FileSystem` resource creates a new, empty file system in Amazon Elastic File System \(Amazon EFS\)\. You must create a mount target \([AWS::EFS::MountTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-mounttarget.html)\) to mount your EFS file system on an Amazon Elastic Compute Cloud \(Amazon EC2\) instance or another resource\. 

## Syntax<a name="aws-resource-efs-filesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-efs-filesystem-syntax.json"></a>

```
{
  "Type" : "AWS::EFS::FileSystem",
  "Properties" : {
      "[Encrypted](#cfn-efs-filesystem-encrypted)" : Boolean,
      "[FileSystemTags](#cfn-efs-filesystem-filesystemtags)" : [ [ElasticFileSystemTag](aws-properties-efs-filesystem-filesystemtags.md), ... ],
      "[KmsKeyId](#cfn-efs-filesystem-kmskeyid)" : String,
      "[PerformanceMode](#cfn-efs-filesystem-performancemode)" : String,
      "[ProvisionedThroughputInMibps](#cfn-elasticfilesystem-filesystem-provisionedthroughputinmibps)" : Double,
      "[ThroughputMode](#cfn-elasticfilesystem-filesystem-throughputmode)" : String
    }
}
```

### YAML<a name="aws-resource-efs-filesystem-syntax.yaml"></a>

```
Type: AWS::EFS::FileSystem
Properties: 
  [Encrypted](#cfn-efs-filesystem-encrypted): Boolean
  [FileSystemTags](#cfn-efs-filesystem-filesystemtags): 
    - [ElasticFileSystemTag](aws-properties-efs-filesystem-filesystemtags.md)
  [KmsKeyId](#cfn-efs-filesystem-kmskeyid): String
  [PerformanceMode](#cfn-efs-filesystem-performancemode): String
  [ProvisionedThroughputInMibps](#cfn-elasticfilesystem-filesystem-provisionedthroughputinmibps): Double
  [ThroughputMode](#cfn-elasticfilesystem-filesystem-throughputmode): String
```

## Properties<a name="aws-resource-efs-filesystem-properties"></a>

`Encrypted`  <a name="cfn-efs-filesystem-encrypted"></a>
A Boolean value that, if true, creates an encrypted file system\. When creating an encrypted file system, you have the option of specifying a KmsKeyId for an existing AWS Key Management Service \(AWS KMS\) customer master key \(CMK\)\. If you don't specify a CMK, then the default CMK for Amazon EFS, `/aws/elasticfilesystem`, is used to protect the encrypted file system\.   
*Required*: Conditional  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemTags`  <a name="cfn-efs-filesystem-filesystemtags"></a>
A value that specifies to create one or more tags associated with the file system\. Each tag is a user\-defined key\-value pair\. Name your file system on creation by including a `"Key":"Name","Value":"{value}"` key\-value pair\.  
*Required*: No  
*Type*: List of [ElasticFileSystemTag](aws-properties-efs-filesystem-filesystemtags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-efs-filesystem-kmskeyid"></a>
The ID of the AWS KMS CMK to be used to protect the encrypted file system\. This parameter is only required if you want to use a nondefault CMK\. If this parameter is not specified, the default CMK for Amazon EFS is used\. This ID can be in one of the following formats:  
+ Key ID \- A unique identifier of the key, for example `1234abcd-12ab-34cd-56ef-1234567890ab`\.
+ ARN \- An Amazon Resource Name \(ARN\) for the key, for example `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab`\.
+ Key alias \- A previously created display name for a key, for example `alias/projectKey1`\.
+ Key alias ARN \- An ARN for a key alias, for example `arn:aws:kms:us-west-2:444455556666:alias/projectKey1`\.
If `KmsKeyId` is specified, the `Encrypted` parameter must be set to true\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PerformanceMode`  <a name="cfn-efs-filesystem-performancemode"></a>
The performance mode of the file system\. We recommend `generalPurpose` performance mode for most file systems\. File systems using the `maxIO` performance mode can scale to higher levels of aggregate throughput and operations per second with a tradeoff of slightly higher latencies for most file operations\. The performance mode can't be changed after the file system has been created\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `generalPurpose | maxIO`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisionedThroughputInMibps`  <a name="cfn-elasticfilesystem-filesystem-provisionedthroughputinmibps"></a>
The throughput, measured in MiB/s, that you want to provision for a file system that you're creating\. Valid values are 1\-1024\. Required if `ThroughputMode` is set to `provisioned`\. The upper limit for throughput is 1024 MiB/s\. You can get this limit increased by contacting AWS Support\. For more information, see [Amazon EFS Limits That You Can Increase](https://docs.aws.amazon.com/efs/latest/ug/limits.html#soft-limits) in the *Amazon EFS User Guide\.*   
*Required*: Conditional  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThroughputMode`  <a name="cfn-elasticfilesystem-filesystem-throughputmode"></a>
The throughput mode for the file system to be created\. There are two throughput modes to choose from for your file system: `bursting` and `provisioned`\. If you set `ThroughputMode` to `provisioned`, you must also set a value for `ProvisionedThroughPutInMibps`\. You can decrease your file system's throughput in Provisioned Throughput mode or change between the throughput modes as long as it’s been more than 24 hours since the last decrease or throughput mode change\. For more, see [Specifying Throughput with Provisioned Mode](https://docs.aws.amazon.com/efs/latest/ug/performance.html#provisioned-throughput) in the *Amazon EFS User Guide\.*   
*Required*: No  
*Type*: String  
*Allowed Values*: `bursting | provisioned`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-efs-filesystem-return-values"></a>

### Ref<a name="aws-resource-efs-filesystem-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID\. For example: 

 `{"Ref":"fs-12345678"}`\.

For the Amazon EFS file system `fs-12345678`, Ref returns the file system ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-efs-filesystem--examples"></a>

### Create an Encrypted File System<a name="aws-resource-efs-filesystem--examples--Create_an_Encrypted_File_System"></a>

The following example declares an encrypted Amazon EFS file system\.

#### JSON<a name="aws-resource-efs-filesystem--examples--Create_an_Encrypted_File_System--json"></a>

```
"Resources": {
        "filesystem": {
            "Type": "AWS::EFS::FileSystem",
            "Properties": {
                "Encrypted": true,
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
        }
    },
    "Outputs": {
        "KeyId": {
            "Value": {
                "Fn::GetAtt": [
                    "key",
                    "Arn"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-efs-filesystem--examples--Create_an_Encrypted_File_System--yaml"></a>

```
Resources:
  filesystem:
    Type: AWS::EFS::FileSystem
    Properties:
      Encrypted: true
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
Outputs:
  KeyId:
    Value: !GetAtt 
      - key
- Arn
```

## See Also<a name="aws-resource-efs-filesystem--seealso"></a>
+  [Amazon EFS: How It Works](https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html) 
+  [Creating an Amazon Elastic File System](https://docs.aws.amazon.com/efs/latest/ug/creating-using-fs.html) 
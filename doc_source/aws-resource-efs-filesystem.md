# AWS::EFS::FileSystem<a name="aws-resource-efs-filesystem"></a>

The `AWS::EFS::FileSystem` resource creates a new, empty file system in Amazon Elastic File System \(Amazon EFS\)\. You must create a mount target \([AWS::EFS::MountTarget](aws-resource-efs-mounttarget.md)\) to mount your Amazon EFS file system on an Amazon Elastic Compute Cloud \(Amazon EC2\) instance\. For more information, see the [CreateFileSystem](http://docs.aws.amazon.com/efs/latest/ug/API_CreateFileSystem.html) API in the *Amazon Elastic File System User Guide*\.

**Topics**
+ [Syntax](#aws-resource-efs-filesystem-syntax)
+ [Properties](#w3ab2c21c10d571b9)
+ [Return Value](#w3ab2c21c10d571c11)
+ [Example](#w3ab2c21c10d571c13)
+ [Additional Resources](#w3ab2c21c10d571c15)

## Syntax<a name="aws-resource-efs-filesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-efs-filesystem-syntax.json"></a>

```
{
  "Type" : "AWS::EFS::FileSystem",
  "Properties" : {
    "[Encrypted](#cfn-efs-filesystem-encrypted)" : Boolean,
    "[FileSystemTags](#cfn-efs-filesystem-filesystemtags)" : [ FileSystemTags, ... ],
    "[KmsKeyId](#cfn-efs-filesystem-kmskeyid)" : String,
    "[PerformanceMode](#cfn-efs-filesystem-performancemode)" : String
  }
}
```

### YAML<a name="aws-resource-efs-filesystem-syntax.yaml"></a>

```
Type: "AWS::EFS::FileSystem"
Properties: 
  [Encrypted](#cfn-efs-filesystem-encrypted): Boolean
  [FileSystemTags](#cfn-efs-filesystem-filesystemtags):
    - FileSystemTags
  [KmsKeyId](#cfn-efs-filesystem-kmskeyid): String
  [PerformanceMode](#cfn-efs-filesystem-performancemode): String
```

## Properties<a name="w3ab2c21c10d571b9"></a>

`FileSystemTags`  <a name="cfn-efs-filesystem-filesystemtags"></a>
Tags to associate with the file system\.  
*Required*: No  
*Type*: [Amazon Elastic File System FileSystem FileSystemTags](aws-properties-efs-filesystem-filesystemtags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Encrypted`  <a name="cfn-efs-filesystem-encrypted"></a>
A boolean value that, if true, creates an encrypted file system\. For more information, see [CreateFileSystem](http://docs.aws.amazon.com/efs/latest/ug/API_CreateFileSystem.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KmsKeyId`  <a name="cfn-efs-filesystem-kmskeyid"></a>
The ID of the AWS KMS customer master key \(CMK\) to use to protect the encrypted file system\. This parameter is only required if you want to use a non\-default CMK\. For more information, see [CreateFileSystem](http://docs.aws.amazon.com/efs/latest/ug/API_CreateFileSystem.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: Conditional\. This parameter is required if you use a non\-default CMK\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PerformanceMode`  <a name="cfn-efs-filesystem-performancemode"></a>
The performance mode of the file system\. For valid values, see the `PerformanceMode` parameter for the [CreateFileSystem](http://docs.aws.amazon.com/efs/latest/ug/API_CreateFileSystem.html) action in the *Amazon Elastic File System User Guide*\.  
For more information about performance modes, see [Amazon EFS Performance](http://docs.aws.amazon.com/efs/latest/ug/performance.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d571c11"></a>

### Ref<a name="w3ab2c21c10d571c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID, such as `fs-47a2c22e`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d571c13"></a>

The following example declares an encrypted file system:

### JSON<a name="aws-resource-efs-filesystem-example.json"></a>

```
{
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

### YAML<a name="aws-resource-efs-filesystem-example.yaml"></a>

```
Resources:
  filesystem:
    Type: 'AWS::EFS::FileSystem'
    Properties:
      Encrypted: true
      KmsKeyId: !GetAtt 
        - key
        - Arn
  key:
    Type: 'AWS::KMS::Key'
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

## Additional Resources<a name="w3ab2c21c10d571c15"></a>

For a complete sample template, see [Amazon Elastic File System Sample Template](quickref-efs.md)\.
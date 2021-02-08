# AWS::S3::Bucket ServerSideEncryptionRule<a name="aws-properties-s3-bucket-serversideencryptionrule"></a>

Specifies the default server\-side encryption configuration\.

## Syntax<a name="aws-properties-s3-bucket-serversideencryptionrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-serversideencryptionrule-syntax.json"></a>

```
{
  "[BucketKeyEnabled](#cfn-s3-bucket-serversideencryptionrule-bucketkeyenabled)" : Boolean,
  "[ServerSideEncryptionByDefault](#cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault)" : ServerSideEncryptionByDefault
}
```

### YAML<a name="aws-properties-s3-bucket-serversideencryptionrule-syntax.yaml"></a>

```
  [BucketKeyEnabled](#cfn-s3-bucket-serversideencryptionrule-bucketkeyenabled): Boolean
  [ServerSideEncryptionByDefault](#cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault): 
    ServerSideEncryptionByDefault
```

## Properties<a name="aws-properties-s3-bucket-serversideencryptionrule-properties"></a>

`BucketKeyEnabled`  <a name="cfn-s3-bucket-serversideencryptionrule-bucketkeyenabled"></a>
Specifies whether Amazon S3 should use an S3 Bucket Key with server\-side encryption using KMS \(SSE\-KMS\) for new objects in the bucket\. Existing objects are not affected\. Setting the `BucketKeyEnabled` element to `true` causes Amazon S3 to use an S3 Bucket Key\. By default, S3 Bucket Key is not enabled\.  
For more information, see [Amazon S3 Bucket Keys](https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-key.html) in the *Amazon S3 Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerSideEncryptionByDefault`  <a name="cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault"></a>
Specifies the default server\-side encryption to apply to new objects in the bucket\. If a PUT Object request doesn't specify any server\-side encryption, this default encryption will be applied\.  
*Required*: No  
*Type*: [ServerSideEncryptionByDefault](aws-properties-s3-bucket-serversideencryptionbydefault.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-serversideencryptionrule--examples"></a>

### Create a bucket with default encryption<a name="aws-properties-s3-bucket-serversideencryptionrule--examples--Create_a_bucket_with_default_encryption"></a>

The following example creates a bucket with server\-side bucket encryption configured\. This example uses KMS\-managed keys\. You can use S3\-managed keys instead by modifying the [Amazon S3 Bucket ServerSideEncryptionByDefault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-serversideencryptionbydefault.html) property\.

#### JSON<a name="aws-properties-s3-bucket-serversideencryptionrule--examples--Create_a_bucket_with_default_encryption--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "S3 bucket with default encryption",
    "Resources": {
        "EncryptedS3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "BucketName": {
                    "Fn::Sub": "encryptedbucket-${AWS::Region}-${AWS::AccountId}"
                },
                "BucketEncryption": {
                    "ServerSideEncryptionConfiguration": [
                        {
                            "ServerSideEncryptionByDefault": {
                                "SSEAlgorithm": "aws:kms",
                                "KMSMasterKeyID": "KMS-KEY-ARN"
                            }
                        }
                    ]
                }
            },
            "DeletionPolicy": "Delete"
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-serversideencryptionrule--examples--Create_a_bucket_with_default_encryption--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: S3 bucket with default encryption
Resources:
  EncryptedS3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      BucketName: !Sub 'encryptedbucket-${AWS::Region}-${AWS::AccountId}'
      BucketEncryption:
        ServerSideEncryptionConfiguration:
          - ServerSideEncryptionByDefault:
              SSEAlgorithm: 'aws:kms'
              KMSMasterKeyID: KMS-KEY-ARN
    DeletionPolicy: Delete
```

### Create a bucket using AWS KMS server\-side encryption with an S3 Bucket Key<a name="aws-properties-s3-bucket-serversideencryptionrule--examples--Create_a_bucket_using_AWS_KMS_server-side_encryption_with_an_S3_Bucket_Key"></a>

The following example creates a bucket that specifies default encryption using AWS KMS server\-side encryption with an S3 Bucket Key\. The example uses a customer managed AWS KMS customer master key \(CMK\)\.

#### JSON<a name="aws-properties-s3-bucket-serversideencryptionrule--examples--Create_a_bucket_using_AWS_KMS_server-side_encryption_with_an_S3_Bucket_Key--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "S3 bucket with default encryption using SSE-KMS with an S3 Bucket Key",
    "Resources": {
        "EncryptedS3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "BucketName": {
                    "Fn::Sub": "encryptedbucket-${AWS::Region}-${AWS::AccountId}"
                },
                "BucketEncryption": {
                    "ServerSideEncryptionConfiguration": [
                        {
                            "ServerSideEncryptionByDefault": {
                                "SSEAlgorithm": "aws:kms",
                                "KMSMasterKeyID": "KMS-KEY-ARN"
                            },
                            "BucketKeyEnabled": true
                        }
                    ]
                }
            },
            "DeletionPolicy": "Delete"
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-serversideencryptionrule--examples--Create_a_bucket_using_AWS_KMS_server-side_encryption_with_an_S3_Bucket_Key--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: S3 bucket with default encryption using SSE-KMS with an S3 Bucket Key
Resources:
  EncryptedS3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      BucketName: !Sub 'encryptedbucket-${AWS::Region}-${AWS::AccountId}'
      BucketEncryption:
        ServerSideEncryptionConfiguration:
          - ServerSideEncryptionByDefault:
              SSEAlgorithm: 'aws:kms'
              KMSMasterKeyID: KMS-KEY-ARN
            BucketKeyEnabled: true
    DeletionPolicy: Delete
```
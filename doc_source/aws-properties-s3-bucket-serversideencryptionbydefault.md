# AWS::S3::Bucket ServerSideEncryptionByDefault<a name="aws-properties-s3-bucket-serversideencryptionbydefault"></a>

Describes the default server\-side encryption to apply to new objects in the bucket\. If a PUT Object request doesn't specify any server\-side encryption, this default encryption will be applied\. If you don't specify a customer managed key at configuration, Amazon S3 automatically creates an AWS KMS key in your AWS account the first time that you add an object encrypted with SSE\-KMS to a bucket\. By default, Amazon S3 uses this KMS key for SSE\-KMS\. For more information, see [PUT Bucket encryption](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTencryption.html) in the *Amazon S3 API Reference*\.

## Syntax<a name="aws-properties-s3-bucket-serversideencryptionbydefault-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-serversideencryptionbydefault-syntax.json"></a>

```
{
  "[KMSMasterKeyID](#cfn-s3-bucket-serversideencryptionbydefault-kmsmasterkeyid)" : String,
  "[SSEAlgorithm](#cfn-s3-bucket-serversideencryptionbydefault-ssealgorithm)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-serversideencryptionbydefault-syntax.yaml"></a>

```
  [KMSMasterKeyID](#cfn-s3-bucket-serversideencryptionbydefault-kmsmasterkeyid): String
  [SSEAlgorithm](#cfn-s3-bucket-serversideencryptionbydefault-ssealgorithm): String
```

## Properties<a name="aws-properties-s3-bucket-serversideencryptionbydefault-properties"></a>

`KMSMasterKeyID`  <a name="cfn-s3-bucket-serversideencryptionbydefault-kmsmasterkeyid"></a>
KMS key ID to use for the default encryption\. This parameter is allowed if SSEAlgorithm is aws:kms\.  
You can specify the key ID, key alias, or the Amazon Resource Name \(ARN\) of the CMK\. However, if you are using encryption with cross\-account operations, you must use a fully qualified CMK ARN\. For more information, see [Using encryption for cross\-account operations](https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html#bucket-encryption-update-bucket-policy)\.  
For example:  
+ Key ID: `1234abcd-12ab-34cd-56ef-1234567890ab`
+ Key ARN: `arn:aws:kms:us-east-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab`
Amazon S3 only supports symmetric KMS keys and not asymmetric KMS keys\. For more information, see [Using Symmetric and Asymmetric Keys](https://docs.aws.amazon.com/kms/latest/developerguide/symmetric-asymmetric.html) in the *AWS Key Management Service Developer Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSEAlgorithm`  <a name="cfn-s3-bucket-serversideencryptionbydefault-ssealgorithm"></a>
Server\-side encryption algorithm to use for the default encryption\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AES256 | aws:kms | aws:kms:dsse`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-serversideencryptionbydefault--examples"></a>

### Create a bucket with default encryption<a name="aws-properties-s3-bucket-serversideencryptionbydefault--examples--Create_a_bucket_with_default_encryption"></a>

The following example creates a bucket with server\-side bucket encryption configured\. This example uses encryption with AWS KMS keys \(SSE\-KMS\)\. You can use dual\-layer server\-side encryption with AWS KMS keys \(DSSE\-KMS\) by specifying `aws:kms:dsse` for `SSEAlgorithm`\. You can also use server\-side encryption with S3\-managed keys \(SSE\-S3\) by modifying the [Amazon S3 Bucket ServerSideEncryptionByDefault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-serversideencryptionbydefault.html) property to specify `AES256` for `SSEAlgorithm`\. For more information, see [Using SSE\-S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingServerSideEncryption.html) in the *Amazon S3 User Guide*\.

#### JSON<a name="aws-properties-s3-bucket-serversideencryptionbydefault--examples--Create_a_bucket_with_default_encryption--json"></a>

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

#### YAML<a name="aws-properties-s3-bucket-serversideencryptionbydefault--examples--Create_a_bucket_with_default_encryption--yaml"></a>

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
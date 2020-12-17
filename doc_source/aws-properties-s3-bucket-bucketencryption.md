# AWS::S3::Bucket BucketEncryption<a name="aws-properties-s3-bucket-bucketencryption"></a>

Specifies default encryption for a bucket using server\-side encryption with Amazon S3\-managed keys \(SSE\-S3\) or AWS KMS\-managed keys \(SSE\-KMS\) bucket\. For information about the Amazon S3 default encryption feature, see [Amazon S3 Default Encryption for S3 Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html) in the *Amazon Simple Storage Service Developer Guide*\.

## Syntax<a name="aws-properties-s3-bucket-bucketencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-bucketencryption-syntax.json"></a>

```
{
  "[ServerSideEncryptionConfiguration](#cfn-s3-bucket-bucketencryption-serversideencryptionconfiguration)" : [ ServerSideEncryptionRule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-bucketencryption-syntax.yaml"></a>

```
  [ServerSideEncryptionConfiguration](#cfn-s3-bucket-bucketencryption-serversideencryptionconfiguration): 
    - ServerSideEncryptionRule
```

## Properties<a name="aws-properties-s3-bucket-bucketencryption-properties"></a>

`ServerSideEncryptionConfiguration`  <a name="cfn-s3-bucket-bucketencryption-serversideencryptionconfiguration"></a>
Specifies the default server\-side\-encryption configuration\.  
*Required*: Yes  
*Type*: List of [ServerSideEncryptionRule](aws-properties-s3-bucket-serversideencryptionrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-bucketencryption--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)


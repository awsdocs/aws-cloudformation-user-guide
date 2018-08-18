# Amazon S3 Bucket BucketEncryption<a name="aws-properties-s3-bucket-bucketencryption"></a>

The `BucketEncryption` property is part of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource that specifies default encryption for a bucket using server\-side encryption with Amazon S3\-managed keys SSE\-S3 or AWS KMS\-managed Keys \(SSE\-KMS\) bucket\. For information about the Amazon S3 default encryption feature, see [Amazon S3 Default Bucket Encryption](http://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html) in the *Amazon Simple Storage Service Developer Guide*\.

## Syntax<a name="w3ab2c21c14e1692b5"></a>

### JSON<a name="aws-properties-s3-bucket-bucketencryption.json"></a>

```
{
  "[ServerSideEncryptionConfiguration](#cfn-s3-bucket-bucketencryption-serversideencryptionconfiguration)" : [ [*ServerSideEncryptionRule*](aws-properties-s3-bucket-serversideencryptionrule.md), ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-bucketencryption.yaml"></a>

```
[ServerSideEncryptionConfiguration](#cfn-s3-bucket-bucketencryption-serversideencryptionconfiguration): 
  - [*ServerSideEncryptionRule*](aws-properties-s3-bucket-serversideencryptionrule.md)
```

## Properties<a name="w3ab2c21c14e1692b7"></a>

`ServerSideEncryptionConfiguration`  <a name="cfn-s3-bucket-bucketencryption-serversideencryptionconfiguration"></a>
Specifies the server\-side encryption by default configuration\.  
*Required*: Yes  
*Type:* List of [Amazon S3 Bucket ServerSideEncryptionRule](aws-properties-s3-bucket-serversideencryptionrule.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
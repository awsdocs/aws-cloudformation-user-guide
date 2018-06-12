# Amazon S3 Bucket ServerSideEncryptionByDefault<a name="aws-properties-s3-bucket-serversideencryptionbydefault"></a>

The `ServerSideEncryptionByDefault` property is part of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource that specifies the server\-side encryption by default\. For more information, see [PUT Bucket encryption](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTencryption.html) in the *Amazon Simple Storage Service API Reference*\.

## Syntax<a name="w3ab2c21c14e1776b5"></a>

### JSON<a name="aws-properties-s3-bucket-serversideencryptionbydefault.json"></a>

```
{
  "[KMSMasterKeyID](#cfn-s3-bucket-serversideencryptionbydefault-kmsmasterkeyid)" : String,
  "[SSEAlgorithm](#cfn-s3-bucket-serversideencryptionbydefault-ssealgorithm)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-serversideencryptionbydefault.yaml"></a>

```
[KMSMasterKeyID](#cfn-s3-bucket-serversideencryptionbydefault-kmsmasterkeyid): String
[SSEAlgorithm](#cfn-s3-bucket-serversideencryptionbydefault-ssealgorithm): String
```

## Properties<a name="w3ab2c21c14e1776b7"></a>

`KMSMasterKeyID`  <a name="cfn-s3-bucket-serversideencryptionbydefault-kmsmasterkeyid"></a>
The AWS KMS master key ID used for the SSE\-KMS encryption\.   
Constraint: Can only be used when you set the value of `SSEAlgorithm` as `aws:kms`\. The default aws/s3 AWS KMS master key is used if this property is absent while `SSEAlgorithm` is `aws:kms`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SSEAlgorithm`  <a name="cfn-s3-bucket-serversideencryptionbydefault-ssealgorithm"></a>
The server\-side encryption algorithm to use\. Valid values include `AES256` and `aws:kms`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
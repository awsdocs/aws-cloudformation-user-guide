# AWS::S3::Bucket ServerSideEncryptionByDefault<a name="aws-properties-s3-bucket-serversideencryptionbydefault"></a>

Describes the default server\-side encryption to apply to new objects in the bucket\. If a PUT Object request doesn't specify any server\-side encryption, this default encryption will be applied\. For more information, see [PUT Bucket encryption](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTencryption.html) in the *Amazon Simple Storage Service API Reference*\.

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
KMS master key ID to use for the default encryption\. This parameter is allowed if and only if `SSEAlgorithm` is set to `aws:kms`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSEAlgorithm`  <a name="cfn-s3-bucket-serversideencryptionbydefault-ssealgorithm"></a>
Server\-side encryption algorithm to use for the default encryption\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `AES256 | aws:kms`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
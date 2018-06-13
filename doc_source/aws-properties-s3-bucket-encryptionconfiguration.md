# Amazon S3 Bucket EncryptionConfiguration<a name="aws-properties-s3-bucket-encryptionconfiguration"></a>

<a name="aws-properties-s3-bucket-encryptionconfiguration-description"></a>The `EncryptionConfiguration` property type specifies encryption\-related information for an Amazon S3 bucket that is a destination for replicated objects\.

<a name="aws-properties-s3-bucket-encryptionconfiguration-inheritance"></a>`EncryptionConfiguration` is a property type of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource\.

## Syntax<a name="aws-properties-s3-bucket-encryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-encryptionconfiguration-syntax.json"></a>

```
{
  "[ReplicaKmsKeyID](#cfn-s3-bucket-encryptionconfiguration-replicakmskeyid)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-encryptionconfiguration-syntax.yaml"></a>

```
[ReplicaKmsKeyID](#cfn-s3-bucket-encryptionconfiguration-replicakmskeyid): String
```

## Properties<a name="aws-properties-s3-bucket-encryptionconfiguration-properties"></a>

`ReplicaKmsKeyID`  <a name="cfn-s3-bucket-encryptionconfiguration-replicakmskeyid"></a>
Specifies the AWS KMS Key ID \(Key ARN or Alias ARN\) for the destination bucket\. Amazon S3 uses this key to encrypt replicas\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
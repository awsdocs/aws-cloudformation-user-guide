# AWS::ECR::Repository EncryptionConfiguration<a name="aws-properties-ecr-repository-encryptionconfiguration"></a>

The encryption configuration for the repository\. This determines how the contents of your repository are encrypted at rest\.

By default, when no encryption configuration is set or the `AES256` encryption type is used, Amazon ECR uses server\-side encryption with Amazon S3\-managed encryption keys which encrypts your data at rest using an AES\-256 encryption algorithm\. This does not require any action on your part\.

For more control over the encryption of the contents of your repository, you can use server\-side encryption with AWS Key Management Service key stored in AWS Key Management Service \(AWS KMS\) to encrypt your images\. For more information, see [Amazon ECR encryption at rest](https://docs.aws.amazon.com/AmazonECR/latest/userguide/encryption-at-rest.html) in the *Amazon Elastic Container Registry User Guide*\.

## Syntax<a name="aws-properties-ecr-repository-encryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecr-repository-encryptionconfiguration-syntax.json"></a>

```
{
  "[EncryptionType](#cfn-ecr-repository-encryptionconfiguration-encryptiontype)" : String,
  "[KmsKey](#cfn-ecr-repository-encryptionconfiguration-kmskey)" : String
}
```

### YAML<a name="aws-properties-ecr-repository-encryptionconfiguration-syntax.yaml"></a>

```
  [EncryptionType](#cfn-ecr-repository-encryptionconfiguration-encryptiontype): String
  [KmsKey](#cfn-ecr-repository-encryptionconfiguration-kmskey): String
```

## Properties<a name="aws-properties-ecr-repository-encryptionconfiguration-properties"></a>

`EncryptionType`  <a name="cfn-ecr-repository-encryptionconfiguration-encryptiontype"></a>
The encryption type to use\.  
If you use the `KMS` encryption type, the contents of the repository will be encrypted using server\-side encryption with AWS Key Management Service key stored in AWS KMS\. When you use AWS KMS to encrypt your data, you can either use the default AWS managed AWS KMS key for Amazon ECR, or specify your own AWS KMS key, which you already created\. For more information, see [Protecting data using server\-side encryption with an AWS KMS key stored in AWS Key Management Service \(SSE\-KMS\)](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingKMSEncryption.html) in the *Amazon Simple Storage Service Console Developer Guide*\.  
If you use the `AES256` encryption type, Amazon ECR uses server\-side encryption with Amazon S3\-managed encryption keys which encrypts the images in the repository using an AES\-256 encryption algorithm\. For more information, see [Protecting data using server\-side encryption with Amazon S3\-managed encryption keys \(SSE\-S3\)](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingServerSideEncryption.html) in the *Amazon Simple Storage Service Console Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AES256 | KMS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKey`  <a name="cfn-ecr-repository-encryptionconfiguration-kmskey"></a>
If you use the `KMS` encryption type, specify the AWS KMS key to use for encryption\. The alias, key ID, or full ARN of the AWS KMS key can be specified\. The key must exist in the same Region as the repository\. If no key is specified, the default AWS managed AWS KMS key for Amazon ECR will be used\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
# AWS::Synthetics::Canary S3Encryption<a name="aws-properties-synthetics-canary-s3encryption"></a>

A structure that contains the configuration of the encryption\-at\-rest settings for artifacts that the canary uploads to Amazon S3\. Artifact encryption functionality is available only for canaries that use Synthetics runtime version syn\-nodejs\-puppeteer\-3\.3 or later\. For more information, see [Encrypting canary artifacts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_artifact_encryption.html)\.

## Syntax<a name="aws-properties-synthetics-canary-s3encryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-s3encryption-syntax.json"></a>

```
{
  "[EncryptionMode](#cfn-synthetics-canary-s3encryption-encryptionmode)" : String,
  "[KmsKeyArn](#cfn-synthetics-canary-s3encryption-kmskeyarn)" : String
}
```

### YAML<a name="aws-properties-synthetics-canary-s3encryption-syntax.yaml"></a>

```
  [EncryptionMode](#cfn-synthetics-canary-s3encryption-encryptionmode): String
  [KmsKeyArn](#cfn-synthetics-canary-s3encryption-kmskeyarn): String
```

## Properties<a name="aws-properties-synthetics-canary-s3encryption-properties"></a>

`EncryptionMode`  <a name="cfn-synthetics-canary-s3encryption-encryptionmode"></a>
The encryption method to use for artifacts created by this canary\. Specify `SSE_S3` to use server\-side encryption \(SSE\) with an Amazon S3\-managed key\. Specify `SSE-KMS` to use server\-side encryption with a customer\-managed AWS KMS key\.  
If you omit this parameter, an AWS\-managed AWS KMS key is used\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-synthetics-canary-s3encryption-kmskeyarn"></a>
The ARN of the customer\-managed AWS KMS key to use, if you specify `SSE-KMS` for `EncryptionMode`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
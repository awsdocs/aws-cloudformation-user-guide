# AWS::Glue::SecurityConfiguration S3Encryption<a name="aws-properties-glue-securityconfiguration-s3encryption"></a>

Specifies how Amazon Simple Storage Service \(Amazon S3\) data should be encrypted\.

## Syntax<a name="aws-properties-glue-securityconfiguration-s3encryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-securityconfiguration-s3encryption-syntax.json"></a>

```
{
  "[KmsKeyArn](#cfn-glue-securityconfiguration-s3encryption-kmskeyarn)" : String,
  "[S3EncryptionMode](#cfn-glue-securityconfiguration-s3encryption-s3encryptionmode)" : String
}
```

### YAML<a name="aws-properties-glue-securityconfiguration-s3encryption-syntax.yaml"></a>

```
  [KmsKeyArn](#cfn-glue-securityconfiguration-s3encryption-kmskeyarn): String
  [S3EncryptionMode](#cfn-glue-securityconfiguration-s3encryption-s3encryptionmode): String
```

## Properties<a name="aws-properties-glue-securityconfiguration-s3encryption-properties"></a>

`KmsKeyArn`  <a name="cfn-glue-securityconfiguration-s3encryption-kmskeyarn"></a>
The Amazon Resource Name \(ARN\) of the KMS key to be used to encrypt the data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3EncryptionMode`  <a name="cfn-glue-securityconfiguration-s3encryption-s3encryptionmode"></a>
The encryption mode to use for Amazon S3 data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
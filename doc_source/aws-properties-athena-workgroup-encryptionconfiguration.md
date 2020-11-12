# AWS::Athena::WorkGroup EncryptionConfiguration<a name="aws-properties-athena-workgroup-encryptionconfiguration"></a>

If query results are encrypted in Amazon S3, indicates the encryption option used \(for example, `SSE-KMS` or `CSE-KMS`\) and key information\.

## Syntax<a name="aws-properties-athena-workgroup-encryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-encryptionconfiguration-syntax.json"></a>

```
{
  "[EncryptionOption](#cfn-athena-workgroup-encryptionconfiguration-encryptionoption)" : String,
  "[KmsKey](#cfn-athena-workgroup-encryptionconfiguration-kmskey)" : String
}
```

### YAML<a name="aws-properties-athena-workgroup-encryptionconfiguration-syntax.yaml"></a>

```
  [EncryptionOption](#cfn-athena-workgroup-encryptionconfiguration-encryptionoption): String
  [KmsKey](#cfn-athena-workgroup-encryptionconfiguration-kmskey): String
```

## Properties<a name="aws-properties-athena-workgroup-encryptionconfiguration-properties"></a>

`EncryptionOption`  <a name="cfn-athena-workgroup-encryptionconfiguration-encryptionoption"></a>
Indicates whether Amazon S3 server\-side encryption with Amazon S3\-managed keys \(`SSE-S3`\), server\-side encryption with KMS\-managed keys \(`SSE-KMS`\), or client\-side encryption with KMS\-managed keys \(CSE\-KMS\) is used\.  
If a query runs in a workgroup and the workgroup overrides client\-side settings, then the workgroup's setting for encryption is used\. It specifies whether query results must be encrypted, for all queries that run in this workgroup\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `CSE_KMS | SSE_KMS | SSE_S3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKey`  <a name="cfn-athena-workgroup-encryptionconfiguration-kmskey"></a>
For `SSE-KMS` and `CSE-KMS`, this is the KMS key ARN or ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
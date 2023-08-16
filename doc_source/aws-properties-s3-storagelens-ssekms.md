# AWS::S3::StorageLens SSEKMS<a name="aws-properties-s3-storagelens-ssekms"></a>

Specifies the use of server\-side encryption using an AWS Key Management Service key \(SSE\-KMS\) to encrypt the delivered S3 Storage Lens metrics export file\.

## Syntax<a name="aws-properties-s3-storagelens-ssekms-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-ssekms-syntax.json"></a>

```
{
  "[KeyId](#cfn-s3-storagelens-ssekms-keyid)" : String
}
```

### YAML<a name="aws-properties-s3-storagelens-ssekms-syntax.yaml"></a>

```
  [KeyId](#cfn-s3-storagelens-ssekms-keyid): String
```

## Properties<a name="aws-properties-s3-storagelens-ssekms-properties"></a>

`KeyId`  <a name="cfn-s3-storagelens-ssekms-keyid"></a>
Specifies the Amazon Resource Name \(ARN\) of the customer managed AWS KMS key to use for encrypting the S3 Storage Lens metrics export file\. Amazon S3 only supports symmetric encryption keys\. For more information, see [Special\-purpose keys](https://docs.aws.amazon.com/kms/latest/developerguide/key-types.html) in the *AWS Key Management Service Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
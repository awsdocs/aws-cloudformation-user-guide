# Amazon S3 Bucket SseKmsEncryptedObjects<a name="aws-properties-s3-bucket-ssekmsencryptedobjects"></a>

<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-description"></a>The `SseKmsEncryptedObjects` property type specifies the status of whether Amazon S3 replicates objects created with server\-side encryption using an AWS KMS\-managed key\.

<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-inheritance"></a>`SseKmsEncryptedObjects` is a property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource\.

## Syntax<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-syntax.json"></a>

```
{
  "[Status](#cfn-s3-bucket-ssekmsencryptedobjects-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-syntax.yaml"></a>

```
[Status](#cfn-s3-bucket-ssekmsencryptedobjects-status): String
```

## Properties<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-properties"></a>

`Status`  <a name="cfn-s3-bucket-ssekmsencryptedobjects-status"></a>
Specifies whether Amazon S3 replicates objects created with server\-side encryption using an AWS KMS\-managed key\. Valid values include `Enabled` and `Disabled`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
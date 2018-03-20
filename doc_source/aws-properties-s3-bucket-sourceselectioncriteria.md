# Amazon S3 Bucket SourceSelectionCriteria<a name="aws-properties-s3-bucket-sourceselectioncriteria"></a>

<a name="aws-properties-s3-bucket-sourceselectioncriteria-description"></a>The `SourceSelectionCriteria` property type specifies additional filters in identifying source objects that you want to replicate\.

Currently, Amazon S3 supports only the filter that you can specify for objects created with server\-side encryption using an AWS KMS\-managed key\. That is, you can choose to enable or disable replication of these objects\.

<a name="aws-properties-s3-bucket-sourceselectioncriteria-inheritance"></a> `SourceSelectionCriteria` is a property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource\.

## Syntax<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax.json"></a>

```
{
  "[SseKmsEncryptedObjects](#cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects)" : [*SseKmsEncryptedObjects*](aws-properties-s3-bucket-ssekmsencryptedobjects.md)
}
```

### YAML<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax.yaml"></a>

```
[SseKmsEncryptedObjects](#cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects): [*SseKmsEncryptedObjects*](aws-properties-s3-bucket-ssekmsencryptedobjects.md)
```

## Properties<a name="aws-properties-s3-bucket-sourceselectioncriteria-properties"></a>

`SseKmsEncryptedObjects`  <a name="cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects"></a>
Contains the status of whether Amazon S3 replicates objects created with server\-side encryption using an AWS KMS\-managed key\.  
 *Required*: Yes  
 *Type*: [Amazon S3 Bucket SseKmsEncryptedObjects](aws-properties-s3-bucket-ssekmsencryptedobjects.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
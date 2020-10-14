# AWS::S3::Bucket SourceSelectionCriteria<a name="aws-properties-s3-bucket-sourceselectioncriteria"></a>

A container that describes additional filters for identifying the source objects that you want to replicate\. You can choose to enable or disable the replication of these objects\. Currently, Amazon S3 supports only the filter that you can specify for objects created with server\-side encryption using a customer master key \(CMK\) stored in AWS Key Management Service \(SSE\-KMS\)\.

## Syntax<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax.json"></a>

```
{
  "[SseKmsEncryptedObjects](#cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects)" : SseKmsEncryptedObjects
}
```

### YAML<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax.yaml"></a>

```
  [SseKmsEncryptedObjects](#cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects): 
    SseKmsEncryptedObjects
```

## Properties<a name="aws-properties-s3-bucket-sourceselectioncriteria-properties"></a>

`SseKmsEncryptedObjects`  <a name="cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects"></a>
 A container for filter information for the selection of Amazon S3 objects encrypted with AWS KMS\. If you include `SourceSelectionCriteria` in the replication configuration, this element is required\.   
*Required*: Yes  
*Type*: [SseKmsEncryptedObjects](aws-properties-s3-bucket-ssekmsencryptedobjects.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::S3::Bucket SourceSelectionCriteria<a name="aws-properties-s3-bucket-sourceselectioncriteria"></a>

A container that describes additional filters for identifying the source objects that you want to replicate\. You can choose to enable or disable the replication of these objects\.

## Syntax<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax.json"></a>

```
{
  "[ReplicaModifications](#cfn-s3-bucket-sourceselectioncriteria-replicamodifications)" : ReplicaModifications,
  "[SseKmsEncryptedObjects](#cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects)" : SseKmsEncryptedObjects
}
```

### YAML<a name="aws-properties-s3-bucket-sourceselectioncriteria-syntax.yaml"></a>

```
  [ReplicaModifications](#cfn-s3-bucket-sourceselectioncriteria-replicamodifications): 
    ReplicaModifications
  [SseKmsEncryptedObjects](#cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects): 
    SseKmsEncryptedObjects
```

## Properties<a name="aws-properties-s3-bucket-sourceselectioncriteria-properties"></a>

`ReplicaModifications`  <a name="cfn-s3-bucket-sourceselectioncriteria-replicamodifications"></a>
A filter that you can specify for selection for modifications on replicas\.   
*Required*: No  
*Type*: [ReplicaModifications](aws-properties-s3-bucket-replicamodifications.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SseKmsEncryptedObjects`  <a name="cfn-s3-bucket-sourceselectioncriteria-ssekmsencryptedobjects"></a>
 A container for filter information for the selection of Amazon S3 objects encrypted with AWS KMS\.  
*Required*: No  
*Type*: [SseKmsEncryptedObjects](aws-properties-s3-bucket-ssekmsencryptedobjects.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
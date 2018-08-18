# Amazon S3 Bucket ReplicationRule<a name="aws-properties-s3-bucket-replicationconfiguration-rules"></a>

The `ReplicationRule` property type specifies which Amazon Simple Storage Service \(Amazon S3\) objects to replicate and where to store them\. The `Rules` subproperty of the [Amazon S3 Bucket ReplicationConfiguration](aws-properties-s3-bucket-replicationconfiguration.md) property contains a list of `ReplicationRule` property types\.

## Syntax<a name="w3ab2c21c14e1758b5"></a>

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.json"></a>

```
{
  "[Destination](#cfn-s3-bucket-replicationconfiguration-rules-destination)" : [*ReplicationDestination*](aws-properties-s3-bucket-replicationconfiguration-rules-destination.md),
  "[Id](#cfn-s3-bucket-replicationconfiguration-rules-id)" : String,
  "[Prefix](#cfn-s3-bucket-replicationconfiguration-rules-prefix)" : String,
  "[SourceSelectionCriteria](#cfn-s3-bucket-replicationrule-sourceselectioncriteria)" : [*SourceSelectionCriteria*](aws-properties-s3-bucket-sourceselectioncriteria.md),              
  "[Status](#cfn-s3-bucket-replicationconfiguration-rules-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.yaml"></a>

```
[Destination](#cfn-s3-bucket-replicationconfiguration-rules-destination): 
  [*ReplicationDestination*](aws-properties-s3-bucket-replicationconfiguration-rules-destination.md)
[Id](#cfn-s3-bucket-replicationconfiguration-rules-id): String
[Prefix](#cfn-s3-bucket-replicationconfiguration-rules-prefix): String
[SourceSelectionCriteria](#cfn-s3-bucket-replicationrule-sourceselectioncriteria): [*SourceSelectionCriteria*](aws-properties-s3-bucket-sourceselectioncriteria.md);
[Status](#cfn-s3-bucket-replicationconfiguration-rules-status): String
```

## Properties<a name="w3ab2c21c14e1758b7"></a>

`Destination`  <a name="cfn-s3-bucket-replicationconfiguration-rules-destination"></a>
Defines the destination where Amazon S3 stores replicated objects\.  
*Required*: Yes  
*Type*: [Amazon S3 Bucket ReplicationDestination](aws-properties-s3-bucket-replicationconfiguration-rules-destination.md)

`Id`  <a name="cfn-s3-bucket-replicationconfiguration-rules-id"></a>
A unique identifier for the rule\. If you don't specify a value, AWS CloudFormation generates a random ID\.  
*Required*: No  
*Type*: String

`Prefix`  <a name="cfn-s3-bucket-replicationconfiguration-rules-prefix"></a>
An object prefix\. This rule applies to all Amazon S3 objects with this prefix\. To specify all objects in an S3 bucket, specify an empty string\.  
*Required*: Yes  
*Type*: String

`SourceSelectionCriteria`  <a name="cfn-s3-bucket-replicationrule-sourceselectioncriteria"></a>
Specifies additional filters in identifying source objects that you want to replicate\.  
Currently, Amazon S3 supports only the filter that you can specify for objects created with server\-side encryption using an AWS KMS\-managed key\. That is, you can choose to enable or disable replication of these objects\.  
*Required*: No  
*Type*: [Amazon S3 Bucket SourceSelectionCriteria](aws-properties-s3-bucket-sourceselectioncriteria.md)

`Status`  <a name="cfn-s3-bucket-replicationconfiguration-rules-status"></a>
Whether the rule is enabled\. For valid values, see the `Status` element of the [PUT Bucket replication](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTreplication.html) action in the *Amazon Simple Storage Service API Reference*\.  
*Required*: Yes  
*Type*: String
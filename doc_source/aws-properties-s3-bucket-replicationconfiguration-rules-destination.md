# Amazon S3 Bucket ReplicationDestination<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination"></a>

`Destination` is a property of the [Amazon S3 Bucket ReplicationRule](aws-properties-s3-bucket-replicationconfiguration-rules.md) property that specifies which Amazon Simple Storage Service \(Amazon S3\) bucket to store replicated objects and their storage class\.

## Syntax<a name="w3ab2c21c14e1754b5"></a>

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination-syntax.json"></a>

```
{
  "[AccessControlTranslation](#cfn-s3-bucket-replicationdestination-accesscontroltranslation)" : [*AccessControlTranslation*](aws-properties-s3-bucket-accesscontroltranslation.md),
  "[Account](#cfn-s3-bucket-replicationdestination-account)" : String,                
  "[Bucket](#cfn-s3-bucket-replicationconfiguration-rules-destination-bucket)" : String,
  "[EncryptionConfiguration](#cfn-s3-bucket-replicationdestination-encryptionconfiguration)" : [*EncryptionConfiguration*](aws-properties-s3-bucket-encryptionconfiguration.md),
  "[StorageClass](#cfn-s3-bucket-replicationconfiguration-rules-destination-storageclass)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination-syntax.yaml"></a>

```
[AccessControlTranslation](#cfn-s3-bucket-replicationdestination-accesscontroltranslation): [*AccessControlTranslation*](aws-properties-s3-bucket-accesscontroltranslation.md)
[Account](#cfn-s3-bucket-replicationdestination-account): String
[Bucket](#cfn-s3-bucket-replicationconfiguration-rules-destination-bucket): String
[EncryptionConfiguration](#cfn-s3-bucket-replicationdestination-encryptionconfiguration): [*EncryptionConfiguration*](aws-properties-s3-bucket-encryptionconfiguration.md)
[StorageClass](#cfn-s3-bucket-replicationconfiguration-rules-destination-storageclass): String
```

## Properties<a name="w3ab2c21c14e1754b7"></a>

`AccessControlTranslation`  <a name="cfn-s3-bucket-replicationdestination-accesscontroltranslation"></a>
Specify this only in a cross\-account scenario \(where source and destination bucket owners are not the same\), and you want to change replica ownership to the AWS account that owns the destination bucket\. If this is not specified in the replication configuration, the replicas are owned by same AWS account that owns the source object\.  
*Required*: No  
Type: [Amazon S3 Bucket AccessControlTranslation](aws-properties-s3-bucket-accesscontroltranslation.md)

`Account`  <a name="cfn-s3-bucket-replicationdestination-account"></a>
Destination bucket owner account ID\. In a cross\-account scenario, if you direct Amazon S3 to change replica ownership to the AWS account that owns the destination bucket by specifying the `AccessControlTranslation` property, this is the account ID of the destination bucket owner\. For more information, see [Cross\-Region Replication Additional Configuration: Change Replica Owner](http://docs.aws.amazon.com/AmazonS3/latest/dev/crr-change-owner.html) in the *Amazon Simple Storage Service Developer Guide*\.  
Conditional: If you specify the `AccessControlTranslation` property, the `Account` property is required\.  
*Required*: No  
*Type*: String

`Bucket`  <a name="cfn-s3-bucket-replicationconfiguration-rules-destination-bucket"></a>
The Amazon resource name \(ARN\) of an S3 bucket where Amazon S3 stores replicated objects\. This destination bucket must be in a different region than your source bucket\.  
If you have multiple rules in your replication configuration, specify the same destination bucket for all of the rules\.  
*Required*: Yes  
*Type*: String

`EncryptionConfiguration`  <a name="cfn-s3-bucket-replicationdestination-encryptionconfiguration"></a>
Specifies encryption\-related information\.  
*Required*: No  
Type: [Amazon S3 Bucket EncryptionConfiguration](aws-properties-s3-bucket-encryptionconfiguration.md)

`StorageClass`  <a name="cfn-s3-bucket-replicationconfiguration-rules-destination-storageclass"></a>
The storage class to use when replicating objects, such as standard or reduced redundancy\. By default, Amazon S3 uses the storage class of the source object to create object replica\. For valid values, see the `StorageClass` element of the [PUT Bucket replication](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTreplication.html) action in the *Amazon Simple Storage Service API Reference*\.  
*Required*: No  
*Type*: String
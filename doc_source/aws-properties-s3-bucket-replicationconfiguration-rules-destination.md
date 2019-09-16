# AWS::S3::Bucket ReplicationDestination<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination"></a>

Specifies which Amazon S3 bucket to store replicated objects in and their storage class\.

## Syntax<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination-syntax.json"></a>

```
{
  "[AccessControlTranslation](#cfn-s3-bucket-replicationdestination-accesscontroltranslation)" : [AccessControlTranslation](aws-properties-s3-bucket-accesscontroltranslation.md),
  "[Account](#cfn-s3-bucket-replicationdestination-account)" : String,
  "[Bucket](#cfn-s3-bucket-replicationconfiguration-rules-destination-bucket)" : String,
  "[EncryptionConfiguration](#cfn-s3-bucket-replicationdestination-encryptionconfiguration)" : [EncryptionConfiguration](aws-properties-s3-bucket-encryptionconfiguration.md),
  "[StorageClass](#cfn-s3-bucket-replicationconfiguration-rules-destination-storageclass)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination-syntax.yaml"></a>

```
  [AccessControlTranslation](#cfn-s3-bucket-replicationdestination-accesscontroltranslation): 
    [AccessControlTranslation](aws-properties-s3-bucket-accesscontroltranslation.md)
  [Account](#cfn-s3-bucket-replicationdestination-account): String
  [Bucket](#cfn-s3-bucket-replicationconfiguration-rules-destination-bucket): String
  [EncryptionConfiguration](#cfn-s3-bucket-replicationdestination-encryptionconfiguration): 
    [EncryptionConfiguration](aws-properties-s3-bucket-encryptionconfiguration.md)
  [StorageClass](#cfn-s3-bucket-replicationconfiguration-rules-destination-storageclass): String
```

## Properties<a name="aws-properties-s3-bucket-replicationconfiguration-rules-destination-properties"></a>

`AccessControlTranslation`  <a name="cfn-s3-bucket-replicationdestination-accesscontroltranslation"></a>
Specify this only in a cross\-account scenario \(where source and destination bucket owners are not the same\), and you want to change replica ownership to the AWS account that owns the destination bucket\. If this is not specified in the replication configuration, the replicas are owned by same AWS account that owns the source object\.  
*Required*: No  
*Type*: [AccessControlTranslation](aws-properties-s3-bucket-accesscontroltranslation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Account`  <a name="cfn-s3-bucket-replicationdestination-account"></a>
Destination bucket owner account ID\. In a cross\-account scenario, if you direct Amazon S3 to change replica ownership to the AWS account that owns the destination bucket by specifying the `AccessControlTranslation` property, this is the account ID of the destination bucket owner\. For more information, see [Cross\-Region Replication Additional Configuration: Change Replica Owner](https://docs.aws.amazon.com/AmazonS3/latest/dev/crr-change-owner.html) in the *Amazon Simple Storage Service Developer Guide*\.  
If you specify the `AccessControlTranslation` property, the `Account` property is required\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Bucket`  <a name="cfn-s3-bucket-replicationconfiguration-rules-destination-bucket"></a>
 The Amazon Resource Name \(ARN\) of the bucket where you want Amazon S3 to store replicas of the object identified by the rule\.  
A replication configuration can replicate objects to only one destination bucket\. If there are multiple rules in your replication configuration, all rules must specify the same destination bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionConfiguration`  <a name="cfn-s3-bucket-replicationdestination-encryptionconfiguration"></a>
Specifies encryption\-related information\.  
*Required*: No  
*Type*: [EncryptionConfiguration](aws-properties-s3-bucket-encryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageClass`  <a name="cfn-s3-bucket-replicationconfiguration-rules-destination-storageclass"></a>
 The storage class to use when replicating objects, such as standard or reduced redundancy\. By default, Amazon S3 uses the storage class of the source object to create the object replica\.   
For valid values, see the `StorageClass` element of the [PUT Bucket replication](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTreplication.html) action in the *Amazon Simple Storage Service API Reference*\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `DEEP_ARCHIVE | GLACIER | INTELLIGENT_TIERING | ONEZONE_IA | REDUCED_REDUNDANCY | STANDARD | STANDARD_IA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
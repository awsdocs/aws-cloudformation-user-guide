# Amazon S3 Bucket ReplicationConfiguration<a name="aws-properties-s3-bucket-replicationconfiguration"></a>

`ReplicationConfiguration` is a property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource that specifies replication rules and the AWS Identity and Access Management \(IAM\) role Amazon Simple Storage Service \(Amazon S3\) uses to replicate objects\.

## Syntax<a name="w3ab2c21c14e1752b5"></a>

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-syntax.json"></a>

```
{
  "[Role](#cfn-s3-bucket-replicationconfiguration-role)" : String,
  "[Rules](#cfn-s3-bucket-replicationconfiguration-rules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-syntax.yaml"></a>

```
[Role](#cfn-s3-bucket-replicationconfiguration-role): String
[Rules](#cfn-s3-bucket-replicationconfiguration-rules):
  - Rule
```

## Properties<a name="w3ab2c21c14e1752b7"></a>

`Role`  <a name="cfn-s3-bucket-replicationconfiguration-role"></a>
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that Amazon S3 assumes when replicating objects\. For more information, see [How to Set Up Cross\-Region Replication](http://docs.aws.amazon.com/AmazonS3/latest/dev/crr-how-setup.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: String

`Rules`  <a name="cfn-s3-bucket-replicationconfiguration-rules"></a>
A replication rule that specifies which objects to replicate and where they are stored\.  
*Required*: Yes  
*Type*: List of [Amazon S3 Bucket ReplicationRule](aws-properties-s3-bucket-replicationconfiguration-rules.md)
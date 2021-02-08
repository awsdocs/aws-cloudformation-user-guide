# AWS::S3::Bucket ReplicationConfiguration<a name="aws-properties-s3-bucket-replicationconfiguration"></a>

A container for replication rules\. You can add up to 1,000 rules\. The maximum size of a replication configuration is 2 MB\.

## Syntax<a name="aws-properties-s3-bucket-replicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-syntax.json"></a>

```
{
  "[Role](#cfn-s3-bucket-replicationconfiguration-role)" : String,
  "[Rules](#cfn-s3-bucket-replicationconfiguration-rules)" : [ ReplicationRule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-syntax.yaml"></a>

```
  [Role](#cfn-s3-bucket-replicationconfiguration-role): String
  [Rules](#cfn-s3-bucket-replicationconfiguration-rules): 
    - ReplicationRule
```

## Properties<a name="aws-properties-s3-bucket-replicationconfiguration-properties"></a>

`Role`  <a name="cfn-s3-bucket-replicationconfiguration-role"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that Amazon S3 assumes when replicating objects\. For more information, see [How to Set Up Replication](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-how-setup.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rules`  <a name="cfn-s3-bucket-replicationconfiguration-rules"></a>
A container for one or more replication rules\. A replication configuration must have at least one rule and can contain a maximum of 1,000 rules\.   
*Required*: Yes  
*Type*: List of [ReplicationRule](aws-properties-s3-bucket-replicationconfiguration-rules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-replicationconfiguration--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)


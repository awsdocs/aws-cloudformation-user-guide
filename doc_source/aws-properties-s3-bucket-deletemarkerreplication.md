# AWS::S3::Bucket DeleteMarkerReplication<a name="aws-properties-s3-bucket-deletemarkerreplication"></a>

Specifies whether Amazon S3 replicates the delete markers\. If you specify a `Filter`, you must specify this element\. However, in the latest version of replication configuration \(when `Filter` is specified\), Amazon S3 doesn't replicate delete markers\. Therefore, the `DeleteMarkerReplication` element can contain only <Status>Disabled</Status>\. For an example configuration, see [Basic Rule Configuration](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-config-min-rule-config)\. 

**Note**  
 If you don't specify the `Filter` element, Amazon S3 assumes that the replication configuration is the earlier version, V1\. In the earlier version, Amazon S3 handled replication of delete markers differently\. For more information, see [Backward Compatibility](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-backward-compat-considerations)\.

## Syntax<a name="aws-properties-s3-bucket-deletemarkerreplication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-deletemarkerreplication-syntax.json"></a>

```
{
  "[Status](#cfn-s3-bucket-deletemarkerreplication-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-deletemarkerreplication-syntax.yaml"></a>

```
  [Status](#cfn-s3-bucket-deletemarkerreplication-status): String
```

## Properties<a name="aws-properties-s3-bucket-deletemarkerreplication-properties"></a>

`Status`  <a name="cfn-s3-bucket-deletemarkerreplication-status"></a>
Indicates whether to replicate delete markers\.  
 In the current implementation, Amazon S3 doesn't replicate the delete markers\. The status must be `Disabled`\. 
*Required*: No  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
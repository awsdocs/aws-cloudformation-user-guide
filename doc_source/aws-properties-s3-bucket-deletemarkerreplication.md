# AWS::S3::Bucket DeleteMarkerReplication<a name="aws-properties-s3-bucket-deletemarkerreplication"></a>

Specifies whether Amazon S3 replicates delete markers\. If you specify a `Filter` in your replication configuration, you must also include a `DeleteMarkerReplication` element\. If your `Filter` includes a `Tag` element, the `DeleteMarkerReplication` `Status` must be set to Disabled, because Amazon S3 does not support replicating delete markers for tag\-based rules\. For an example configuration, see [Basic Rule Configuration](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-config-min-rule-config)\. 

For more information about delete marker replication, see [Basic Rule Configuration](https://docs.aws.amazon.com/AmazonS3/latest/dev/delete-marker-replication.html)\. 

**Note**  
If you are using an earlier version of the replication configuration, Amazon S3 handles replication of delete markers differently\. For more information, see [Backward Compatibility](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-backward-compat-considerations)\.

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
Indicates whether to replicate delete markers\.
*Required*: No  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
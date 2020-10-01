# AWS::S3::Bucket ReplicationRule<a name="aws-properties-s3-bucket-replicationconfiguration-rules"></a>

Specifies which Amazon S3 objects to replicate and where to store the replicas\.

## Syntax<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.json"></a>

```
{
  "[DeleteMarkerReplication](#cfn-s3-bucket-replicationrule-deletemarkerreplication)" : DeleteMarkerReplication,
  "[Destination](#cfn-s3-bucket-replicationconfiguration-rules-destination)" : ReplicationDestination,
  "[Filter](#cfn-s3-bucket-replicationrule-filter)" : ReplicationRuleFilter,
  "[Id](#cfn-s3-bucket-replicationconfiguration-rules-id)" : String,
  "[Prefix](#cfn-s3-bucket-replicationconfiguration-rules-prefix)" : String,
  "[Priority](#cfn-s3-bucket-replicationrule-priority)" : Integer,
  "[SourceSelectionCriteria](#cfn-s3-bucket-replicationrule-sourceselectioncriteria)" : SourceSelectionCriteria,
  "[Status](#cfn-s3-bucket-replicationconfiguration-rules-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.yaml"></a>

```
  [DeleteMarkerReplication](#cfn-s3-bucket-replicationrule-deletemarkerreplication): 
    DeleteMarkerReplication
  [Destination](#cfn-s3-bucket-replicationconfiguration-rules-destination): 
    ReplicationDestination
  [Filter](#cfn-s3-bucket-replicationrule-filter): 
    ReplicationRuleFilter
  [Id](#cfn-s3-bucket-replicationconfiguration-rules-id): String
  [Prefix](#cfn-s3-bucket-replicationconfiguration-rules-prefix): String
  [Priority](#cfn-s3-bucket-replicationrule-priority): Integer
  [SourceSelectionCriteria](#cfn-s3-bucket-replicationrule-sourceselectioncriteria): 
    SourceSelectionCriteria
  [Status](#cfn-s3-bucket-replicationconfiguration-rules-status): String
```

## Properties<a name="aws-properties-s3-bucket-replicationconfiguration-rules-properties"></a>

`DeleteMarkerReplication`  <a name="cfn-s3-bucket-replicationrule-deletemarkerreplication"></a>
Specifies whether Amazon S3 replicates the delete markers\. If you specify a `Filter`, you must specify this element\. However, in the latest version of replication configuration \(when `Filter` is specified\), Amazon S3 doesn't replicate delete markers\. Therefore, the `DeleteMarkerReplication` element can contain only <Status>Disabled</Status>\. For an example configuration, see [Basic Rule Configuration](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-config-min-rule-config)\.   
 If you don't specify the `Filter` element, Amazon S3 assumes that the replication configuration is the earlier version, V1\. In the earlier version, Amazon S3 handled replication of delete markers differently\. For more information, see [Backward Compatibility](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-backward-compat-considerations)\.
*Required*: No  
*Type*: [DeleteMarkerReplication](aws-properties-s3-bucket-deletemarkerreplication.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-s3-bucket-replicationconfiguration-rules-destination"></a>
A container for information about the replication destination and its configurations including enabling the S3 Replication Time Control \(S3 RTC\)\.  
*Required*: Yes  
*Type*: [ReplicationDestination](aws-properties-s3-bucket-replicationconfiguration-rules-destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-s3-bucket-replicationrule-filter"></a>
A filter that identifies the subset of objects to which the replication rule applies\. A `Filter` must specify exactly one `Prefix`, `TagFilter`, or an `And` child element\.  
*Required*: No  
*Type*: [ReplicationRuleFilter](aws-properties-s3-bucket-replicationrulefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3-bucket-replicationconfiguration-rules-id"></a>
A unique identifier for the rule\. The maximum value is 255 characters\. If you don't specify a value, AWS CloudFormation generates a random ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-replicationconfiguration-rules-prefix"></a>
An object key name prefix that identifies the object or objects to which the rule applies\. The maximum prefix length is 1,024 characters\. To include all objects in a bucket, specify an empty string\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-s3-bucket-replicationrule-priority"></a>
The priority associated with the rule\. If you specify multiple rules in a replication configuration, Amazon S3 prioritizes the rules to prevent conflicts when filtering\. If two or more rules identify the same object based on a specified filter, the rule with higher priority takes precedence\. For example:  
+ Same object quality prefix\-based filter criteria if prefixes you specified in multiple rules overlap 
+ Same object qualify tag\-based filter criteria specified in multiple rules
For more information, see [Replication](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSelectionCriteria`  <a name="cfn-s3-bucket-replicationrule-sourceselectioncriteria"></a>
A container that describes additional filters for identifying the source objects that you want to replicate\. You can choose to enable or disable the replication of these objects\. Currently, Amazon S3 supports only the filter that you can specify for objects created with server\-side encryption using a customer master key \(CMK\) stored in AWS Key Management Service \(SSE\-KMS\)\.  
*Required*: No  
*Type*: [SourceSelectionCriteria](aws-properties-s3-bucket-sourceselectioncriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-s3-bucket-replicationconfiguration-rules-status"></a>
Specifies whether the rule is enabled\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
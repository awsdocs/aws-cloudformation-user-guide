# AWS::S3::Bucket ReplicationTime<a name="aws-properties-s3-bucket-replicationtime"></a>

 A container specifying S3 Replication Time Control \(S3 RTC\) related information, including whether S3 RTC is enabled and the time when all objects and operations on objects must be replicated\. Must be specified together with a `Metrics` block\. 

## Syntax<a name="aws-properties-s3-bucket-replicationtime-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationtime-syntax.json"></a>

```
{
  "[Status](#cfn-s3-bucket-replicationtime-status)" : String,
  "[Time](#cfn-s3-bucket-replicationtime-time)" : ReplicationTimeValue
}
```

### YAML<a name="aws-properties-s3-bucket-replicationtime-syntax.yaml"></a>

```
  [Status](#cfn-s3-bucket-replicationtime-status): String
  [Time](#cfn-s3-bucket-replicationtime-time): 
    ReplicationTimeValue
```

## Properties<a name="aws-properties-s3-bucket-replicationtime-properties"></a>

`Status`  <a name="cfn-s3-bucket-replicationtime-status"></a>
 Specifies whether the replication time is enabled\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-s3-bucket-replicationtime-time"></a>
 A container specifying the time by which replication should be complete for all objects and operations on objects\.   
*Required*: Yes  
*Type*: [ReplicationTimeValue](aws-properties-s3-bucket-replicationtimevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
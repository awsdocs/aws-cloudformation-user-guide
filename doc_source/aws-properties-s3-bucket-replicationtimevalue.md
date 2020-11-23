# AWS::S3::Bucket ReplicationTimeValue<a name="aws-properties-s3-bucket-replicationtimevalue"></a>

 A container specifying the time value for S3 Replication Time Control \(S3 RTC\) and replication metrics `EventThreshold`\. 

## Syntax<a name="aws-properties-s3-bucket-replicationtimevalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationtimevalue-syntax.json"></a>

```
{
  "[Minutes](#cfn-s3-bucket-replicationtimevalue-minutes)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-replicationtimevalue-syntax.yaml"></a>

```
  [Minutes](#cfn-s3-bucket-replicationtimevalue-minutes): Integer
```

## Properties<a name="aws-properties-s3-bucket-replicationtimevalue-properties"></a>

`Minutes`  <a name="cfn-s3-bucket-replicationtimevalue-minutes"></a>
 Contains an integer specifying time in minutes\.   
 Valid values: 15 minutes\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::S3::StorageLens AccountLevel<a name="aws-properties-s3-storagelens-accountlevel"></a>

This resource contains the details of the account\-level metrics for Amazon S3 Storage Lens\.

## Syntax<a name="aws-properties-s3-storagelens-accountlevel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-accountlevel-syntax.json"></a>

```
{
  "[ActivityMetrics](#cfn-s3-storagelens-accountlevel-activitymetrics)" : ActivityMetrics,
  "[BucketLevel](#cfn-s3-storagelens-accountlevel-bucketlevel)" : BucketLevel
}
```

### YAML<a name="aws-properties-s3-storagelens-accountlevel-syntax.yaml"></a>

```
  [ActivityMetrics](#cfn-s3-storagelens-accountlevel-activitymetrics): 
    ActivityMetrics
  [BucketLevel](#cfn-s3-storagelens-accountlevel-bucketlevel): 
    BucketLevel
```

## Properties<a name="aws-properties-s3-storagelens-accountlevel-properties"></a>

`ActivityMetrics`  <a name="cfn-s3-storagelens-accountlevel-activitymetrics"></a>
This property contains the details of the account\-level activity metrics for Amazon S3 Storage Lens\.  
*Required*: No  
*Type*: [ActivityMetrics](aws-properties-s3-storagelens-activitymetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketLevel`  <a name="cfn-s3-storagelens-accountlevel-bucketlevel"></a>
This property contains the details of the account\-level bucket\-level configurations for Amazon S3 Storage Lens\.  
*Required*: Yes  
*Type*: [BucketLevel](aws-properties-s3-storagelens-bucketlevel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
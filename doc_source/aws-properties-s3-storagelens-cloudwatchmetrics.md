# AWS::S3::StorageLens CloudWatchMetrics<a name="aws-properties-s3-storagelens-cloudwatchmetrics"></a>

This resource enables the Amazon CloudWatch publishing option for Amazon S3 Storage Lens metrics\.

For more information, see [ Monitor S3 Storage Lens metrics in CloudWatch](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_view_metrics_cloudwatch.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-storagelens-cloudwatchmetrics-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-cloudwatchmetrics-syntax.json"></a>

```
{
  "[IsEnabled](#cfn-s3-storagelens-cloudwatchmetrics-isenabled)" : Boolean
}
```

### YAML<a name="aws-properties-s3-storagelens-cloudwatchmetrics-syntax.yaml"></a>

```
  [IsEnabled](#cfn-s3-storagelens-cloudwatchmetrics-isenabled): Boolean
```

## Properties<a name="aws-properties-s3-storagelens-cloudwatchmetrics-properties"></a>

`IsEnabled`  <a name="cfn-s3-storagelens-cloudwatchmetrics-isenabled"></a>
This property identifies whether the CloudWatch publishing option for S3 Storage Lens is enabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
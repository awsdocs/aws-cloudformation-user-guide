# AWS::S3::StorageLens DataExport<a name="aws-properties-s3-storagelens-dataexport"></a>

This resource contains the details of the Amazon S3 Storage Lens metrics export\.

## Syntax<a name="aws-properties-s3-storagelens-dataexport-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-dataexport-syntax.json"></a>

```
{
  "[CloudWatchMetrics](#cfn-s3-storagelens-dataexport-cloudwatchmetrics)" : CloudWatchMetrics,
  "[S3BucketDestination](#cfn-s3-storagelens-dataexport-s3bucketdestination)" : S3BucketDestination
}
```

### YAML<a name="aws-properties-s3-storagelens-dataexport-syntax.yaml"></a>

```
  [CloudWatchMetrics](#cfn-s3-storagelens-dataexport-cloudwatchmetrics): 
    CloudWatchMetrics
  [S3BucketDestination](#cfn-s3-storagelens-dataexport-s3bucketdestination): 
    S3BucketDestination
```

## Properties<a name="aws-properties-s3-storagelens-dataexport-properties"></a>

`CloudWatchMetrics`  <a name="cfn-s3-storagelens-dataexport-cloudwatchmetrics"></a>
This property enables the Amazon CloudWatch publishing option for S3 Storage Lens metrics\.  
*Required*: No  
*Type*: [CloudWatchMetrics](aws-properties-s3-storagelens-cloudwatchmetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketDestination`  <a name="cfn-s3-storagelens-dataexport-s3bucketdestination"></a>
This property contains the details of the bucket where the S3 Storage Lens metrics export will be placed\.  
*Required*: No  
*Type*: [S3BucketDestination](aws-properties-s3-storagelens-s3bucketdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
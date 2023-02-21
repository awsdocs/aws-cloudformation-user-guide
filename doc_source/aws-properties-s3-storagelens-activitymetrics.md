# AWS::S3::StorageLens ActivityMetrics<a name="aws-properties-s3-storagelens-activitymetrics"></a>

This resource enables Amazon S3 Storage Lens activity metrics\. Activity metrics show details about how your storage is requested, such as requests \(for example, All requests, Get requests, Put requests\), bytes uploaded or downloaded, and errors\.

For more information, see [ Assessing your storage activity and usage with S3 Storage Lens](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens.html) in the *Amazon S3 User Guide*\. For a complete list of metrics, see [ S3 Storage Lens metrics glossary](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_metrics_glossary.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-storagelens-activitymetrics-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-activitymetrics-syntax.json"></a>

```
{
  "[IsEnabled](#cfn-s3-storagelens-activitymetrics-isenabled)" : Boolean
}
```

### YAML<a name="aws-properties-s3-storagelens-activitymetrics-syntax.yaml"></a>

```
  [IsEnabled](#cfn-s3-storagelens-activitymetrics-isenabled): Boolean
```

## Properties<a name="aws-properties-s3-storagelens-activitymetrics-properties"></a>

`IsEnabled`  <a name="cfn-s3-storagelens-activitymetrics-isenabled"></a>
A property that indicates whether the activity metrics is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
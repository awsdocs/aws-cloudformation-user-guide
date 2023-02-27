# AWS::S3::StorageLens DetailedStatusCodesMetrics<a name="aws-properties-s3-storagelens-detailedstatuscodesmetrics"></a>

This resource enables Amazon S3 Storage Lens detailed status code metrics\. Detailed status code metrics generate metrics for HTTP status codes, such as `200 OK`, `403 Forbidden`, `503 Service Unavailable` and others\. 

For more information, see [ Assessing your storage activity and usage with S3 Storage Lens](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens.html) in the *Amazon S3 User Guide*\. For a complete list of metrics, see [ S3 Storage Lens metrics glossary](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_metrics_glossary.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-storagelens-detailedstatuscodesmetrics-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-detailedstatuscodesmetrics-syntax.json"></a>

```
{
  "[IsEnabled](#cfn-s3-storagelens-detailedstatuscodesmetrics-isenabled)" : Boolean
}
```

### YAML<a name="aws-properties-s3-storagelens-detailedstatuscodesmetrics-syntax.yaml"></a>

```
  [IsEnabled](#cfn-s3-storagelens-detailedstatuscodesmetrics-isenabled): Boolean
```

## Properties<a name="aws-properties-s3-storagelens-detailedstatuscodesmetrics-properties"></a>

`IsEnabled`  <a name="cfn-s3-storagelens-detailedstatuscodesmetrics-isenabled"></a>
Indicates whether detailed status code metrics are enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
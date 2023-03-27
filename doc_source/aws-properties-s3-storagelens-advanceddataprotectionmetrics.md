# AWS::S3::StorageLens AdvancedDataProtectionMetrics<a name="aws-properties-s3-storagelens-advanceddataprotectionmetrics"></a>

This resource enables Amazon S3 Storage Lens advanced data protection metrics\. Advanced data protection metrics provide insights that you can use to perform audits and protect your data, for example replication rule counts within and across Regions\.

For more information, see [ Assessing your storage activity and usage with S3 Storage Lens](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens.html) in the *Amazon S3 User Guide*\. For a complete list of metrics, see [ S3 Storage Lens metrics glossary](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_metrics_glossary.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-storagelens-advanceddataprotectionmetrics-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-advanceddataprotectionmetrics-syntax.json"></a>

```
{
  "[IsEnabled](#cfn-s3-storagelens-advanceddataprotectionmetrics-isenabled)" : Boolean
}
```

### YAML<a name="aws-properties-s3-storagelens-advanceddataprotectionmetrics-syntax.yaml"></a>

```
  [IsEnabled](#cfn-s3-storagelens-advanceddataprotectionmetrics-isenabled): Boolean
```

## Properties<a name="aws-properties-s3-storagelens-advanceddataprotectionmetrics-properties"></a>

`IsEnabled`  <a name="cfn-s3-storagelens-advanceddataprotectionmetrics-isenabled"></a>
Indicates whether advanced data protection metrics are enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
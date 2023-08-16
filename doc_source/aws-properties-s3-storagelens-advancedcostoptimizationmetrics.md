# AWS::S3::StorageLens AdvancedCostOptimizationMetrics<a name="aws-properties-s3-storagelens-advancedcostoptimizationmetrics"></a>

This resource enables Amazon S3 Storage Lens advanced cost optimization metrics\. Advanced cost optimization metrics provide insights that you can use to manage and optimize your storage costs, for example, lifecycle rule counts for transitions, expirations, and incomplete multipart uploads\.

For more information, see [ Assessing your storage activity and usage with S3 Storage Lens](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens.html) in the *Amazon S3 User Guide*\. For a complete list of metrics, see [ S3 Storage Lens metrics glossary](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_metrics_glossary.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-storagelens-advancedcostoptimizationmetrics-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-advancedcostoptimizationmetrics-syntax.json"></a>

```
{
  "[IsEnabled](#cfn-s3-storagelens-advancedcostoptimizationmetrics-isenabled)" : Boolean
}
```

### YAML<a name="aws-properties-s3-storagelens-advancedcostoptimizationmetrics-syntax.yaml"></a>

```
  [IsEnabled](#cfn-s3-storagelens-advancedcostoptimizationmetrics-isenabled): Boolean
```

## Properties<a name="aws-properties-s3-storagelens-advancedcostoptimizationmetrics-properties"></a>

`IsEnabled`  <a name="cfn-s3-storagelens-advancedcostoptimizationmetrics-isenabled"></a>
Indicates whether advanced cost optimization metrics are enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
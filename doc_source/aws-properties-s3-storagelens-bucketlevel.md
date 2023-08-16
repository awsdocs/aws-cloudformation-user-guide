# AWS::S3::StorageLens BucketLevel<a name="aws-properties-s3-storagelens-bucketlevel"></a>

A property for the bucket\-level storage metrics for Amazon S3 Storage Lens\.

## Syntax<a name="aws-properties-s3-storagelens-bucketlevel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-bucketlevel-syntax.json"></a>

```
{
  "[ActivityMetrics](#cfn-s3-storagelens-bucketlevel-activitymetrics)" : ActivityMetrics,
  "[AdvancedCostOptimizationMetrics](#cfn-s3-storagelens-bucketlevel-advancedcostoptimizationmetrics)" : AdvancedCostOptimizationMetrics,
  "[AdvancedDataProtectionMetrics](#cfn-s3-storagelens-bucketlevel-advanceddataprotectionmetrics)" : AdvancedDataProtectionMetrics,
  "[DetailedStatusCodesMetrics](#cfn-s3-storagelens-bucketlevel-detailedstatuscodesmetrics)" : DetailedStatusCodesMetrics,
  "[PrefixLevel](#cfn-s3-storagelens-bucketlevel-prefixlevel)" : PrefixLevel
}
```

### YAML<a name="aws-properties-s3-storagelens-bucketlevel-syntax.yaml"></a>

```
  [ActivityMetrics](#cfn-s3-storagelens-bucketlevel-activitymetrics): 
    ActivityMetrics
  [AdvancedCostOptimizationMetrics](#cfn-s3-storagelens-bucketlevel-advancedcostoptimizationmetrics): 
    AdvancedCostOptimizationMetrics
  [AdvancedDataProtectionMetrics](#cfn-s3-storagelens-bucketlevel-advanceddataprotectionmetrics): 
    AdvancedDataProtectionMetrics
  [DetailedStatusCodesMetrics](#cfn-s3-storagelens-bucketlevel-detailedstatuscodesmetrics): 
    DetailedStatusCodesMetrics
  [PrefixLevel](#cfn-s3-storagelens-bucketlevel-prefixlevel): 
    PrefixLevel
```

## Properties<a name="aws-properties-s3-storagelens-bucketlevel-properties"></a>

`ActivityMetrics`  <a name="cfn-s3-storagelens-bucketlevel-activitymetrics"></a>
A property for bucket\-level activity metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [ActivityMetrics](aws-properties-s3-storagelens-activitymetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdvancedCostOptimizationMetrics`  <a name="cfn-s3-storagelens-bucketlevel-advancedcostoptimizationmetrics"></a>
A property for bucket\-level advanced cost optimization metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [AdvancedCostOptimizationMetrics](aws-properties-s3-storagelens-advancedcostoptimizationmetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdvancedDataProtectionMetrics`  <a name="cfn-s3-storagelens-bucketlevel-advanceddataprotectionmetrics"></a>
A property for bucket\-level advanced data protection metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [AdvancedDataProtectionMetrics](aws-properties-s3-storagelens-advanceddataprotectionmetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetailedStatusCodesMetrics`  <a name="cfn-s3-storagelens-bucketlevel-detailedstatuscodesmetrics"></a>
A property for bucket\-level detailed status code metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [DetailedStatusCodesMetrics](aws-properties-s3-storagelens-detailedstatuscodesmetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrefixLevel`  <a name="cfn-s3-storagelens-bucketlevel-prefixlevel"></a>
A property for bucket\-level prefix\-level storage metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [PrefixLevel](aws-properties-s3-storagelens-prefixlevel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
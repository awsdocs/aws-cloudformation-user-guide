# AWS::S3::StorageLens AccountLevel<a name="aws-properties-s3-storagelens-accountlevel"></a>

This resource contains the details of the account\-level metrics for Amazon S3 Storage Lens\.

## Syntax<a name="aws-properties-s3-storagelens-accountlevel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-accountlevel-syntax.json"></a>

```
{
  "[ActivityMetrics](#cfn-s3-storagelens-accountlevel-activitymetrics)" : ActivityMetrics,
  "[AdvancedCostOptimizationMetrics](#cfn-s3-storagelens-accountlevel-advancedcostoptimizationmetrics)" : AdvancedCostOptimizationMetrics,
  "[AdvancedDataProtectionMetrics](#cfn-s3-storagelens-accountlevel-advanceddataprotectionmetrics)" : AdvancedDataProtectionMetrics,
  "[BucketLevel](#cfn-s3-storagelens-accountlevel-bucketlevel)" : BucketLevel,
  "[DetailedStatusCodesMetrics](#cfn-s3-storagelens-accountlevel-detailedstatuscodesmetrics)" : DetailedStatusCodesMetrics
}
```

### YAML<a name="aws-properties-s3-storagelens-accountlevel-syntax.yaml"></a>

```
  [ActivityMetrics](#cfn-s3-storagelens-accountlevel-activitymetrics): 
    ActivityMetrics
  [AdvancedCostOptimizationMetrics](#cfn-s3-storagelens-accountlevel-advancedcostoptimizationmetrics): 
    AdvancedCostOptimizationMetrics
  [AdvancedDataProtectionMetrics](#cfn-s3-storagelens-accountlevel-advanceddataprotectionmetrics): 
    AdvancedDataProtectionMetrics
  [BucketLevel](#cfn-s3-storagelens-accountlevel-bucketlevel): 
    BucketLevel
  [DetailedStatusCodesMetrics](#cfn-s3-storagelens-accountlevel-detailedstatuscodesmetrics): 
    DetailedStatusCodesMetrics
```

## Properties<a name="aws-properties-s3-storagelens-accountlevel-properties"></a>

`ActivityMetrics`  <a name="cfn-s3-storagelens-accountlevel-activitymetrics"></a>
This property contains the details of account\-level activity metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [ActivityMetrics](aws-properties-s3-storagelens-activitymetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdvancedCostOptimizationMetrics`  <a name="cfn-s3-storagelens-accountlevel-advancedcostoptimizationmetrics"></a>
This property contains the details of account\-level advanced cost optimization metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [AdvancedCostOptimizationMetrics](aws-properties-s3-storagelens-advancedcostoptimizationmetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdvancedDataProtectionMetrics`  <a name="cfn-s3-storagelens-accountlevel-advanceddataprotectionmetrics"></a>
This property contains the details of account\-level advanced data protection metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [AdvancedDataProtectionMetrics](aws-properties-s3-storagelens-advanceddataprotectionmetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketLevel`  <a name="cfn-s3-storagelens-accountlevel-bucketlevel"></a>
This property contains the details of the account\-level bucket\-level configurations for Amazon S3 Storage Lens\.  
*Required*: Yes  
*Type*: [BucketLevel](aws-properties-s3-storagelens-bucketlevel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetailedStatusCodesMetrics`  <a name="cfn-s3-storagelens-accountlevel-detailedstatuscodesmetrics"></a>
This property contains the details of account\-level detailed status code metrics for S3 Storage Lens\.  
*Required*: No  
*Type*: [DetailedStatusCodesMetrics](aws-properties-s3-storagelens-detailedstatuscodesmetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
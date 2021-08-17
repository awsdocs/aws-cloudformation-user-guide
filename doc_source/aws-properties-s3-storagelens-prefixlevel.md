# AWS::S3::StorageLens PrefixLevel<a name="aws-properties-s3-storagelens-prefixlevel"></a>

This resource contains the details of the prefix\-level of the Amazon S3 Storage Lens\.

## Syntax<a name="aws-properties-s3-storagelens-prefixlevel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-prefixlevel-syntax.json"></a>

```
{
  "[StorageMetrics](#cfn-s3-storagelens-prefixlevel-storagemetrics)" : PrefixLevelStorageMetrics
}
```

### YAML<a name="aws-properties-s3-storagelens-prefixlevel-syntax.yaml"></a>

```
  [StorageMetrics](#cfn-s3-storagelens-prefixlevel-storagemetrics): 
    PrefixLevelStorageMetrics
```

## Properties<a name="aws-properties-s3-storagelens-prefixlevel-properties"></a>

`StorageMetrics`  <a name="cfn-s3-storagelens-prefixlevel-storagemetrics"></a>
A property for the prefix\-level storage metrics for Amazon S3 Storage Lens\.  
*Required*: Yes  
*Type*: [PrefixLevelStorageMetrics](aws-properties-s3-storagelens-prefixlevelstoragemetrics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
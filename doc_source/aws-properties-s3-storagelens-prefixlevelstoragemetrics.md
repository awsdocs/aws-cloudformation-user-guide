# AWS::S3::StorageLens PrefixLevelStorageMetrics<a name="aws-properties-s3-storagelens-prefixlevelstoragemetrics"></a>

This resource contains the details of the prefix\-level storage metrics for Amazon S3 Storage Lens\.

## Syntax<a name="aws-properties-s3-storagelens-prefixlevelstoragemetrics-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-prefixlevelstoragemetrics-syntax.json"></a>

```
{
  "[IsEnabled](#cfn-s3-storagelens-prefixlevelstoragemetrics-isenabled)" : Boolean,
  "[SelectionCriteria](#cfn-s3-storagelens-prefixlevelstoragemetrics-selectioncriteria)" : SelectionCriteria
}
```

### YAML<a name="aws-properties-s3-storagelens-prefixlevelstoragemetrics-syntax.yaml"></a>

```
  [IsEnabled](#cfn-s3-storagelens-prefixlevelstoragemetrics-isenabled): Boolean
  [SelectionCriteria](#cfn-s3-storagelens-prefixlevelstoragemetrics-selectioncriteria): 
    SelectionCriteria
```

## Properties<a name="aws-properties-s3-storagelens-prefixlevelstoragemetrics-properties"></a>

`IsEnabled`  <a name="cfn-s3-storagelens-prefixlevelstoragemetrics-isenabled"></a>
This property identifies whether the details of the prefix\-level storage metrics for S3 Storage Lens are enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectionCriteria`  <a name="cfn-s3-storagelens-prefixlevelstoragemetrics-selectioncriteria"></a>
This property identifies whether the details of the prefix\-level storage metrics for S3 Storage Lens are enabled\.  
*Required*: No  
*Type*: [SelectionCriteria](aws-properties-s3-storagelens-selectioncriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
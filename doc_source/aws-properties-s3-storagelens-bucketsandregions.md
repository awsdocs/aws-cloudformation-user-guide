# AWS::S3::StorageLens BucketsAndRegions<a name="aws-properties-s3-storagelens-bucketsandregions"></a>

This resource contains the details of the buckets and Regions for the Amazon S3 Storage Lens configuration\. 

## Syntax<a name="aws-properties-s3-storagelens-bucketsandregions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-bucketsandregions-syntax.json"></a>

```
{
  "[Buckets](#cfn-s3-storagelens-bucketsandregions-buckets)" : [ String, ... ],
  "[Regions](#cfn-s3-storagelens-bucketsandregions-regions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-s3-storagelens-bucketsandregions-syntax.yaml"></a>

```
  [Buckets](#cfn-s3-storagelens-bucketsandregions-buckets): 
    - String
  [Regions](#cfn-s3-storagelens-bucketsandregions-regions): 
    - String
```

## Properties<a name="aws-properties-s3-storagelens-bucketsandregions-properties"></a>

`Buckets`  <a name="cfn-s3-storagelens-bucketsandregions-buckets"></a>
This property contains the details of the buckets for the Amazon S3 Storage Lens configuration\. This should be the bucket Amazon Resource Name\(ARN\)\. For valid values, see [Buckets ARN format here](https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_Include.html#API_control_Include_Contents) in the *Amazon Simple Storage Service API Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regions`  <a name="cfn-s3-storagelens-bucketsandregions-regions"></a>
This property contains the details of the Regions for the S3 Storage Lens configuration\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
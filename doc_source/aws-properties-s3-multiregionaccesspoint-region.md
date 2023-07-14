# AWS::S3::MultiRegionAccessPoint Region<a name="aws-properties-s3-multiregionaccesspoint-region"></a>

A bucket associated with a specific Region when creating Multi\-Region Access Points\.

## Syntax<a name="aws-properties-s3-multiregionaccesspoint-region-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-multiregionaccesspoint-region-syntax.json"></a>

```
{
  "[Bucket](#cfn-s3-multiregionaccesspoint-region-bucket)" : String,
  "[BucketAccountId](#cfn-s3-multiregionaccesspoint-region-bucketaccountid)" : String
}
```

### YAML<a name="aws-properties-s3-multiregionaccesspoint-region-syntax.yaml"></a>

```
  [Bucket](#cfn-s3-multiregionaccesspoint-region-bucket): String
  [BucketAccountId](#cfn-s3-multiregionaccesspoint-region-bucketaccountid): String
```

## Properties<a name="aws-properties-s3-multiregionaccesspoint-region-properties"></a>

`Bucket`  <a name="cfn-s3-multiregionaccesspoint-region-bucket"></a>
The name of the associated bucket for the Region\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketAccountId`  <a name="cfn-s3-multiregionaccesspoint-region-bucketaccountid"></a>
The AWS account ID that owns the Amazon S3 bucket that's associated with this Multi\-Region Access Point\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
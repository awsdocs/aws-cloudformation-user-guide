# AWS::S3::Bucket Destination<a name="aws-properties-s3-bucket-destination"></a>

Specifies information about where to publish analysis or configuration results for an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-bucket-destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-destination-syntax.json"></a>

```
{
  "[BucketAccountId](#cfn-s3-bucket-destination-bucketaccountid)" : String,
  "[BucketArn](#cfn-s3-bucket-destination-bucketarn)" : String,
  "[Format](#cfn-s3-bucket-destination-format)" : String,
  "[Prefix](#cfn-s3-bucket-destination-prefix)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-destination-syntax.yaml"></a>

```
  [BucketAccountId](#cfn-s3-bucket-destination-bucketaccountid): String
  [BucketArn](#cfn-s3-bucket-destination-bucketarn): String
  [Format](#cfn-s3-bucket-destination-format): String
  [Prefix](#cfn-s3-bucket-destination-prefix): String
```

## Properties<a name="aws-properties-s3-bucket-destination-properties"></a>

`BucketAccountId`  <a name="cfn-s3-bucket-destination-bucketaccountid"></a>
The account ID that owns the destination S3 bucket\. If no account ID is provided, the owner is not validated before exporting data\.  
 Although this value is optional, we strongly recommend that you set it to help prevent problems if the destination bucket ownership changes\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketArn`  <a name="cfn-s3-bucket-destination-bucketarn"></a>
The Amazon Resource Name \(ARN\) of the bucket to which data is exported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-s3-bucket-destination-format"></a>
Specifies the file format used when exporting data to Amazon S3\.  
*Allowed values*: `CSV` \| `ORC` \| `Parquet`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-destination-prefix"></a>
The prefix to use when exporting data\. The prefix is prepended to all results\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-destination--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)


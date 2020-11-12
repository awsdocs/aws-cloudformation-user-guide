# AWS::S3::Bucket Tiering<a name="aws-properties-s3-bucket-tiering"></a>

The S3 Intelligent\-Tiering storage class is designed to optimize storage costs by automatically moving data to the most cost\-effective storage access tier, without additional operational overhead\.

## Syntax<a name="aws-properties-s3-bucket-tiering-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-tiering-syntax.json"></a>

```
{
  "[AccessTier](#cfn-s3-bucket-tiering-accesstier)" : String,
  "[Days](#cfn-s3-bucket-tiering-days)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-tiering-syntax.yaml"></a>

```
  [AccessTier](#cfn-s3-bucket-tiering-accesstier): String
  [Days](#cfn-s3-bucket-tiering-days): Integer
```

## Properties<a name="aws-properties-s3-bucket-tiering-properties"></a>

`AccessTier`  <a name="cfn-s3-bucket-tiering-accesstier"></a>
S3 Intelligent\-Tiering access tier\. See [Storage class for automatically optimizing frequently and infrequently accessed objects](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html#sc-dynamic-data-access) for a list of access tiers in the S3 Intelligent\-Tiering storage class\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ARCHIVE_ACCESS | DEEP_ARCHIVE_ACCESS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Days`  <a name="cfn-s3-bucket-tiering-days"></a>
The number of days that you want your archived data to be accessible\. The minimum number of days specified in the restore request must be at least 90 days\. If a smaller value is specifed it will be ignored\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::S3::Bucket VersioningConfiguration<a name="aws-properties-s3-bucket-versioningconfig"></a>

Describes the versioning state of an Amazon S3 bucket\. For more information, see [PUT Bucket versioning](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTVersioningStatus.html) in the *Amazon Simple Storage Service API Reference*\.

## Syntax<a name="aws-properties-s3-bucket-versioningconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-versioningconfig-syntax.json"></a>

```
{
  "[Status](#cfn-s3-bucket-versioningconfig-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-versioningconfig-syntax.yaml"></a>

```
  [Status](#cfn-s3-bucket-versioningconfig-status): String
```

## Properties<a name="aws-properties-s3-bucket-versioningconfig-properties"></a>

`Status`  <a name="cfn-s3-bucket-versioningconfig-status"></a>
The versioning state of the bucket\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Enabled | Suspended`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-versioningconfig--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)


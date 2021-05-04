# AWS::S3Outposts::Bucket AbortIncompleteMultipartUpload<a name="aws-properties-s3outposts-bucket-abortincompletemultipartupload"></a>

Specifies the days since the initiation of an incomplete multipart upload that Amazon S3 on Outposts waits before permanently removing all parts of the upload\. For more information, see [Aborting Incomplete Multipart Uploads Using a Bucket Lifecycle Policy](https://docs.aws.amazon.com/AmazonS3/latest/userguide/mpuoverview.html#mpu-abort-incomplete-mpu-lifecycle-config)\.

## Syntax<a name="aws-properties-s3outposts-bucket-abortincompletemultipartupload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3outposts-bucket-abortincompletemultipartupload-syntax.json"></a>

```
{
  "[DaysAfterInitiation](#cfn-s3outposts-bucket-abortincompletemultipartupload-daysafterinitiation)" : Integer
}
```

### YAML<a name="aws-properties-s3outposts-bucket-abortincompletemultipartupload-syntax.yaml"></a>

```
  [DaysAfterInitiation](#cfn-s3outposts-bucket-abortincompletemultipartupload-daysafterinitiation): Integer
```

## Properties<a name="aws-properties-s3outposts-bucket-abortincompletemultipartupload-properties"></a>

`DaysAfterInitiation`  <a name="cfn-s3outposts-bucket-abortincompletemultipartupload-daysafterinitiation"></a>
Specifies the number of days after initiation that Amazon S3 on Outposts aborts an incomplete multipart upload\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# Amazon S3 Bucket AbortIncompleteMultipartUpload<a name="aws-properties-s3-bucket-abortincompletemultipartupload"></a>

The `AbortIncompleteMultipartUpload` property type creates a lifecycle rule that aborts incomplete multipart uploads to an Amazon S3 bucket\. When Amazon S3 aborts a multipart upload, it deletes all parts associated with the multipart upload\. For more information, see [ Aborting Incomplete Multipart Uploads Using a Bucket Lifecycle Policy](http://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html#mpu-abort-incomplete-mpu-lifecycle-config) in the *Amazon Simple Storage Service Developer Guide*\.

 `AbortIncompleteMultipartUpload` is a property of the [Amazon S3 Bucket Rule](aws-properties-s3-bucket-lifecycleconfig-rule.md) property type\.

## Syntax<a name="aws-properties-s3-bucket-abortincompletemultipartupload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-abortincompletemultipartupload-syntax.json"></a>

```
{
  "[DaysAfterInitiation](#cfn-s3-bucket-abortincompletemultipartupload-daysafterinitiation)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-abortincompletemultipartupload-syntax.yaml"></a>

```
[DaysAfterInitiation](#cfn-s3-bucket-abortincompletemultipartupload-daysafterinitiation): Integer
```

## Properties<a name="aws-properties-s3-bucket-abortincompletemultipartupload-properties"></a>

`DaysAfterInitiation`  <a name="cfn-s3-bucket-abortincompletemultipartupload-daysafterinitiation"></a>
The number of days after the upload is initiated before aborting the upload\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
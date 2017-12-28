# Amazon S3 Bucket VersioningConfiguration<a name="aws-properties-s3-bucket-versioningconfig"></a>

Describes the versioning state of an  AWS::S3::Bucket resource\. For more information, see [PUT Bucket versioning](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTVersioningStatus.html) in the *Amazon Simple Storage Service API Reference*\.

## Syntax<a name="w3ab2c21c14e1545b5"></a>

### JSON<a name="aws-properties-s3-bucket-versioningconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-versioningconfig-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-versioningconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-versioningconfig-status): String
```

## Properties<a name="w3ab2c21c14e1545b7"></a>

`Status`  
The versioning state of an Amazon S3 bucket\. If you enable versioning, you must suspend versioning to disable it\.   
Valid values include `Enabled` and `Suspended`\. The default is `Suspended`\.  
*Required: *Yes  
*Type*: String
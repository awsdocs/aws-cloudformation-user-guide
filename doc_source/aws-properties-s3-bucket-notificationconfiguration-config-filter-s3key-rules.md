# Amazon S3 Bucket FilterRule<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-rules"></a>

`Rules` is a property of the [Amazon S3 Bucket S3KeyFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key.md) property that describes the Amazon Simple Storage Service \(Amazon S3\) object key name to filter on and whether to filter on the suffix or prefix of the key name\.

## Syntax<a name="w3ab2c21c14e1491b5"></a>

### JSON<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-rules-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules-value)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-rules-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules-value): String
```

## Properties<a name="w3ab2c21c14e1491b7"></a>

`Name`  
Whether the filter matches the prefix or suffix of object key names\. For valid values, see the `Name` request element of the [PUT Bucket notification](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTnotification.html) action in the *Amazon Simple Storage Service API Reference*\.  
*Required: *Yes  
*Type*: String

`Value`  
The value that the filter searches for in object key names\.  
*Required: *Yes  
*Type*: String
# Amazon S3 Bucket LoggingConfiguration<a name="aws-properties-s3-bucket-loggingconfig"></a>

Describes where logs are stored and the prefix that Amazon S3 assigns to all log object keys for an  AWS::S3::Bucket resource\. These logs track requests to an Amazon S3 bucket\. For more information, see [PUT Bucket logging](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTlogging.html) in the *Amazon Simple Storage Service API Reference*\.

## Syntax<a name="w3ab2c21c14e1503b5"></a>

### JSON<a name="aws-properties-s3-bucket-loggingconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-loggingconfig-destinationbucketname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-loggingconfig-logfileprefix)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-loggingconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-loggingconfig-destinationbucketname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-loggingconfig-logfileprefix): String
```

## Properties<a name="w3ab2c21c14e1503b7"></a>

`DestinationBucketName`  
The name of an Amazon S3 bucket where Amazon S3 store server access log files\. You can store log files in any bucket that you own\. By default, logs are stored in the bucket where the `LoggingConfiguration` property is defined\.  
*Required: *No  
*Type*: String

`LogFilePrefix`  
A prefix for the all log object keys\. If you store log files from multiple Amazon S3 buckets in a single bucket, you can use a prefix to distinguish which log files came from which bucket\.  
*Required: *No  
*Type*: String
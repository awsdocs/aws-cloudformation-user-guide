# AWS::S3::Bucket LoggingConfiguration<a name="aws-properties-s3-bucket-loggingconfig"></a>

Describes where logs are stored and the prefix that Amazon S3 assigns to all log object keys for a bucket\. For examples and more information, see [PUT Bucket logging](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTlogging.html) in the *Amazon Simple Storage Service API Reference*\.

## Syntax<a name="aws-properties-s3-bucket-loggingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-loggingconfig-syntax.json"></a>

```
{
  "[DestinationBucketName](#cfn-s3-bucket-loggingconfig-destinationbucketname)" : String,
  "[LogFilePrefix](#cfn-s3-bucket-loggingconfig-logfileprefix)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-loggingconfig-syntax.yaml"></a>

```
  [DestinationBucketName](#cfn-s3-bucket-loggingconfig-destinationbucketname): String
  [LogFilePrefix](#cfn-s3-bucket-loggingconfig-logfileprefix): String
```

## Properties<a name="aws-properties-s3-bucket-loggingconfig-properties"></a>

`DestinationBucketName`  <a name="cfn-s3-bucket-loggingconfig-destinationbucketname"></a>
The name of the bucket where Amazon S3 should store server access log files\. You can store log files in any bucket that you own\. By default, logs are stored in the bucket where the `LoggingConfiguration` property is defined\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogFilePrefix`  <a name="cfn-s3-bucket-loggingconfig-logfileprefix"></a>
A prefix for all log object keys\. If you store log files from multiple Amazon S3 buckets in a single bucket, you can use a prefix to distinguish which log files came from which bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-loggingconfig--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)


# AWS::S3::Bucket LoggingConfiguration<a name="aws-properties-s3-bucket-loggingconfig"></a>

Describes where logs are stored and the prefix that Amazon S3 assigns to all log object keys for a bucket\. For examples and more information, see [PUT Bucket logging](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTlogging.html) in the *Amazon S3 API Reference*\.

**Note**  
To successfully complete the `AWS::S3::Bucket LoggingConfiguration` request, you must have `s3:PutObject` and `s3:PutObjectAcl` in your IAM permissions\.

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

## Examples<a name="aws-properties-s3-bucket-loggingconfig--examples"></a>



### Log access requests for a specific S3 bucket<a name="aws-properties-s3-bucket-loggingconfig--examples--Log_access_requests_for_a_specific_S3_bucket"></a>

The following example template creates two S3 buckets\. The `LoggingBucket` bucket store the logs from the `S3Bucket` bucket\. To receive logs from the `S3Bucket` bucket, the logging bucket requires log delivery write permissions\.

#### JSON<a name="aws-properties-s3-bucket-loggingconfig--examples--Log_access_requests_for_a_specific_S3_bucket--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "Private",
                "LoggingConfiguration": {
                    "DestinationBucketName": {
                        "Ref": "LoggingBucket"
                    },
                    "LogFilePrefix": "testing-logs"
                }
            }
        },
        "LoggingBucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "LogDeliveryWrite"
            }
        }
    },
    "Outputs": {
        "BucketName": {
            "Value": {
                "Ref": "S3Bucket"
            },
            "Description": "Name of the sample Amazon S3 bucket with a logging configuration."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-loggingconfig--examples--Log_access_requests_for_a_specific_S3_bucket--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: Private
      LoggingConfiguration:
        DestinationBucketName: !Ref LoggingBucket
        LogFilePrefix: testing-logs
  LoggingBucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: LogDeliveryWrite
Outputs:
  BucketName:
    Value: !Ref S3Bucket
    Description: Name of the sample Amazon S3 bucket with a logging configuration.
```
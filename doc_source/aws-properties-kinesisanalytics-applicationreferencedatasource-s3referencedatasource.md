# AWS::KinesisAnalytics::ApplicationReferenceDataSource S3ReferenceDataSource<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource"></a>

Identifies the S3 bucket and object that contains the reference data\. Also identifies the IAM role Amazon Kinesis Analytics can assume to read this object on your behalf\.

An Amazon Kinesis Analytics application loads reference data only once\. If the data changes, you call the [UpdateApplication](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/API_UpdateApplication.html) operation to trigger reloading of data into your application\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-syntax.json"></a>

```
{
  "[BucketARN](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-bucketarn)" : String,
  "[FileKey](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-filekey)" : String,
  "[ReferenceRoleARN](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-referencerolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-syntax.yaml"></a>

```
  [BucketARN](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-bucketarn): String
  [FileKey](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-filekey): String
  [ReferenceRoleARN](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-referencerolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-properties"></a>

`BucketARN`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-bucketarn"></a>
Amazon Resource Name \(ARN\) of the S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileKey`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-filekey"></a>
Object key name containing reference data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReferenceRoleARN`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-referencerolearn"></a>
ARN of the IAM role that the service can assume to read data on your behalf\. This role must have permission for the `s3:GetObject` action on the object and trust policy that allows Amazon Kinesis Analytics service principal to assume this role\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
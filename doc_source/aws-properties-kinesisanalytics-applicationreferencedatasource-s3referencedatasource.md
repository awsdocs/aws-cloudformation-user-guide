# Amazon Kinesis Data Analytics ApplicationReferenceDataSource S3ReferenceDataSource<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource"></a>

The `S3ReferenceDataSource` property type specifies the Amazon S3 bucket and object that contains the reference data for Amazon Kinesis Data Analytics\.

 `S3ReferenceDataSource` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md) parameter\. 

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
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FileKey`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-filekey"></a>
The object key name containing reference data\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ReferenceRoleARN`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-referencerolearn"></a>
The ARN of the IAM role that the service can assume to read data on your behalf\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
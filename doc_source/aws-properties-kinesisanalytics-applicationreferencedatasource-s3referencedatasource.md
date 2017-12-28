# Amazon Kinesis Data Analytics ApplicationReferenceDataSource S3ReferenceDataSource<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource"></a>

The `S3ReferenceDataSource` property type specifies the Amazon S3 bucket and object that contains the reference data for Amazon Kinesis Data Analytics\.

 `S3ReferenceDataSource` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md) parameter\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-bucketarn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-filekey)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-referencerolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-bucketarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-filekey): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-referencerolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource-properties"></a>

`BucketARN`  
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: No interruption 

`FileKey`  
The object key name containing reference data\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: No interruption 

`ReferenceRoleARN`  
The ARN of the IAM role that the service can assume to read data on your behalf\.  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: No interruption 
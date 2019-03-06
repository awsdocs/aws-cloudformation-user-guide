# Amazon Kinesis Data Analytics ApplicationReferenceDataSource S3ReferenceDataSource<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-description"></a>The `S3ReferenceDataSource` property type specifies the Amazon S3 bucket and object that contains reference data for a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-inheritance"></a> `S3ReferenceDataSource` is a property of the [ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-syntax.json"></a>

```
{
  "[BucketARN](#cfn-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-bucketarn)" : String,
  "[FileKey](#cfn-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-filekey)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-syntax.yaml"></a>

```
[BucketARN](#cfn-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-bucketarn): String
[FileKey](#cfn-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-filekey): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-properties"></a>

`BucketARN`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-bucketarn"></a>
The Amazon Resource Name \(ARN\) of the S3 bucket\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FileKey`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource-filekey"></a>
The object key name containing the reference data\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
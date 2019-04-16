# Amazon Kinesis Data Analytics Application S3ContentLocation<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation"></a>

<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation-description"></a>The `S3ContentLocation` property type specifies a description of an Amazon S3 object, including the Amazon Resource Name \(ARN\) of the S3 bucket, the name of the Amazon S3 object that contains the data, and the version number of the Amazon S3 object that contains the data for a Java\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation-inheritance"></a> `S3ContentLocation` is a property of the [CodeContent](aws-properties-kinesisanalyticsv2-application-codecontent.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation-syntax.json"></a>

```
{
  "[BucketARN](#cfn-kinesisanalyticsv2-application-s3contentlocation-bucketarn)" : String,
  "[FileKey](#cfn-kinesisanalyticsv2-application-s3contentlocation-filekey)" : String,
  "[ObjectVersion](#cfn-kinesisanalyticsv2-application-s3contentlocation-objectversion)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation-syntax.yaml"></a>

```
[BucketARN](#cfn-kinesisanalyticsv2-application-s3contentlocation-bucketarn): String
[FileKey](#cfn-kinesisanalyticsv2-application-s3contentlocation-filekey): String
[ObjectVersion](#cfn-kinesisanalyticsv2-application-s3contentlocation-objectversion): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation-properties"></a>

`BucketARN`  <a name="cfn-kinesisanalyticsv2-application-s3contentlocation-bucketarn"></a>
The Amazon Resource Name \(ARN\) for the S3 bucket containing the application code\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FileKey`  <a name="cfn-kinesisanalyticsv2-application-s3contentlocation-filekey"></a>
The file key for the object containing the application code\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ObjectVersion`  <a name="cfn-kinesisanalyticsv2-application-s3contentlocation-objectversion"></a>
The version of the object containing the application code\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 
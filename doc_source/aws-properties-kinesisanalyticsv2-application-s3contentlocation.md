# AWS::KinesisAnalyticsV2::Application S3ContentLocation<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation"></a>

For a Flink\-based Kinesis Data Analytics application, provides a description of an Amazon S3 object, including the Amazon Resource Name \(ARN\) of the S3 bucket, the name of the Amazon S3 object that contains the data, and the version number of the Amazon S3 object that contains the data\. 

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
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileKey`  <a name="cfn-kinesisanalyticsv2-application-s3contentlocation-filekey"></a>
The file key for the object containing the application code\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectVersion`  <a name="cfn-kinesisanalyticsv2-application-s3contentlocation-objectversion"></a>
The version of the object containing the application code\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-s3contentlocation--seealso"></a>
+  [S3ContentLocation](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_S3ContentLocation.html) in the *Amazon Kinesis Data Analytics API Reference* 


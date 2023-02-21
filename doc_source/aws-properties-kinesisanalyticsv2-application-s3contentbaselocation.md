# AWS::KinesisAnalyticsV2::Application S3ContentBaseLocation<a name="aws-properties-kinesisanalyticsv2-application-s3contentbaselocation"></a>

The base location of the Amazon Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-s3contentbaselocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-s3contentbaselocation-syntax.json"></a>

```
{
  "[BasePath](#cfn-kinesisanalyticsv2-application-s3contentbaselocation-basepath)" : String,
  "[BucketARN](#cfn-kinesisanalyticsv2-application-s3contentbaselocation-bucketarn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-s3contentbaselocation-syntax.yaml"></a>

```
  [BasePath](#cfn-kinesisanalyticsv2-application-s3contentbaselocation-basepath): String
  [BucketARN](#cfn-kinesisanalyticsv2-application-s3contentbaselocation-bucketarn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-s3contentbaselocation-properties"></a>

`BasePath`  <a name="cfn-kinesisanalyticsv2-application-s3contentbaselocation-basepath"></a>
The base path for the S3 bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[a-zA-Z0-9/!-_.*'()]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketARN`  <a name="cfn-kinesisanalyticsv2-application-s3contentbaselocation-bucketarn"></a>
The Amazon Resource Name \(ARN\) of the S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
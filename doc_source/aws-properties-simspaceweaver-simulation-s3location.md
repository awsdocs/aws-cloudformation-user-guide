# AWS::SimSpaceWeaver::Simulation S3Location<a name="aws-properties-simspaceweaver-simulation-s3location"></a>

A location in Amazon Simple Storage Service \(Amazon S3\) where SimSpace Weaver stores simulation data, such as your app \.zip files and schema file\. For more information about Amazon S3, see the [https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)\.

## Syntax<a name="aws-properties-simspaceweaver-simulation-s3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-simspaceweaver-simulation-s3location-syntax.json"></a>

```
{
  "[BucketName](#cfn-simspaceweaver-simulation-s3location-bucketname)" : String,
  "[ObjectKey](#cfn-simspaceweaver-simulation-s3location-objectkey)" : String
}
```

### YAML<a name="aws-properties-simspaceweaver-simulation-s3location-syntax.yaml"></a>

```
  [BucketName](#cfn-simspaceweaver-simulation-s3location-bucketname): String
  [ObjectKey](#cfn-simspaceweaver-simulation-s3location-objectkey): String
```

## Properties<a name="aws-properties-simspaceweaver-simulation-s3location-properties"></a>

`BucketName`  <a name="cfn-simspaceweaver-simulation-s3location-bucketname"></a>
The name of an Amazon S3 bucket\. For more information about buckets, see [Creating, configuring, and working with Amazon S3 buckets](https://docs.aws.amazon.com/AmazonS3/latest/userguide/creating-buckets-s3.html) in the *Amazon Simple Storage Service User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectKey`  <a name="cfn-simspaceweaver-simulation-s3location-objectkey"></a>
The key name of an object in Amazon S3\. For more information about Amazon S3 objects and object keys, see [Uploading, downloading, and working with objects in Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/uploading-downloading-objects.html) in the *Amazon Simple Storage Service User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
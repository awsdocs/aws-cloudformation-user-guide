# AWS::IoTFleetWise::Campaign S3Config<a name="aws-properties-iotfleetwise-campaign-s3config"></a>

The Amazon S3 bucket where the AWS IoT FleetWise campaign sends data\. Amazon S3 is an object storage service that stores data as objects within buckets\. For more information, see [Creating, configuring, and working with Amazon S3 buckets](https://docs.aws.amazon.com/AmazonS3/latest/userguide/creating-buckets-s3.html) in the *Amazon Simple Storage Service User Guide*\.

## Syntax<a name="aws-properties-iotfleetwise-campaign-s3config-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-campaign-s3config-syntax.json"></a>

```
{
  "[BucketArn](#cfn-iotfleetwise-campaign-s3config-bucketarn)" : String,
  "[DataFormat](#cfn-iotfleetwise-campaign-s3config-dataformat)" : String,
  "[Prefix](#cfn-iotfleetwise-campaign-s3config-prefix)" : String,
  "[StorageCompressionFormat](#cfn-iotfleetwise-campaign-s3config-storagecompressionformat)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-campaign-s3config-syntax.yaml"></a>

```
  [BucketArn](#cfn-iotfleetwise-campaign-s3config-bucketarn): String
  [DataFormat](#cfn-iotfleetwise-campaign-s3config-dataformat): String
  [Prefix](#cfn-iotfleetwise-campaign-s3config-prefix): String
  [StorageCompressionFormat](#cfn-iotfleetwise-campaign-s3config-storagecompressionformat): String
```

## Properties<a name="aws-properties-iotfleetwise-campaign-s3config-properties"></a>

`BucketArn`  <a name="cfn-iotfleetwise-campaign-s3config-bucketarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `16`  
*Maximum*: `100`  
*Pattern*: `arn:(aws[a-zA-Z0-9-]*):s3:::.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataFormat`  <a name="cfn-iotfleetwise-campaign-s3config-dataformat"></a>
\(Optional\) Specify the format that files are saved in the Amazon S3 bucket\. You can save files in an Apache Parquet or JSON format\.  
+ Parquet \- Store data in a columnar storage file format\. Parquet is optimal for fast data retrieval and can reduce costs\. This option is selected by default\.
+ JSON \- Store data in a standard text\-based JSON file format\.
*Required*: No  
*Type*: String  
*Allowed values*: `JSON | PARQUET`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-iotfleetwise-campaign-s3config-prefix"></a>
\(Optional\) Enter an S3 bucket prefix\. The prefix is the string of characters after the bucket name and before the object name\. You can use the prefix to organize data stored in Amazon S3 buckets\. For more information, see [Organizing objects using prefixes](https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-prefixes.html) in the *Amazon Simple Storage Service User Guide*\.  
By default, AWS IoT FleetWise sets the prefix `processed-data/year=YY/month=MM/date=DD/hour=HH/` \(in UTC\) to data it delivers to Amazon S3\. You can enter a prefix to append it to this default prefix\. For example, if you enter the prefix `vehicles`, the prefix will be `vehicles/processed-data/year=YY/month=MM/date=DD/hour=HH/`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[a-zA-Z0-9-_:./!*'()]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageCompressionFormat`  <a name="cfn-iotfleetwise-campaign-s3config-storagecompressionformat"></a>
\(Optional\) By default, stored data is compressed as a \.gzip file\. Compressed files have a reduced file size, which can optimize the cost of data storage\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GZIP | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
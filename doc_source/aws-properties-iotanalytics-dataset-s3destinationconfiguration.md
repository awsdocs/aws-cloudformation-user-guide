# AWS::IoTAnalytics::Dataset S3DestinationConfiguration<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration"></a>

Configuration information for delivery of dataset contents to Amazon Simple Storage Service \(Amazon S3\)\.

## Syntax<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration-syntax.json"></a>

```
{
  "[Bucket](#cfn-iotanalytics-dataset-s3destinationconfiguration-bucket)" : String,
  "[GlueConfiguration](#cfn-iotanalytics-dataset-s3destinationconfiguration-glueconfiguration)" : GlueConfiguration,
  "[Key](#cfn-iotanalytics-dataset-s3destinationconfiguration-key)" : String,
  "[RoleArn](#cfn-iotanalytics-dataset-s3destinationconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration-syntax.yaml"></a>

```
  [Bucket](#cfn-iotanalytics-dataset-s3destinationconfiguration-bucket): String
  [GlueConfiguration](#cfn-iotanalytics-dataset-s3destinationconfiguration-glueconfiguration): 
    GlueConfiguration
  [Key](#cfn-iotanalytics-dataset-s3destinationconfiguration-key): String
  [RoleArn](#cfn-iotanalytics-dataset-s3destinationconfiguration-rolearn): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration-properties"></a>

`Bucket`  <a name="cfn-iotanalytics-dataset-s3destinationconfiguration-bucket"></a>
The name of the S3 bucket to which dataset contents are delivered\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9.\-_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlueConfiguration`  <a name="cfn-iotanalytics-dataset-s3destinationconfiguration-glueconfiguration"></a>
Configuration information for coordination with AWS Glue, a fully managed extract, transform and load \(ETL\) service\.  
*Required*: No  
*Type*: [GlueConfiguration](aws-properties-iotanalytics-dataset-glueconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-iotanalytics-dataset-s3destinationconfiguration-key"></a>
The key of the dataset contents object in an S3 bucket\. Each object has a key that is a unique identifier\. Each object has exactly one key\.  
You can create a unique key with the following options:  
+ Use `!{iotanalytics:scheduleTime}` to insert the time of a scheduled SQL query run\.
+ Use `!{iotanalytics:versionId}` to insert a unique hash that identifies a dataset content\.
+ Use `!{iotanalytics:creationTime}` to insert the creation time of a dataset content\.
The following example creates a unique key for a CSV file: `dataset/mydataset/!{iotanalytics:scheduleTime}/!{iotanalytics:versionId}.csv`   
If you don't use `!{iotanalytics:versionId}` to specify the key, you might get duplicate keys\. For example, you might have two dataset contents with the same `scheduleTime` but different `versionId`s\. This means that one dataset content overwrites the other\. 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9!_.*'()/{}:-]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iotanalytics-dataset-s3destinationconfiguration-rolearn"></a>
The ARN of the role that grants AWS IoT Analytics permission to interact with your Amazon S3 and AWS Glue resources\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
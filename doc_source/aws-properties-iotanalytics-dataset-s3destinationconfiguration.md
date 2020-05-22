# AWS::IoTAnalytics::Dataset S3DestinationConfiguration<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration"></a>

Configuration information for delivery of dataset contents to Amazon S3\.

## Syntax<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration-syntax.json"></a>

```
{
  "[Bucket](#cfn-iotanalytics-dataset-s3destinationconfiguration-bucket)" : String,
  "[GlueConfiguration](#cfn-iotanalytics-dataset-s3destinationconfiguration-glueconfiguration)" : [GlueConfiguration](aws-properties-iotanalytics-dataset-glueconfiguration.md),
  "[Key](#cfn-iotanalytics-dataset-s3destinationconfiguration-key)" : String,
  "[RoleArn](#cfn-iotanalytics-dataset-s3destinationconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-s3destinationconfiguration-syntax.yaml"></a>

```
  [Bucket](#cfn-iotanalytics-dataset-s3destinationconfiguration-bucket): String
  [GlueConfiguration](#cfn-iotanalytics-dataset-s3destinationconfiguration-glueconfiguration): 
    [GlueConfiguration](aws-properties-iotanalytics-dataset-glueconfiguration.md)
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
The key of the dataset contents object\. Each object in an S3 bucket has a key that is its unique identifier in the bucket\. Each object in a bucket has exactly one key\. To produce a unique key, you can use \!\{iotanalytics:scheduleTime\} to insert the time of the scheduled SQL query run, or \!\{iotanalytics:versionId\} to insert a unique hash identifying the dataset \(for example, /DataSet/\!\{iotanalytics:scheduleTime\}/\!\{iotanalytics:versionId\}\.csv\)\.  
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
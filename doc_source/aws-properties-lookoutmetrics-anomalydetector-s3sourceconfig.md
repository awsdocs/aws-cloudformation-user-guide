# AWS::LookoutMetrics::AnomalyDetector S3SourceConfig<a name="aws-properties-lookoutmetrics-anomalydetector-s3sourceconfig"></a>

Contains information about the configuration of the S3 bucket that contains source files\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-s3sourceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-s3sourceconfig-syntax.json"></a>

```
{
  "[FileFormatDescriptor](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-fileformatdescriptor)" : FileFormatDescriptor,
  "[HistoricalDataPathList](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-historicaldatapathlist)" : [ String, ... ],
  "[RoleArn](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-rolearn)" : String,
  "[TemplatedPathList](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-templatedpathlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-s3sourceconfig-syntax.yaml"></a>

```
  [FileFormatDescriptor](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-fileformatdescriptor): 
    FileFormatDescriptor
  [HistoricalDataPathList](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-historicaldatapathlist): 
    - String
  [RoleArn](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-rolearn): String
  [TemplatedPathList](#cfn-lookoutmetrics-anomalydetector-s3sourceconfig-templatedpathlist): 
    - String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-s3sourceconfig-properties"></a>

`FileFormatDescriptor`  <a name="cfn-lookoutmetrics-anomalydetector-s3sourceconfig-fileformatdescriptor"></a>
Contains information about a source file's formatting\.  
*Required*: Yes  
*Type*: [FileFormatDescriptor](aws-properties-lookoutmetrics-anomalydetector-fileformatdescriptor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HistoricalDataPathList`  <a name="cfn-lookoutmetrics-anomalydetector-s3sourceconfig-historicaldatapathlist"></a>
A list of paths to the historical data files\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-lookoutmetrics-anomalydetector-s3sourceconfig-rolearn"></a>
The ARN of an IAM role that has read and write access permissions to the source S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplatedPathList`  <a name="cfn-lookoutmetrics-anomalydetector-s3sourceconfig-templatedpathlist"></a>
A list of templated paths to the source files\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
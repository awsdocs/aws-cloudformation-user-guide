# AWS::KinesisAnalyticsV2::Application KinesisFirehoseInput<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput"></a>

For a SQL\-based Kinesis Data Analytics application, identifies a Kinesis Data Firehose delivery stream as the streaming source\. You provide the delivery stream's Amazon Resource Name \(ARN\)\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisfirehoseinput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalyticsv2-application-kinesisfirehoseinput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-application-kinesisfirehoseinput-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the delivery stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-kinesisfirehoseinput--seealso"></a>
+  [KinesisFirehoseInput](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_KinesisFirehoseInput.html) in the *Amazon Kinesis Data Analytics API Reference* 


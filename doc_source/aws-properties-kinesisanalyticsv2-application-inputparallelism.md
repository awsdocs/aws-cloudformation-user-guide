# AWS::KinesisAnalyticsV2::Application InputParallelism<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism"></a>

For a SQL\-based Kinesis Data Analytics application, describes the number of in\-application streams to create for a given streaming source\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-syntax.json"></a>

```
{
  "[Count](#cfn-kinesisanalyticsv2-application-inputparallelism-count)" : Integer
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-syntax.yaml"></a>

```
  [Count](#cfn-kinesisanalyticsv2-application-inputparallelism-count): Integer
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism-properties"></a>

`Count`  <a name="cfn-kinesisanalyticsv2-application-inputparallelism-count"></a>
The number of in\-application streams to create\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-inputparallelism--seealso"></a>
+  [InputParallelism](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_InputParallelism.html) in the *Amazon Kinesis Data Analytics API Reference* 


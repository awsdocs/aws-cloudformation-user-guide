# AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption"></a>

The `AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption` resource to add an Amazon CloudWatch log stream to monitor application configuration errors\. For more information, see [CloudWatchLoggingOption](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_CloudWatchLoggingOption.html) in the *Amazon Kinesis Data Analytics Developer Guide*\. 

## Syntax<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption",
  "Properties" : {
    "[ApplicationName](#cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-applicationname)" : String,
    "[CloudWatchLoggingOption](#cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption)" : [*CloudWatchLoggingOption*](aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption.md)
  }
}
```

### YAML<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption"
Properties:
  [ApplicationName](#cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-applicationname): String
  [CloudWatchLoggingOption](#cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption): [*CloudWatchLoggingOption*](aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption.md)
```

## Properties<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-applicationname"></a>
The name of your application \(for example, sample\-app\)\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CloudWatchLoggingOption`  <a name="cfn-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption"></a>
Use this parameter to configure an Amazon CloudWatch log stream to monitor application configuration errors\.   
 *Required*: Yes  
 *Type*: [CloudWatchLoggingOption](aws-properties-kinesisanalyticsv2-applicationcloudwatchloggingoption-cloudwatchloggingoption.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption-examples"></a>

### ApplicationCloudWatchLoggingOption example<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption-example1"></a>

The following example demonstrates how to create an `ApplicationCloudWatchLoggingOption` resource\.

#### YAML<a name="aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption-example1.yaml"></a>

```
BasicApplicationV2CloudWatchLoggingOption:
  Type: "AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption"
  Properties:
    ApplicationName: !Ref BasicApplication
    CloudWatchLoggingOption:
      LogStreamARN:
        !Join
        - ':'
        - - 'arn:aws:logs'
          - !Ref AWS::Region
          - !Ref AWS::AccountId
          - 'log-group'
          - !Ref TestCWLogGroup
          - 'log-stream'
          - !Ref TestCWLogStream
```
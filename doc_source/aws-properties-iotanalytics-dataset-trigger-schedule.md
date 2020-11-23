# AWS::IoTAnalytics::Dataset Schedule<a name="aws-properties-iotanalytics-dataset-trigger-schedule"></a>

The schedule for when to trigger an update\.

## Syntax<a name="aws-properties-iotanalytics-dataset-trigger-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-trigger-schedule-syntax.json"></a>

```
{
  "[ScheduleExpression](#cfn-iotanalytics-dataset-trigger-schedule-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-trigger-schedule-syntax.yaml"></a>

```
  [ScheduleExpression](#cfn-iotanalytics-dataset-trigger-schedule-scheduleexpression): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-trigger-schedule-properties"></a>

`ScheduleExpression`  <a name="cfn-iotanalytics-dataset-trigger-schedule-scheduleexpression"></a>
The expression that defines when to trigger an update\. For more information, see [ Schedule Expressions for Rules](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/ScheduledEvents.html) in the Amazon CloudWatch documentation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
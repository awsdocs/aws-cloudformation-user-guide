# AWS IoT Analytics Dataset Schedule<a name="aws-properties-iotanalytics-dataset-schedule"></a>

<a name="aws-properties-iotanalytics-dataset-schedule-description"></a>The `Schedule` property type specifies the "schedule" when a trigger is initiated for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-schedule-inheritance"></a> `Schedule` is a property of the [Trigger](aws-properties-iotanalytics-dataset-trigger.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-schedule-syntax.json"></a>

```
{
  "[ScheduleExpression](#cfn-iotanalytics-dataset-schedule-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-schedule-syntax.yaml"></a>

```
[ScheduleExpression](#cfn-iotanalytics-dataset-schedule-scheduleexpression): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-schedule-properties"></a>

`ScheduleExpression`  <a name="cfn-iotanalytics-dataset-schedule-scheduleexpression"></a>
The expression that defines when to trigger an update\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-schedule-seealso"></a>
+ [ CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *AWS IoT Analytics User Guide*
# AWS::CustomerProfiles::Integration ScheduledTriggerProperties<a name="aws-properties-customerprofiles-integration-scheduledtriggerproperties"></a>

Specifies the configuration details of a scheduled\-trigger flow that you define\. Currently, these settings only apply to the scheduled\-trigger type\.

## Syntax<a name="aws-properties-customerprofiles-integration-scheduledtriggerproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-scheduledtriggerproperties-syntax.json"></a>

```
{
  "[DataPullMode](#cfn-customerprofiles-integration-scheduledtriggerproperties-datapullmode)" : String,
  "[FirstExecutionFrom](#cfn-customerprofiles-integration-scheduledtriggerproperties-firstexecutionfrom)" : Double,
  "[ScheduleEndTime](#cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleendtime)" : Double,
  "[ScheduleExpression](#cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleexpression)" : String,
  "[ScheduleOffset](#cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleoffset)" : Integer,
  "[ScheduleStartTime](#cfn-customerprofiles-integration-scheduledtriggerproperties-schedulestarttime)" : Double,
  "[Timezone](#cfn-customerprofiles-integration-scheduledtriggerproperties-timezone)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-scheduledtriggerproperties-syntax.yaml"></a>

```
  [DataPullMode](#cfn-customerprofiles-integration-scheduledtriggerproperties-datapullmode): String
  [FirstExecutionFrom](#cfn-customerprofiles-integration-scheduledtriggerproperties-firstexecutionfrom): Double
  [ScheduleEndTime](#cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleendtime): Double
  [ScheduleExpression](#cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleexpression): String
  [ScheduleOffset](#cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleoffset): Integer
  [ScheduleStartTime](#cfn-customerprofiles-integration-scheduledtriggerproperties-schedulestarttime): Double
  [Timezone](#cfn-customerprofiles-integration-scheduledtriggerproperties-timezone): String
```

## Properties<a name="aws-properties-customerprofiles-integration-scheduledtriggerproperties-properties"></a>

`DataPullMode`  <a name="cfn-customerprofiles-integration-scheduledtriggerproperties-datapullmode"></a>
Specifies whether a scheduled flow has an incremental data transfer or a complete data transfer for each flow run\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Complete | Incremental`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirstExecutionFrom`  <a name="cfn-customerprofiles-integration-scheduledtriggerproperties-firstexecutionfrom"></a>
Specifies the date range for the records to import from the connector in the first flow run\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleEndTime`  <a name="cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleendtime"></a>
Specifies the scheduled end time for a scheduled\-trigger flow\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleexpression"></a>
The scheduling expression that determines the rate at which the schedule will run, for example rate \(5 minutes\)\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleOffset`  <a name="cfn-customerprofiles-integration-scheduledtriggerproperties-scheduleoffset"></a>
Specifies the optional offset that is added to the time interval for a schedule\-triggered flow\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleStartTime`  <a name="cfn-customerprofiles-integration-scheduledtriggerproperties-schedulestarttime"></a>
Specifies the scheduled start time for a scheduled\-trigger flow\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timezone`  <a name="cfn-customerprofiles-integration-scheduledtriggerproperties-timezone"></a>
Specifies the time zone used when referring to the date and time of a scheduled\-triggered flow, such as America/New\_York\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
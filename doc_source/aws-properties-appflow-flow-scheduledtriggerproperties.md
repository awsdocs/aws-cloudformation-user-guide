# AWS::AppFlow::Flow ScheduledTriggerProperties<a name="aws-properties-appflow-flow-scheduledtriggerproperties"></a>

 Specifies the configuration details of a schedule\-triggered flow as defined by the user\. Currently, these settings only apply to the `Scheduled` trigger type\. 

## Syntax<a name="aws-properties-appflow-flow-scheduledtriggerproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-scheduledtriggerproperties-syntax.json"></a>

```
{
  "[DataPullMode](#cfn-appflow-flow-scheduledtriggerproperties-datapullmode)" : String,
  "[ScheduleEndTime](#cfn-appflow-flow-scheduledtriggerproperties-scheduleendtime)" : Double,
  "[ScheduleExpression](#cfn-appflow-flow-scheduledtriggerproperties-scheduleexpression)" : String,
  "[ScheduleStartTime](#cfn-appflow-flow-scheduledtriggerproperties-schedulestarttime)" : Double,
  "[TimeZone](#cfn-appflow-flow-scheduledtriggerproperties-timezone)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-scheduledtriggerproperties-syntax.yaml"></a>

```
  [DataPullMode](#cfn-appflow-flow-scheduledtriggerproperties-datapullmode): String
  [ScheduleEndTime](#cfn-appflow-flow-scheduledtriggerproperties-scheduleendtime): Double
  [ScheduleExpression](#cfn-appflow-flow-scheduledtriggerproperties-scheduleexpression): String
  [ScheduleStartTime](#cfn-appflow-flow-scheduledtriggerproperties-schedulestarttime): Double
  [TimeZone](#cfn-appflow-flow-scheduledtriggerproperties-timezone): String
```

## Properties<a name="aws-properties-appflow-flow-scheduledtriggerproperties-properties"></a>

`DataPullMode`  <a name="cfn-appflow-flow-scheduledtriggerproperties-datapullmode"></a>
 Specifies whether a scheduled flow has an incremental data transfer or a complete data transfer for each flow run\.   
*Required*: No  
*Type*: String  
*Allowed values*: `Complete | Incremental`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleEndTime`  <a name="cfn-appflow-flow-scheduledtriggerproperties-scheduleendtime"></a>
 Specifies the scheduled end time for a schedule\-triggered flow\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-appflow-flow-scheduledtriggerproperties-scheduleexpression"></a>
 The scheduling expression that determines the rate at which the scheduled flow will run, for example: `rate(5minutes)`\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleStartTime`  <a name="cfn-appflow-flow-scheduledtriggerproperties-schedulestarttime"></a>
 Specifies the scheduled start time for a schedule\-triggered flow\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZone`  <a name="cfn-appflow-flow-scheduledtriggerproperties-timezone"></a>
 Specifies the time zone used when referring to the date and time of a scheduled\-triggered flow\.   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-scheduledtriggerproperties--seealso"></a>
+ [ScheduledTriggerProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ScheduledTriggerProperties.html) in the *Amazon AppFlow API Reference*\.


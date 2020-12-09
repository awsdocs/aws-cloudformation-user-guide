# AWS::SageMaker::MonitoringSchedule MonitoringScheduleConfig<a name="aws-properties-sagemaker-monitoringschedule-monitoringscheduleconfig"></a>

Configures the monitoring schedule and defines the monitoring job\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringscheduleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringscheduleconfig-syntax.json"></a>

```
{
  "[MonitoringJobDefinition](#cfn-sagemaker-monitoringschedule-monitoringscheduleconfig-monitoringjobdefinition)" : MonitoringJobDefinition,
  "[ScheduleConfig](#cfn-sagemaker-monitoringschedule-monitoringscheduleconfig-scheduleconfig)" : ScheduleConfig
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringscheduleconfig-syntax.yaml"></a>

```
  [MonitoringJobDefinition](#cfn-sagemaker-monitoringschedule-monitoringscheduleconfig-monitoringjobdefinition): 
    MonitoringJobDefinition
  [ScheduleConfig](#cfn-sagemaker-monitoringschedule-monitoringscheduleconfig-scheduleconfig): 
    ScheduleConfig
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringscheduleconfig-properties"></a>

`MonitoringJobDefinition`  <a name="cfn-sagemaker-monitoringschedule-monitoringscheduleconfig-monitoringjobdefinition"></a>
Defines the monitoring job\.  
*Required*: Yes  
*Type*: [MonitoringJobDefinition](aws-properties-sagemaker-monitoringschedule-monitoringjobdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleConfig`  <a name="cfn-sagemaker-monitoringschedule-monitoringscheduleconfig-scheduleconfig"></a>
Configures the monitoring schedule\.  
*Required*: No  
*Type*: [ScheduleConfig](aws-properties-sagemaker-monitoringschedule-scheduleconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
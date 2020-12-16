# AWS::SageMaker::MonitoringSchedule ScheduleConfig<a name="aws-properties-sagemaker-monitoringschedule-scheduleconfig"></a>

Configuration details about the monitoring schedule\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-scheduleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-scheduleconfig-syntax.json"></a>

```
{
  "[ScheduleExpression](#cfn-sagemaker-monitoringschedule-scheduleconfig-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-scheduleconfig-syntax.yaml"></a>

```
  [ScheduleExpression](#cfn-sagemaker-monitoringschedule-scheduleconfig-scheduleexpression): String
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-scheduleconfig-properties"></a>

`ScheduleExpression`  <a name="cfn-sagemaker-monitoringschedule-scheduleconfig-scheduleexpression"></a>
A cron expression that describes details about the monitoring schedule\.  
Currently the only supported cron expressions are:  
+ If you want to set the job to start every hour, please use the following:

   `Hourly: cron(0 * ? * * *)` 
+ If you want to start the job daily:

   `cron(0 [00-23] ? * * *)` 
For example, the following are valid cron expressions:  
+ Daily at noon UTC: `cron(0 12 ? * * *)` 
+ Daily at midnight UTC: `cron(0 0 ? * * *)` 
To support running every 6, 12 hours, the following are also supported:  
 `cron(0 [00-23]/[01-24] ? * * *)`   
For example, the following are valid cron expressions:  
+ Every 12 hours, starting at 5pm UTC: `cron(0 17/12 ? * * *)` 
+ Every two hours starting at midnight: `cron(0 0/2 ? * * *)` 
+ Even though the cron expression is set to start at 5PM UTC, note that there could be a delay of 0\-20 minutes from the actual requested time to run the execution\. 
+ We recommend that if you would like a daily schedule, you do not provide this parameter\. Amazon SageMaker will pick a time for running every day\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
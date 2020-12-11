# AWS::SageMaker::MonitoringSchedule MonitoringExecutionSummary<a name="aws-properties-sagemaker-monitoringschedule-monitoringexecutionsummary"></a>

Summary of information about the last monitoring job to run\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringexecutionsummary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringexecutionsummary-syntax.json"></a>

```
{
  "[CreationTime](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-creationtime)" : String,
  "[EndpointName](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-endpointname)" : String,
  "[FailureReason](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-failurereason)" : String,
  "[LastModifiedTime](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-lastmodifiedtime)" : String,
  "[MonitoringExecutionStatus](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-monitoringexecutionstatus)" : String,
  "[MonitoringScheduleName](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-monitoringschedulename)" : String,
  "[ProcessingJobArn](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-processingjobarn)" : String,
  "[ScheduledTime](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-scheduledtime)" : String
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringexecutionsummary-syntax.yaml"></a>

```
  [CreationTime](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-creationtime): String
  [EndpointName](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-endpointname): String
  [FailureReason](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-failurereason): String
  [LastModifiedTime](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-lastmodifiedtime): String
  [MonitoringExecutionStatus](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-monitoringexecutionstatus): String
  [MonitoringScheduleName](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-monitoringschedulename): String
  [ProcessingJobArn](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-processingjobarn): String
  [ScheduledTime](#cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-scheduledtime): String
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringexecutionsummary-properties"></a>

`CreationTime`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-creationtime"></a>
The time at which the monitoring job was created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointName`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-endpointname"></a>
The name of the endpoint used to run the monitoring job\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureReason`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-failurereason"></a>
Contains the reason a monitoring job failed, if it failed\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastModifiedTime`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-lastmodifiedtime"></a>
A timestamp that indicates the last time the monitoring job was modified\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringExecutionStatus`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-monitoringexecutionstatus"></a>
The status of the monitoring job\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Completed | CompletedWithViolations | Failed | InProgress | Pending | Stopped | Stopping`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringScheduleName`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-monitoringschedulename"></a>
The name of the monitoring schedule\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProcessingJobArn`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-processingjobarn"></a>
The Amazon Resource Name \(ARN\) of the monitoring job\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `arn:aws[a-z\-]*:sagemaker:[a-z0-9\-]*:[0-9]{12}:processing-job/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduledTime`  <a name="cfn-sagemaker-monitoringschedule-monitoringexecutionsummary-scheduledtime"></a>
The time the monitoring job was scheduled\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
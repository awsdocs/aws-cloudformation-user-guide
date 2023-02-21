# AWS::IoT::JobTemplate TimeoutConfig<a name="aws-properties-iot-jobtemplate-timeoutconfig"></a>

Specifies the amount of time each device has to finish its execution of the job\. A timer is started when the job execution status is set to `IN_PROGRESS`\. If the job execution status is not set to another terminal state before the timer expires, it will be automatically set to `TIMED_OUT`\.

## Syntax<a name="aws-properties-iot-jobtemplate-timeoutconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-timeoutconfig-syntax.json"></a>

```
{
  "[InProgressTimeoutInMinutes](#cfn-iot-jobtemplate-timeoutconfig-inprogresstimeoutinminutes)" : Integer
}
```

### YAML<a name="aws-properties-iot-jobtemplate-timeoutconfig-syntax.yaml"></a>

```
  [InProgressTimeoutInMinutes](#cfn-iot-jobtemplate-timeoutconfig-inprogresstimeoutinminutes): Integer
```

## Properties<a name="aws-properties-iot-jobtemplate-timeoutconfig-properties"></a>

`InProgressTimeoutInMinutes`  <a name="cfn-iot-jobtemplate-timeoutconfig-inprogresstimeoutinminutes"></a>
Specifies the amount of time, in minutes, this device has to finish execution of this job\. The timeout interval can be anywhere between 1 minute and 7 days \(1 to 10080 minutes\)\. The in progress timer can't be updated and will apply to all job executions for the job\. Whenever a job execution remains in the IN\_PROGRESS status for longer than this interval, the job execution will fail and switch to the terminal `TIMED_OUT` status\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
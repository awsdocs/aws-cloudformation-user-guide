# AWS::GreengrassV2::Deployment IoTJobTimeoutConfig<a name="aws-properties-greengrassv2-deployment-iotjobtimeoutconfig"></a>

Contains information about the timeout configuration for a job\.

## Syntax<a name="aws-properties-greengrassv2-deployment-iotjobtimeoutconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-iotjobtimeoutconfig-syntax.json"></a>

```
{
  "[InProgressTimeoutInMinutes](#cfn-greengrassv2-deployment-iotjobtimeoutconfig-inprogresstimeoutinminutes)" : Integer
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-iotjobtimeoutconfig-syntax.yaml"></a>

```
  [InProgressTimeoutInMinutes](#cfn-greengrassv2-deployment-iotjobtimeoutconfig-inprogresstimeoutinminutes): Integer
```

## Properties<a name="aws-properties-greengrassv2-deployment-iotjobtimeoutconfig-properties"></a>

`InProgressTimeoutInMinutes`  <a name="cfn-greengrassv2-deployment-iotjobtimeoutconfig-inprogresstimeoutinminutes"></a>
The amount of time, in minutes, that devices have to complete the job\. The timer starts when the job status is set to `IN_PROGRESS`\. If the job status doesn't change to a terminal state before the time expires, then the job status is set to `TIMED_OUT`\.  
The timeout interval must be between 1 minute and 7 days \(10080 minutes\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
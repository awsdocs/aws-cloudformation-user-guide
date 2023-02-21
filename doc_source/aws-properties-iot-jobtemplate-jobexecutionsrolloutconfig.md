# AWS::IoT::JobTemplate JobExecutionsRolloutConfig<a name="aws-properties-iot-jobtemplate-jobexecutionsrolloutconfig"></a>

Allows you to create a staged rollout of a job\.

## Syntax<a name="aws-properties-iot-jobtemplate-jobexecutionsrolloutconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-jobexecutionsrolloutconfig-syntax.json"></a>

```
{
  "[ExponentialRolloutRate](#cfn-iot-jobtemplate-jobexecutionsrolloutconfig-exponentialrolloutrate)" : ExponentialRolloutRate,
  "[MaximumPerMinute](#cfn-iot-jobtemplate-jobexecutionsrolloutconfig-maximumperminute)" : Integer
}
```

### YAML<a name="aws-properties-iot-jobtemplate-jobexecutionsrolloutconfig-syntax.yaml"></a>

```
  [ExponentialRolloutRate](#cfn-iot-jobtemplate-jobexecutionsrolloutconfig-exponentialrolloutrate): 
    ExponentialRolloutRate
  [MaximumPerMinute](#cfn-iot-jobtemplate-jobexecutionsrolloutconfig-maximumperminute): Integer
```

## Properties<a name="aws-properties-iot-jobtemplate-jobexecutionsrolloutconfig-properties"></a>

`ExponentialRolloutRate`  <a name="cfn-iot-jobtemplate-jobexecutionsrolloutconfig-exponentialrolloutrate"></a>
Allows you to create an exponential rate of rollout for a job\.  
*Required*: No  
*Type*: [ExponentialRolloutRate](aws-properties-iot-jobtemplate-exponentialrolloutrate.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaximumPerMinute`  <a name="cfn-iot-jobtemplate-jobexecutionsrolloutconfig-maximumperminute"></a>
The maximum number of things that will be notified of a pending job, per minute\. This parameter allows you to create a staged rollout\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
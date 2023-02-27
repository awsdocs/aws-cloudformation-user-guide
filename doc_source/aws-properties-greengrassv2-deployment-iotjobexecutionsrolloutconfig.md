# AWS::GreengrassV2::Deployment IoTJobExecutionsRolloutConfig<a name="aws-properties-greengrassv2-deployment-iotjobexecutionsrolloutconfig"></a>

Contains information about the rollout configuration for a job\. This configuration defines the rate at which the job deploys a configuration to a fleet of target devices\.

## Syntax<a name="aws-properties-greengrassv2-deployment-iotjobexecutionsrolloutconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-iotjobexecutionsrolloutconfig-syntax.json"></a>

```
{
  "[ExponentialRate](#cfn-greengrassv2-deployment-iotjobexecutionsrolloutconfig-exponentialrate)" : IoTJobExponentialRolloutRate,
  "[MaximumPerMinute](#cfn-greengrassv2-deployment-iotjobexecutionsrolloutconfig-maximumperminute)" : Integer
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-iotjobexecutionsrolloutconfig-syntax.yaml"></a>

```
  [ExponentialRate](#cfn-greengrassv2-deployment-iotjobexecutionsrolloutconfig-exponentialrate): 
    IoTJobExponentialRolloutRate
  [MaximumPerMinute](#cfn-greengrassv2-deployment-iotjobexecutionsrolloutconfig-maximumperminute): Integer
```

## Properties<a name="aws-properties-greengrassv2-deployment-iotjobexecutionsrolloutconfig-properties"></a>

`ExponentialRate`  <a name="cfn-greengrassv2-deployment-iotjobexecutionsrolloutconfig-exponentialrate"></a>
The exponential rate to increase the job rollout rate\.  
*Required*: No  
*Type*: [IoTJobExponentialRolloutRate](aws-properties-greengrassv2-deployment-iotjobexponentialrolloutrate.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaximumPerMinute`  <a name="cfn-greengrassv2-deployment-iotjobexecutionsrolloutconfig-maximumperminute"></a>
The maximum number of devices that receive a pending job notification, per minute\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
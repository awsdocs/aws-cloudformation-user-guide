# AWS::IoT::JobTemplate ExponentialRolloutRate<a name="aws-properties-iot-jobtemplate-exponentialrolloutrate"></a>

Allows you to create an exponential rate of rollout for a job\.

## Syntax<a name="aws-properties-iot-jobtemplate-exponentialrolloutrate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-exponentialrolloutrate-syntax.json"></a>

```
{
  "[BaseRatePerMinute](#cfn-iot-jobtemplate-exponentialrolloutrate-baserateperminute)" : Integer,
  "[IncrementFactor](#cfn-iot-jobtemplate-exponentialrolloutrate-incrementfactor)" : Double,
  "[RateIncreaseCriteria](#cfn-iot-jobtemplate-exponentialrolloutrate-rateincreasecriteria)" : RateIncreaseCriteria
}
```

### YAML<a name="aws-properties-iot-jobtemplate-exponentialrolloutrate-syntax.yaml"></a>

```
  [BaseRatePerMinute](#cfn-iot-jobtemplate-exponentialrolloutrate-baserateperminute): Integer
  [IncrementFactor](#cfn-iot-jobtemplate-exponentialrolloutrate-incrementfactor): Double
  [RateIncreaseCriteria](#cfn-iot-jobtemplate-exponentialrolloutrate-rateincreasecriteria): 
    RateIncreaseCriteria
```

## Properties<a name="aws-properties-iot-jobtemplate-exponentialrolloutrate-properties"></a>

`BaseRatePerMinute`  <a name="cfn-iot-jobtemplate-exponentialrolloutrate-baserateperminute"></a>
The minimum number of things that will be notified of a pending job, per minute at the start of job rollout\. This parameter allows you to define the initial rate of rollout\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IncrementFactor`  <a name="cfn-iot-jobtemplate-exponentialrolloutrate-incrementfactor"></a>
The exponential factor to increase the rate of rollout for a job\.  
 AWS IoT Core supports up to one digit after the decimal \(for example, 1\.5, but not 1\.55\)\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RateIncreaseCriteria`  <a name="cfn-iot-jobtemplate-exponentialrolloutrate-rateincreasecriteria"></a>
The criteria to initiate the increase in rate of rollout for a job\.  
*Required*: Yes  
*Type*: [RateIncreaseCriteria](aws-properties-iot-jobtemplate-rateincreasecriteria.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
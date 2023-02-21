# AWS::IoT::JobTemplate RateIncreaseCriteria<a name="aws-properties-iot-jobtemplate-rateincreasecriteria"></a>

Allows you to define a criteria to initiate the increase in rate of rollout for a job\.

## Syntax<a name="aws-properties-iot-jobtemplate-rateincreasecriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-rateincreasecriteria-syntax.json"></a>

```
{
  "[NumberOfNotifiedThings](#cfn-iot-jobtemplate-rateincreasecriteria-numberofnotifiedthings)" : Integer,
  "[NumberOfSucceededThings](#cfn-iot-jobtemplate-rateincreasecriteria-numberofsucceededthings)" : Integer
}
```

### YAML<a name="aws-properties-iot-jobtemplate-rateincreasecriteria-syntax.yaml"></a>

```
  [NumberOfNotifiedThings](#cfn-iot-jobtemplate-rateincreasecriteria-numberofnotifiedthings): Integer
  [NumberOfSucceededThings](#cfn-iot-jobtemplate-rateincreasecriteria-numberofsucceededthings): Integer
```

## Properties<a name="aws-properties-iot-jobtemplate-rateincreasecriteria-properties"></a>

`NumberOfNotifiedThings`  <a name="cfn-iot-jobtemplate-rateincreasecriteria-numberofnotifiedthings"></a>
The threshold for number of notified things that will initiate the increase in rate of rollout\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NumberOfSucceededThings`  <a name="cfn-iot-jobtemplate-rateincreasecriteria-numberofsucceededthings"></a>
The threshold for number of succeeded things that will initiate the increase in rate of rollout\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
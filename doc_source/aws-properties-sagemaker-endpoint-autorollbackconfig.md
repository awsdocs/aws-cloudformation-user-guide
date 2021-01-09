# AWS::SageMaker::Endpoint AutoRollbackConfig<a name="aws-properties-sagemaker-endpoint-autorollbackconfig"></a>

Currently, the `AutoRollbackConfig` API is not supported\.

## Syntax<a name="aws-properties-sagemaker-endpoint-autorollbackconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-autorollbackconfig-syntax.json"></a>

```
{
  "[Alarms](#cfn-sagemaker-endpoint-autorollbackconfig-alarms)" : [ Alarm, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-autorollbackconfig-syntax.yaml"></a>

```
  [Alarms](#cfn-sagemaker-endpoint-autorollbackconfig-alarms): 
    - Alarm
```

## Properties<a name="aws-properties-sagemaker-endpoint-autorollbackconfig-properties"></a>

`Alarms`  <a name="cfn-sagemaker-endpoint-autorollbackconfig-alarms"></a>
  
*Required*: Yes  
*Type*: List of [Alarm](aws-properties-sagemaker-endpoint-alarm.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
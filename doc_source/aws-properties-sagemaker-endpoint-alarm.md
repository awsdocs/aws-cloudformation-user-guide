# AWS::SageMaker::Endpoint Alarm<a name="aws-properties-sagemaker-endpoint-alarm"></a>

An Amazon CloudWatch alarm configured to monitor metrics on an endpoint\.

## Syntax<a name="aws-properties-sagemaker-endpoint-alarm-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-alarm-syntax.json"></a>

```
{
  "[AlarmName](#cfn-sagemaker-endpoint-alarm-alarmname)" : String
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-alarm-syntax.yaml"></a>

```
  [AlarmName](#cfn-sagemaker-endpoint-alarm-alarmname): String
```

## Properties<a name="aws-properties-sagemaker-endpoint-alarm-properties"></a>

`AlarmName`  <a name="cfn-sagemaker-endpoint-alarm-alarmname"></a>
The name of a CloudWatch alarm in your account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^(?!\s*$).+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
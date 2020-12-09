# AWS::SageMaker::MonitoringSchedule MonitoringInput<a name="aws-properties-sagemaker-monitoringschedule-monitoringinput"></a>

The inputs for a monitoring job\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringinput-syntax.json"></a>

```
{
  "[EndpointInput](#cfn-sagemaker-monitoringschedule-monitoringinput-endpointinput)" : EndpointInput
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringinput-syntax.yaml"></a>

```
  [EndpointInput](#cfn-sagemaker-monitoringschedule-monitoringinput-endpointinput): 
    EndpointInput
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringinput-properties"></a>

`EndpointInput`  <a name="cfn-sagemaker-monitoringschedule-monitoringinput-endpointinput"></a>
The endpoint for a monitoring job\.  
*Required*: Yes  
*Type*: [EndpointInput](aws-properties-sagemaker-monitoringschedule-endpointinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
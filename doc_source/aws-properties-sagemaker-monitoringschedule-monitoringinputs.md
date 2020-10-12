# AWS::SageMaker::MonitoringSchedule MonitoringInputs<a name="aws-properties-sagemaker-monitoringschedule-monitoringinputs"></a>

The array of inputs for the monitoring job\. Currently we support monitoring a sagemaker endpoint\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringinputs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringinputs-syntax.json"></a>

```
{
  "[MonitoringInputs](#cfn-sagemaker-monitoringschedule-monitoringinputs-monitoringinputs)" : [ MonitoringInput, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringinputs-syntax.yaml"></a>

```
  [MonitoringInputs](#cfn-sagemaker-monitoringschedule-monitoringinputs-monitoringinputs): 
    - MonitoringInput
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringinputs-properties"></a>

`MonitoringInputs`  <a name="cfn-sagemaker-monitoringschedule-monitoringinputs-monitoringinputs"></a>
The array of inputs for the monitoring job\. Currently we support monitoring a SageMaker endpoint\.  
*Required*: No  
*Type*: [List](#aws-properties-sagemaker-monitoringschedule-monitoringinputs) of [MonitoringInput](aws-properties-sagemaker-monitoringschedule-monitoringinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::SageMaker::Endpoint BlueGreenUpdatePolicy<a name="aws-properties-sagemaker-endpoint-bluegreenupdatepolicy"></a>

Currently, the `BlueGreenUpdatePolicy` API is not supported\.

## Syntax<a name="aws-properties-sagemaker-endpoint-bluegreenupdatepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-bluegreenupdatepolicy-syntax.json"></a>

```
{
  "[MaximumExecutionTimeoutInSeconds](#cfn-sagemaker-endpoint-bluegreenupdatepolicy-maximumexecutiontimeoutinseconds)" : Integer,
  "[TerminationWaitInSeconds](#cfn-sagemaker-endpoint-bluegreenupdatepolicy-terminationwaitinseconds)" : Integer,
  "[TrafficRoutingConfiguration](#cfn-sagemaker-endpoint-bluegreenupdatepolicy-trafficroutingconfiguration)" : TrafficRoutingConfig
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-bluegreenupdatepolicy-syntax.yaml"></a>

```
  [MaximumExecutionTimeoutInSeconds](#cfn-sagemaker-endpoint-bluegreenupdatepolicy-maximumexecutiontimeoutinseconds): Integer
  [TerminationWaitInSeconds](#cfn-sagemaker-endpoint-bluegreenupdatepolicy-terminationwaitinseconds): Integer
  [TrafficRoutingConfiguration](#cfn-sagemaker-endpoint-bluegreenupdatepolicy-trafficroutingconfiguration): 
    TrafficRoutingConfig
```

## Properties<a name="aws-properties-sagemaker-endpoint-bluegreenupdatepolicy-properties"></a>

`MaximumExecutionTimeoutInSeconds`  <a name="cfn-sagemaker-endpoint-bluegreenupdatepolicy-maximumexecutiontimeoutinseconds"></a>
  
*Required*: No  
*Type*: Integer  
*Minimum*: `600`  
*Maximum*: `14400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminationWaitInSeconds`  <a name="cfn-sagemaker-endpoint-bluegreenupdatepolicy-terminationwaitinseconds"></a>
  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `3600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficRoutingConfiguration`  <a name="cfn-sagemaker-endpoint-bluegreenupdatepolicy-trafficroutingconfiguration"></a>
  
*Required*: Yes  
*Type*: [TrafficRoutingConfig](aws-properties-sagemaker-endpoint-trafficroutingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
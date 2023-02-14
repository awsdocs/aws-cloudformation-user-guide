# AWS::SageMaker::Endpoint BlueGreenUpdatePolicy<a name="aws-properties-sagemaker-endpoint-bluegreenupdatepolicy"></a>

Update policy for a blue/green deployment\. If this update policy is specified, SageMaker creates a new fleet during the deployment while maintaining the old fleet\. SageMaker flips traffic to the new fleet according to the specified traffic routing configuration\. Only one update policy should be used in the deployment configuration\. If no update policy is specified, SageMaker uses a blue/green deployment strategy with all at once traffic shifting by default\.

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
Maximum execution timeout for the deployment\. Note that the timeout value should be larger than the total waiting time specified in `TerminationWaitInSeconds` and `WaitIntervalInSeconds`\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `600`  
*Maximum*: `14400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminationWaitInSeconds`  <a name="cfn-sagemaker-endpoint-bluegreenupdatepolicy-terminationwaitinseconds"></a>
Additional waiting time in seconds after the completion of an endpoint deployment before terminating the old endpoint fleet\. Default is 0\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `3600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficRoutingConfiguration`  <a name="cfn-sagemaker-endpoint-bluegreenupdatepolicy-trafficroutingconfiguration"></a>
Defines the traffic routing strategy to shift traffic from the old fleet to the new fleet during an endpoint deployment\.  
*Required*: Yes  
*Type*: [TrafficRoutingConfig](aws-properties-sagemaker-endpoint-trafficroutingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
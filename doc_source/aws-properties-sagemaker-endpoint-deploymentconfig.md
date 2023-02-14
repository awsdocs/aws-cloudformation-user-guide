# AWS::SageMaker::Endpoint DeploymentConfig<a name="aws-properties-sagemaker-endpoint-deploymentconfig"></a>

The deployment configuration for an endpoint, which contains the desired deployment strategy and rollback configurations\.

## Syntax<a name="aws-properties-sagemaker-endpoint-deploymentconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-deploymentconfig-syntax.json"></a>

```
{
  "[AutoRollbackConfiguration](#cfn-sagemaker-endpoint-deploymentconfig-autorollbackconfiguration)" : AutoRollbackConfig,
  "[BlueGreenUpdatePolicy](#cfn-sagemaker-endpoint-deploymentconfig-bluegreenupdatepolicy)" : BlueGreenUpdatePolicy
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-deploymentconfig-syntax.yaml"></a>

```
  [AutoRollbackConfiguration](#cfn-sagemaker-endpoint-deploymentconfig-autorollbackconfiguration): 
    AutoRollbackConfig
  [BlueGreenUpdatePolicy](#cfn-sagemaker-endpoint-deploymentconfig-bluegreenupdatepolicy): 
    BlueGreenUpdatePolicy
```

## Properties<a name="aws-properties-sagemaker-endpoint-deploymentconfig-properties"></a>

`AutoRollbackConfiguration`  <a name="cfn-sagemaker-endpoint-deploymentconfig-autorollbackconfiguration"></a>
Automatic rollback configuration for handling endpoint deployment failures and recovery\.  
*Required*: No  
*Type*: [AutoRollbackConfig](aws-properties-sagemaker-endpoint-autorollbackconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlueGreenUpdatePolicy`  <a name="cfn-sagemaker-endpoint-deploymentconfig-bluegreenupdatepolicy"></a>
Update policy for a blue/green deployment\. If this update policy is specified, SageMaker creates a new fleet during the deployment while maintaining the old fleet\. SageMaker flips traffic to the new fleet according to the specified traffic routing configuration\. Only one update policy should be used in the deployment configuration\. If no update policy is specified, SageMaker uses a blue/green deployment strategy with all at once traffic shifting by default\.  
*Required*: Yes  
*Type*: [BlueGreenUpdatePolicy](aws-properties-sagemaker-endpoint-bluegreenupdatepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
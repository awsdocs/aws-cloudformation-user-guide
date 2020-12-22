# AWS::SageMaker::Endpoint DeploymentConfig<a name="aws-properties-sagemaker-endpoint-deploymentconfig"></a>

Currently, the `DeploymentConfig` API is not supported\.

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
  
*Required*: No  
*Type*: [AutoRollbackConfig](aws-properties-sagemaker-endpoint-autorollbackconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlueGreenUpdatePolicy`  <a name="cfn-sagemaker-endpoint-deploymentconfig-bluegreenupdatepolicy"></a>
  
*Required*: Yes  
*Type*: [BlueGreenUpdatePolicy](aws-properties-sagemaker-endpoint-bluegreenupdatepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
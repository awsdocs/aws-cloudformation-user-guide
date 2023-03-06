# AWS::GreengrassV2::Deployment DeploymentConfigurationValidationPolicy<a name="aws-properties-greengrassv2-deployment-deploymentconfigurationvalidationpolicy"></a>

Contains information about how long a component on a core device can validate its configuration updates before it times out\. Components can use the [SubscribeToValidateConfigurationUpdates](https://docs.aws.amazon.com/greengrass/v2/developerguide/interprocess-communication.html#ipc-operation-subscribetovalidateconfigurationupdates) IPC operation to receive notifications when a deployment specifies a configuration update\. Then, components can respond with the [SendConfigurationValidityReport](https://docs.aws.amazon.com/greengrass/v2/developerguide/interprocess-communication.html#ipc-operation-sendconfigurationvalidityreport) IPC operation\. For more information, see the [Create deployments](https://docs.aws.amazon.com/greengrass/v2/developerguide/create-deployments.html) in the *AWS IoT Greengrass V2 Developer Guide*\.

## Syntax<a name="aws-properties-greengrassv2-deployment-deploymentconfigurationvalidationpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-deploymentconfigurationvalidationpolicy-syntax.json"></a>

```
{
  "[TimeoutInSeconds](#cfn-greengrassv2-deployment-deploymentconfigurationvalidationpolicy-timeoutinseconds)" : Integer
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-deploymentconfigurationvalidationpolicy-syntax.yaml"></a>

```
  [TimeoutInSeconds](#cfn-greengrassv2-deployment-deploymentconfigurationvalidationpolicy-timeoutinseconds): Integer
```

## Properties<a name="aws-properties-greengrassv2-deployment-deploymentconfigurationvalidationpolicy-properties"></a>

`TimeoutInSeconds`  <a name="cfn-greengrassv2-deployment-deploymentconfigurationvalidationpolicy-timeoutinseconds"></a>
The amount of time in seconds that a component can validate its configuration updates\. If the validation time exceeds this timeout, then the deployment proceeds for the device\.  
Default: `30`  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
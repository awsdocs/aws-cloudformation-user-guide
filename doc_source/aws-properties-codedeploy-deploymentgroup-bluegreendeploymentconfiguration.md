# AWS::CodeDeploy::DeploymentGroup BlueGreenDeploymentConfiguration<a name="aws-properties-codedeploy-deploymentgroup-bluegreendeploymentconfiguration"></a>

Information about blue/green deployment options for a deployment group\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-syntax.json"></a>

```
{
  "[DeploymentReadyOption](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-deploymentreadyoption)" : DeploymentReadyOption,
  "[GreenFleetProvisioningOption](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-greenfleetprovisioningoption)" : GreenFleetProvisioningOption,
  "[TerminateBlueInstancesOnDeploymentSuccess](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-terminateblueinstancesondeploymentsuccess)" : BlueInstanceTerminationOption
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-syntax.yaml"></a>

```
  [DeploymentReadyOption](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-deploymentreadyoption): 
    DeploymentReadyOption
  [GreenFleetProvisioningOption](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-greenfleetprovisioningoption): 
    GreenFleetProvisioningOption
  [TerminateBlueInstancesOnDeploymentSuccess](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-terminateblueinstancesondeploymentsuccess): 
    BlueInstanceTerminationOption
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-properties"></a>

`DeploymentReadyOption`  <a name="cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-deploymentreadyoption"></a>
Information about the action to take when newly provisioned instances are ready to receive traffic in a blue/green deployment\.  
*Required*: No  
*Type*: [DeploymentReadyOption](aws-properties-codedeploy-deploymentgroup-deploymentreadyoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GreenFleetProvisioningOption`  <a name="cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-greenfleetprovisioningoption"></a>
Information about how instances are provisioned for a replacement environment in a blue/green deployment\.  
*Required*: No  
*Type*: [GreenFleetProvisioningOption](aws-properties-codedeploy-deploymentgroup-greenfleetprovisioningoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminateBlueInstancesOnDeploymentSuccess`  <a name="cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-terminateblueinstancesondeploymentsuccess"></a>
Information about whether to terminate instances in the original fleet during a blue/green deployment\.  
*Required*: No  
*Type*: [BlueInstanceTerminationOption](aws-properties-codedeploy-deploymentgroup-blueinstanceterminationoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
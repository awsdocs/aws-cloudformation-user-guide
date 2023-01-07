# AWS::CodeDeploy::DeploymentGroup AutoRollbackConfiguration<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration"></a>

The `AutoRollbackConfiguration` property type configures automatic rollback for an AWS CodeDeploy deployment group when a deployment is not completed successfully\. For more information, see [Automatic Rollbacks](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployments-rollback-and-redeploy.html#deployments-rollback-and-redeploy-automatic-rollbacks) in the *AWS CodeDeploy User Guide*\.

 `AutoRollbackConfiguration` is a property of the [DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html) resource\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-enabled)" : Boolean,
  "[Events](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-events)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-enabled): Boolean
  [Events](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-events): 
    - String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-properties"></a>

`Enabled`  <a name="cfn-codedeploy-deploymentgroup-autorollbackconfiguration-enabled"></a>
Indicates whether a defined automatic rollback configuration is currently enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Events`  <a name="cfn-codedeploy-deploymentgroup-autorollbackconfiguration-events"></a>
 The event type or types that trigger a rollback\. Valid values are `DEPLOYMENT_FAILURE`, `DEPLOYMENT_STOP_ON_ALARM`, or `DEPLOYMENT_STOP_ON_REQUEST`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
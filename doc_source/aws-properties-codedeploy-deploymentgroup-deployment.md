# AWS CodeDeploy DeploymentGroup Deployment<a name="aws-properties-codedeploy-deploymentgroup-deployment"></a>

`Deployment` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource that specifies an AWS CodeDeploy application revision to be deployed to instances in the deployment group\. If you specify an application revision, your target revision will be deployed as soon as the provisioning process is complete\.

## Syntax<a name="w3ab2c21c14d399b5"></a>

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deployment-syntax.json"></a>

```
{
  "[Description](#cfn-properties-codedeploy-deploymentgroup-deployment-description)" : String,
  "[IgnoreApplicationStopFailures](#cfn-properties-codedeploy-deploymentgroup-deployment-ignoreapplicationstopfailures)" : Boolean,
  "[Revision](#cfn-properties-codedeploy-deploymentgroup-deployment-revision)" : Revision
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deployment-syntax.yaml"></a>

```
[Description](#cfn-properties-codedeploy-deploymentgroup-deployment-description): String
[IgnoreApplicationStopFailures](#cfn-properties-codedeploy-deploymentgroup-deployment-ignoreapplicationstopfailures): Boolean
[Revision](#cfn-properties-codedeploy-deploymentgroup-deployment-revision):
  Revision
```

## Properties<a name="w3ab2c21c14d399b7"></a>

`Description`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-description"></a>
A description about this deployment\.  
*Required*: No  
*Type*: String

`IgnoreApplicationStopFailures`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-ignoreapplicationstopfailures"></a>
Whether to continue the deployment if the `ApplicationStop` deployment lifecycle event fails\. If you want AWS CodeDeploy to continue the deployment lifecycle even if the `ApplicationStop` event fails on an instance, specify `true`\. The deployment continues to the `BeforeInstall` deployment lifecycle event\. If you want AWS CodeDeploy to stop deployment on the instance if the `ApplicationStop` event fails, specify `false` or do not specify a value\.  
*Required*: No  
*Type*: Boolean

`Revision`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision"></a>
The location of the application revision to deploy\.  
*Required*: Yes  
*Type*: [AWS CodeDeploy DeploymentGroup Deployment Revision](aws-properties-codedeploy-deploymentgroup-deployment-revision.md)
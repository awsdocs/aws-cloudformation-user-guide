# AWS::CodeDeploy::DeploymentGroup Deployment<a name="aws-properties-codedeploy-deploymentgroup-deployment"></a>

 `Deployment` is a property of the [DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html) resource that specifies an AWS CodeDeploy application revision to be deployed to instances in the deployment group\. If you specify an application revision, your target revision is deployed as soon as the provisioning process is complete\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-deployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deployment-syntax.json"></a>

```
{
  "[Description](#cfn-properties-codedeploy-deploymentgroup-deployment-description)" : String,
  "[IgnoreApplicationStopFailures](#cfn-properties-codedeploy-deploymentgroup-deployment-ignoreapplicationstopfailures)" : Boolean,
  "[Revision](#cfn-properties-codedeploy-deploymentgroup-deployment-revision)" : RevisionLocation
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deployment-syntax.yaml"></a>

```
  [Description](#cfn-properties-codedeploy-deploymentgroup-deployment-description): String
  [IgnoreApplicationStopFailures](#cfn-properties-codedeploy-deploymentgroup-deployment-ignoreapplicationstopfailures): Boolean
  [Revision](#cfn-properties-codedeploy-deploymentgroup-deployment-revision): 
    RevisionLocation
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-deployment-properties"></a>

`Description`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-description"></a>
A comment about the deployment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IgnoreApplicationStopFailures`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-ignoreapplicationstopfailures"></a>
 If true, then if an `ApplicationStop`, `BeforeBlockTraffic`, or `AfterBlockTraffic` deployment lifecycle event to an instance fails, then the deployment continues to the next deployment lifecycle event\. For example, if `ApplicationStop` fails, the deployment continues with DownloadBundle\. If `BeforeBlockTraffic` fails, the deployment continues with `BlockTraffic`\. If `AfterBlockTraffic` fails, the deployment continues with `ApplicationStop`\.   
 If false or not specified, then if a lifecycle event fails during a deployment to an instance, that deployment fails\. If deployment to that instance is part of an overall deployment and the number of healthy hosts is not less than the minimum number of healthy hosts, then a deployment to the next instance is attempted\.   
 During a deployment, the AWS CodeDeploy agent runs the scripts specified for `ApplicationStop`, `BeforeBlockTraffic`, and `AfterBlockTraffic` in the AppSpec file from the previous successful deployment\. \(All other scripts are run from the AppSpec file in the current deployment\.\) If one of these scripts contains an error and does not run successfully, the deployment can fail\.   
 If the cause of the failure is a script from the last successful deployment that will never run successfully, create a new deployment and use `ignoreApplicationStopFailures` to specify that the `ApplicationStop`, `BeforeBlockTraffic`, and `AfterBlockTraffic` failures should be ignored\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Revision`  <a name="cfn-properties-codedeploy-deploymentgroup-deployment-revision"></a>
Information about the location of stored application artifacts and the service from which to retrieve them\.  
*Required*: Yes  
*Type*: [RevisionLocation](aws-properties-codedeploy-deploymentgroup-deployment-revision.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
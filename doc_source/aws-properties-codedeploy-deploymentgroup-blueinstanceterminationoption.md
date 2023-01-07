# AWS::CodeDeploy::DeploymentGroup BlueInstanceTerminationOption<a name="aws-properties-codedeploy-deploymentgroup-blueinstanceterminationoption"></a>

Information about whether instances in the original environment are terminated when a blue/green deployment is successful\. `BlueInstanceTerminationOption` does not apply to Lambda deployments\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-blueinstanceterminationoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-blueinstanceterminationoption-syntax.json"></a>

```
{
  "[Action](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-blueinstanceterminationoption-action)" : String,
  "[TerminationWaitTimeInMinutes](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-blueinstanceterminationoption-terminationwaittimeinminutes)" : Integer
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-blueinstanceterminationoption-syntax.yaml"></a>

```
  [Action](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-blueinstanceterminationoption-action): String
  [TerminationWaitTimeInMinutes](#cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-blueinstanceterminationoption-terminationwaittimeinminutes): Integer
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-blueinstanceterminationoption-properties"></a>

`Action`  <a name="cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-blueinstanceterminationoption-action"></a>
The action to take on instances in the original environment after a successful blue/green deployment\.  
+  `TERMINATE`: Instances are terminated after a specified wait time\.
+  `KEEP_ALIVE`: Instances are left running after they are deregistered from the load balancer and removed from the deployment group\.
*Required*: No  
*Type*: String  
*Allowed values*: `KEEP_ALIVE | TERMINATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminationWaitTimeInMinutes`  <a name="cfn-codedeploy-deploymentgroup-bluegreendeploymentconfiguration-blueinstanceterminationoption-terminationwaittimeinminutes"></a>
For an Amazon EC2 deployment, the number of minutes to wait after a successful blue/green deployment before terminating instances from the original environment\.  
 For an Amazon ECS deployment, the number of minutes before deleting the original \(blue\) task set\. During an Amazon ECS deployment, CodeDeploy shifts traffic from the original \(blue\) task set to a replacement \(green\) task set\.   
 The maximum setting is 2880 minutes \(2 days\)\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
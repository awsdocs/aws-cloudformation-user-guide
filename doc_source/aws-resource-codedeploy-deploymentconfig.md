# AWS::CodeDeploy::DeploymentConfig<a name="aws-resource-codedeploy-deploymentconfig"></a>

The `AWS::CodeDeploy::DeploymentConfig` resource creates a set of deployment rules, deployment success conditions, and deployment failure conditions that AWS CodeDeploy uses during a deployment\. The deployment configuration specifies, through the use of a `MinimumHealthyHosts` value, the number or percentage of instances that must remain available at any time during a deployment\.

**Topics**
+ [Syntax](#aws-resource-codedeploy-deploymentconfig-syntax)
+ [Properties](#w3ab2c21c10d254b9)
+ [Return Value](#w3ab2c21c10d254c11)
+ [Example](#w3ab2c21c10d254c13)

## Syntax<a name="aws-resource-codedeploy-deploymentconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codedeploy-deploymentconfig-syntax.json"></a>

```
{
  "Type" : "AWS::CodeDeploy::DeploymentConfig",
  "Properties" : {
    "[DeploymentConfigName](#cfn-codedeploy-deploymentconfig-deploymentconfigname)" : String,
    "[MinimumHealthyHosts](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts)" : MinimumHealthyHosts
  }
}
```

### YAML<a name="aws-resource-codedeploy-deploymentconfig-syntax.yaml"></a>

```
Type: "AWS::CodeDeploy::DeploymentConfig"
Properties:
  [DeploymentConfigName](#cfn-codedeploy-deploymentconfig-deploymentconfigname): String
  [MinimumHealthyHosts](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts):
    MinimumHealthyHosts
```

## Properties<a name="w3ab2c21c10d254b9"></a>

`DeploymentConfigName`  <a name="cfn-codedeploy-deploymentconfig-deploymentconfigname"></a>
A name for the deployment configuration\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the deployment configuration name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MinimumHealthyHosts`  <a name="cfn-codedeploy-deploymentconfig-minimumhealthyhosts"></a>
The minimum number of healthy instances that must be available at any time during an AWS CodeDeploy deployment\. For example, for a fleet of nine instances, if you specify a minimum of six healthy instances, AWS CodeDeploy deploys your application up to three instances at a time so that you always have six healthy instances\. The deployment succeeds if your application successfully deploys to six or more instances; otherwise, the deployment fails\.  
For more information about instance health, see [AWS CodeDeploy Instance Health](http://docs.aws.amazon.com/codedeploy/latest/userguide/host-health.html) in the *AWS CodeDeploy User Guide*\.  
*Required*: Yes  
*Type*: [AWS CodeDeploy DeploymentConfig MinimumHealthyHosts](aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d254c11"></a>

### Ref<a name="w3ab2c21c10d254c11b2"></a>

When you pass the logical ID of an `AWS::CodeDeploy::DeploymentConfig` resource to the intrinsic `Ref` function, the function returns the deployment configuration name, such as `mydeploymentconfig-a123d0d1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d254c13"></a>

The following example requires at least 75% of the fleet to be healthy\. For example, if you had a fleet of four instances, the deployment proceeds one instance at a time\.

### JSON<a name="aws-resource-codedeploy-deploymentconfig-example.json"></a>

```
"TwentyFivePercentAtATime" : {
  "Type" : "AWS::CodeDeploy::DeploymentConfig",
  "Properties" : {
    "MinimumHealthyHosts" : {
      "Type" : "FLEET_PERCENT",
      "Value" : "75"
    }
  }
}
```

### YAML<a name="aws-resource-codedeploy-deploymentconfig-example.yaml"></a>

```
TwentyFivePercentAtATime: 
  Type: "AWS::CodeDeploy::DeploymentConfig"
  Properties: 
    MinimumHealthyHosts: 
      Type: "FLEET_PERCENT"
      Value: 75
```
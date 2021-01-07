# AWS::CodeDeploy::DeploymentConfig<a name="aws-resource-codedeploy-deploymentconfig"></a>

 The `AWS::CodeDeploy::DeploymentConfig` resource creates a set of deployment rules, deployment success conditions, and deployment failure conditions that AWS CodeDeploy uses during a deployment\. The deployment configuration specifies, through the use of a `MinimumHealthyHosts` value, the number or percentage of instances that must remain available at any time during a deployment\. 

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
Type: AWS::CodeDeploy::DeploymentConfig
Properties: 
  [DeploymentConfigName](#cfn-codedeploy-deploymentconfig-deploymentconfigname): String
  [MinimumHealthyHosts](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts): 
    MinimumHealthyHosts
```

## Properties<a name="aws-resource-codedeploy-deploymentconfig-properties"></a>

`DeploymentConfigName`  <a name="cfn-codedeploy-deploymentconfig-deploymentconfigname"></a>
 A name for the deployment configuration\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the deployment configuration name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.   
 If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinimumHealthyHosts`  <a name="cfn-codedeploy-deploymentconfig-minimumhealthyhosts"></a>
The minimum number of healthy instances that should be available at any time during the deployment\. There are two parameters expected in the input: type and value\.  
The type parameter takes either of the following values:  
+ HOST\_COUNT: The value parameter represents the minimum number of healthy instances as an absolute value\.
+ FLEET\_PERCENT: The value parameter represents the minimum number of healthy instances as a percentage of the total number of instances in the deployment\. If you specify FLEET\_PERCENT, at the start of the deployment, AWS CodeDeploy converts the percentage to the equivalent number of instance and rounds up fractional instances\.
The value parameter takes an integer\.  
For example, to set a minimum of 95% healthy instance, specify a type of FLEET\_PERCENT and a value of 95\.  
 For more information about instance health, see [CodeDeploy Instance Health](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-health.html) in the AWS CodeDeploy User Guide\.   
*Required*: No  
*Type*: [MinimumHealthyHosts](aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-codedeploy-deploymentconfig-return-values"></a>

### Ref<a name="aws-resource-codedeploy-deploymentconfig-return-values-ref"></a>

When you pass the logical ID of an `AWS::CodeDeploy::DeploymentConfig` resource to the intrinsic `Ref` function, the function returns the deployment configuration name, such as `mydeploymentconfig-a123d0d1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-codedeploy-deploymentconfig--examples"></a>



### Specifying minimum healthy hosts<a name="aws-resource-codedeploy-deploymentconfig--examples--Specifying_minimum_healthy_hosts"></a>

The following example requires at least 75% of the fleet to be healthy\. For example, if you had a fleet of four instances, the deployment proceeds one instance at a time\.

#### JSON<a name="aws-resource-codedeploy-deploymentconfig--examples--Specifying_minimum_healthy_hosts--json"></a>

```
"TwentyFivePercentAtATime" : {
  "Type" : "AWS::CodeDeploy::DeploymentConfig",
  "Properties" : {
    "MinimumHealthyHosts" : {
      "Type" : "FLEET_PERCENT",
      "Value" : 75
    }
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentconfig--examples--Specifying_minimum_healthy_hosts--yaml"></a>

```
TwentyFivePercentAtATime: 
  Type: AWS::CodeDeploy::DeploymentConfig
  Properties: 
    MinimumHealthyHosts: 
      Type: "FLEET_PERCENT"
      Value: 75
```
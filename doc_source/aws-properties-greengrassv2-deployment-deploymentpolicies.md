# AWS::GreengrassV2::Deployment DeploymentPolicies<a name="aws-properties-greengrassv2-deployment-deploymentpolicies"></a>

Contains information about policies that define how a deployment updates components and handles failure\.

## Syntax<a name="aws-properties-greengrassv2-deployment-deploymentpolicies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-deploymentpolicies-syntax.json"></a>

```
{
  "[ComponentUpdatePolicy](#cfn-greengrassv2-deployment-deploymentpolicies-componentupdatepolicy)" : DeploymentComponentUpdatePolicy,
  "[ConfigurationValidationPolicy](#cfn-greengrassv2-deployment-deploymentpolicies-configurationvalidationpolicy)" : DeploymentConfigurationValidationPolicy,
  "[FailureHandlingPolicy](#cfn-greengrassv2-deployment-deploymentpolicies-failurehandlingpolicy)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-deploymentpolicies-syntax.yaml"></a>

```
  [ComponentUpdatePolicy](#cfn-greengrassv2-deployment-deploymentpolicies-componentupdatepolicy): 
    DeploymentComponentUpdatePolicy
  [ConfigurationValidationPolicy](#cfn-greengrassv2-deployment-deploymentpolicies-configurationvalidationpolicy): 
    DeploymentConfigurationValidationPolicy
  [FailureHandlingPolicy](#cfn-greengrassv2-deployment-deploymentpolicies-failurehandlingpolicy): String
```

## Properties<a name="aws-properties-greengrassv2-deployment-deploymentpolicies-properties"></a>

`ComponentUpdatePolicy`  <a name="cfn-greengrassv2-deployment-deploymentpolicies-componentupdatepolicy"></a>
The component update policy for the configuration deployment\. This policy defines when it's safe to deploy the configuration to devices\.  
*Required*: No  
*Type*: [DeploymentComponentUpdatePolicy](aws-properties-greengrassv2-deployment-deploymentcomponentupdatepolicy.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationValidationPolicy`  <a name="cfn-greengrassv2-deployment-deploymentpolicies-configurationvalidationpolicy"></a>
The configuration validation policy for the configuration deployment\. This policy defines how long each component has to validate its configure updates\.  
*Required*: No  
*Type*: [DeploymentConfigurationValidationPolicy](aws-properties-greengrassv2-deployment-deploymentconfigurationvalidationpolicy.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FailureHandlingPolicy`  <a name="cfn-greengrassv2-deployment-deploymentpolicies-failurehandlingpolicy"></a>
The failure handling policy for the configuration deployment\. This policy defines what to do if the deployment fails\.  
Default: `ROLLBACK`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
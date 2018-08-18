# AWS CodeDeploy DeploymentConfig MinimumHealthyHosts<a name="aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts"></a>

`MinimumHealthyHosts` is a property of the [AWS::CodeDeploy::DeploymentConfig](aws-resource-codedeploy-deploymentconfig.md) resource that defines how many instances must remain healthy during an AWS CodeDeploy deployment\.

## Syntax<a name="w3ab2c21c14d385b5"></a>

### JSON<a name="aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts-syntax.json"></a>

```
{
  "[Type](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-type)" : String,
  "[Value](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-value)" : Integer
}
```

### YAML<a name="aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts-syntax.yaml"></a>

```
[Type](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-type): String
[Value](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-value): Integer
```

## Properties<a name="w3ab2c21c14d385b7"></a>

`Type`  <a name="cfn-codedeploy-deploymentconfig-minimumhealthyhosts-type"></a>
The type of count to use, such as an absolute value or a percentage of the total number of instances in the deployment\. For valid values, see [MinimumHealthyHosts](http://docs.aws.amazon.com/codedeploy/latest/APIReference/API_MinimumHealthyHosts.html) in the *AWS CodeDeploy API Reference*\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-codedeploy-deploymentconfig-minimumhealthyhosts-value"></a>
The minimum number of healthy instances\.  
*Required*: Yes  
*Type*: Integer
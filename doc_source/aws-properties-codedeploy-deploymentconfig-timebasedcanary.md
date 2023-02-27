# AWS::CodeDeploy::DeploymentConfig TimeBasedCanary<a name="aws-properties-codedeploy-deploymentconfig-timebasedcanary"></a>

A configuration that shifts traffic from one version of a Lambda function or Amazon ECS task set to another in two increments\. The original and target Lambda function versions or ECS task sets are specified in the deployment's AppSpec file\.

## Syntax<a name="aws-properties-codedeploy-deploymentconfig-timebasedcanary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentconfig-timebasedcanary-syntax.json"></a>

```
{
  "[CanaryInterval](#cfn-codedeploy-deploymentconfig-timebasedcanary-canaryinterval)" : Integer,
  "[CanaryPercentage](#cfn-codedeploy-deploymentconfig-timebasedcanary-canarypercentage)" : Integer
}
```

### YAML<a name="aws-properties-codedeploy-deploymentconfig-timebasedcanary-syntax.yaml"></a>

```
  [CanaryInterval](#cfn-codedeploy-deploymentconfig-timebasedcanary-canaryinterval): Integer
  [CanaryPercentage](#cfn-codedeploy-deploymentconfig-timebasedcanary-canarypercentage): Integer
```

## Properties<a name="aws-properties-codedeploy-deploymentconfig-timebasedcanary-properties"></a>

`CanaryInterval`  <a name="cfn-codedeploy-deploymentconfig-timebasedcanary-canaryinterval"></a>
The number of minutes between the first and second traffic shifts of a `TimeBasedCanary` deployment\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CanaryPercentage`  <a name="cfn-codedeploy-deploymentconfig-timebasedcanary-canarypercentage"></a>
The percentage of traffic to shift in the first increment of a `TimeBasedCanary` deployment\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
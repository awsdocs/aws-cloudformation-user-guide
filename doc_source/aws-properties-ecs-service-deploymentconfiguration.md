# Amazon Elastic Container Service Service DeploymentConfiguration<a name="aws-properties-ecs-service-deploymentconfiguration"></a>

`DeploymentConfiguration` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource that configures how many tasks run when you update a running Amazon Elastic Container Service \(Amazon ECS\) service\.

## Syntax<a name="w3ab2c21c14d837b5"></a>

### JSON<a name="aws-properties-ecs-service-deploymentconfiguration-syntax.json"></a>

```
{
  "[MaximumPercent](#cfn-ecs-service-deploymentconfiguration-maximumpercent)" : Integer,
  "[MinimumHealthyPercent](#cfn-ecs-service-deploymentconfiguration-minimumhealthypercent)" : Integer
}
```

### YAML<a name="aws-properties-ecs-service-deploymentconfiguration-syntax.yaml"></a>

```
[MaximumPercent](#cfn-ecs-service-deploymentconfiguration-maximumpercent): Integer
[MinimumHealthyPercent](#cfn-ecs-service-deploymentconfiguration-minimumhealthypercent): Integer
```

## Properties<a name="w3ab2c21c14d837b7"></a>

`MaximumPercent`  <a name="cfn-ecs-service-deploymentconfiguration-maximumpercent"></a>
The maximum number of tasks, specified as a percentage of the Amazon ECS service's `DesiredCount` value, that can run in a service during a deployment\. To calculate the maximum number of tasks, Amazon ECS uses this formula: the value of `DesiredCount` \* \(the value of the `MaximumPercent`/100\), rounded down to the nearest integer value\.  
*Required*: No  
*Type*: Integer

`MinimumHealthyPercent`  <a name="cfn-ecs-service-deploymentconfiguration-minimumhealthypercent"></a>
The minimum number of tasks, specified as a percentage of the Amazon ECS service's `DesiredCount` value, that must continue to run and remain healthy during a deployment\. To calculate the minimum number of tasks, Amazon ECS uses this formula: the value of `DesiredCount` \* \(the value of the `MinimumHealthyPercent`/100\), rounded up to the nearest integer value\.  
*Required*: No  
*Type*: Integer
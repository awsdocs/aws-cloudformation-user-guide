# AWS::ECS::Service DeploymentCircuitBreaker<a name="aws-properties-ecs-service-deploymentcircuitbreaker"></a>

**Note**  
The deployment circuit breaker can only be used for services using the rolling update \(`ECS`\) deployment type\.

The `DeploymentCircuitBreaker` property determines whether a service deployment will fail if the service can't reach a steady state\. If deployment circuit breaker is enabled, a service deployment will transition to a failed state and stop launching new tasks\. If rollback is enabled, when a service deployment fails, the service is rolled back to the last deployment that completed successfully\.

## Syntax<a name="aws-properties-ecs-service-deploymentcircuitbreaker-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-deploymentcircuitbreaker-syntax.json"></a>

```
{
  "[Enable](#cfn-ecs-service-deploymentcircuitbreaker-enable)" : Boolean,
  "[Rollback](#cfn-ecs-service-deploymentcircuitbreaker-rollback)" : Boolean
}
```

### YAML<a name="aws-properties-ecs-service-deploymentcircuitbreaker-syntax.yaml"></a>

```
  [Enable](#cfn-ecs-service-deploymentcircuitbreaker-enable): Boolean
  [Rollback](#cfn-ecs-service-deploymentcircuitbreaker-rollback): Boolean
```

## Properties<a name="aws-properties-ecs-service-deploymentcircuitbreaker-properties"></a>

`Enable`  <a name="cfn-ecs-service-deploymentcircuitbreaker-enable"></a>
Whether to enable the deployment circuit breaker logic for the service\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rollback`  <a name="cfn-ecs-service-deploymentcircuitbreaker-rollback"></a>
Whether to enable Amazon ECS to roll back the service if a service deployment fails\. If rollback is enabled, when a service deployment fails, the service is rolled back to the last deployment that completed successfully\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
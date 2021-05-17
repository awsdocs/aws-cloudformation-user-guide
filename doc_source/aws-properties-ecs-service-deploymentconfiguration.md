# AWS::ECS::Service DeploymentConfiguration<a name="aws-properties-ecs-service-deploymentconfiguration"></a>

The `DeploymentConfiguration` property specifies optional deployment parameters that control how many tasks run during the deployment and the ordering of stopping and starting tasks\.

## Syntax<a name="aws-properties-ecs-service-deploymentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-deploymentconfiguration-syntax.json"></a>

```
{
  "[DeploymentCircuitBreaker](#cfn-ecs-service-deploymentconfiguration-deploymentcircuitbreaker)" : DeploymentCircuitBreaker,
  "[MaximumPercent](#cfn-ecs-service-deploymentconfiguration-maximumpercent)" : Integer,
  "[MinimumHealthyPercent](#cfn-ecs-service-deploymentconfiguration-minimumhealthypercent)" : Integer
}
```

### YAML<a name="aws-properties-ecs-service-deploymentconfiguration-syntax.yaml"></a>

```
  [DeploymentCircuitBreaker](#cfn-ecs-service-deploymentconfiguration-deploymentcircuitbreaker): 
    DeploymentCircuitBreaker
  [MaximumPercent](#cfn-ecs-service-deploymentconfiguration-maximumpercent): Integer
  [MinimumHealthyPercent](#cfn-ecs-service-deploymentconfiguration-minimumhealthypercent): Integer
```

## Properties<a name="aws-properties-ecs-service-deploymentconfiguration-properties"></a>

`DeploymentCircuitBreaker`  <a name="cfn-ecs-service-deploymentconfiguration-deploymentcircuitbreaker"></a>
The deployment circuit breaker can only be used for services using the rolling update \(`ECS`\) deployment type that are not behind a Classic Load Balancer\.
The **deployment circuit breaker** determines whether a service deployment will fail if the service can't reach a steady state\. If enabled, a service deployment will transition to a failed state and stop launching new tasks\. You can also enable Amazon ECS to roll back your service to the last completed deployment after a failure\. For more information, see [Rolling update](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-type-ecs.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: [DeploymentCircuitBreaker](aws-properties-ecs-service-deploymentcircuitbreaker.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumPercent`  <a name="cfn-ecs-service-deploymentconfiguration-maximumpercent"></a>
If a service is using the rolling update \(`ECS`\) deployment type, the **maximum percent** parameter represents an upper limit on the number of tasks in a service that are allowed in the `RUNNING` or `PENDING` state during a deployment, as a percentage of the desired number of tasks \(rounded down to the nearest integer\), and while any container instances are in the `DRAINING` state if the service contains tasks using the EC2 launch type\. This parameter enables you to define the deployment batch size\. For example, if your service has a desired number of four tasks and a maximum percent value of 200%, the scheduler may start four new tasks before stopping the four older tasks \(provided that the cluster resources required to do this are available\)\. The default value for maximum percent is 200%\.  
If a service is using the blue/green \(`CODE_DEPLOY`\) or `EXTERNAL` deployment types and tasks that use the EC2 launch type, the **maximum percent** value is set to the default value and is used to define the upper limit on the number of the tasks in the service that remain in the `RUNNING` state while the container instances are in the `DRAINING` state\. If the tasks in the service use the Fargate launch type, the maximum percent value is not used, although it is returned when describing your service\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumHealthyPercent`  <a name="cfn-ecs-service-deploymentconfiguration-minimumhealthypercent"></a>
If a service is using the rolling update \(`ECS`\) deployment type, the **minimum healthy percent** represents a lower limit on the number of tasks in a service that must remain in the `RUNNING` state during a deployment, as a percentage of the desired number of tasks \(rounded up to the nearest integer\), and while any container instances are in the `DRAINING` state if the service contains tasks using the EC2 launch type\. This parameter enables you to deploy without using additional cluster capacity\. For example, if your service has a desired number of four tasks and a minimum healthy percent of 50%, the scheduler may stop two existing tasks to free up cluster capacity before starting two new tasks\. Tasks for services that *do not* use a load balancer are considered healthy if they are in the `RUNNING` state; tasks for services that *do* use a load balancer are considered healthy if they are in the `RUNNING` state and they are reported as healthy by the load balancer\. The default value for minimum healthy percent is 100%\.  
If a service is using the blue/green \(`CODE_DEPLOY`\) or `EXTERNAL` deployment types and tasks that use the EC2 launch type, the **minimum healthy percent** value is set to the default value and is used to define the lower limit on the number of the tasks in the service that remain in the `RUNNING` state while the container instances are in the `DRAINING` state\. If the tasks in the service use the Fargate launch type, the minimum healthy percent value is not used, although it is returned when describing your service\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
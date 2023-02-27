# AWS::ECS::Service DeploymentConfiguration<a name="aws-properties-ecs-service-deploymentconfiguration"></a>

The `DeploymentConfiguration` property specifies optional deployment parameters that control how many tasks run during the deployment and the ordering of stopping and starting tasks\.

## Syntax<a name="aws-properties-ecs-service-deploymentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-deploymentconfiguration-syntax.json"></a>

```
{
  "[Alarms](#cfn-ecs-service-deploymentconfiguration-alarms)" : DeploymentAlarms,
  "[DeploymentCircuitBreaker](#cfn-ecs-service-deploymentconfiguration-deploymentcircuitbreaker)" : DeploymentCircuitBreaker,
  "[MaximumPercent](#cfn-ecs-service-deploymentconfiguration-maximumpercent)" : Integer,
  "[MinimumHealthyPercent](#cfn-ecs-service-deploymentconfiguration-minimumhealthypercent)" : Integer
}
```

### YAML<a name="aws-properties-ecs-service-deploymentconfiguration-syntax.yaml"></a>

```
  [Alarms](#cfn-ecs-service-deploymentconfiguration-alarms): 
    DeploymentAlarms
  [DeploymentCircuitBreaker](#cfn-ecs-service-deploymentconfiguration-deploymentcircuitbreaker): 
    DeploymentCircuitBreaker
  [MaximumPercent](#cfn-ecs-service-deploymentconfiguration-maximumpercent): Integer
  [MinimumHealthyPercent](#cfn-ecs-service-deploymentconfiguration-minimumhealthypercent): Integer
```

## Properties<a name="aws-properties-ecs-service-deploymentconfiguration-properties"></a>

`Alarms`  <a name="cfn-ecs-service-deploymentconfiguration-alarms"></a>
Information about the CloudWatch alarms\.  
*Required*: No  
*Type*: [DeploymentAlarms](aws-properties-ecs-service-deploymentalarms.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentCircuitBreaker`  <a name="cfn-ecs-service-deploymentconfiguration-deploymentcircuitbreaker"></a>
The deployment circuit breaker can only be used for services using the rolling update \(`ECS`\) deployment type\.
The **deployment circuit breaker** determines whether a service deployment will fail if the service can't reach a steady state\. If you use the deployment circuit breaker, a service deployment will transition to a failed state and stop launching new tasks\. If you use the rollback option, when a service deployment fails, the service is rolled back to the last deployment that completed successfully\. For more information, see [Rolling update](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-type-ecs.html) in the *Amazon Elastic Container Service Developer Guide*   
*Required*: No  
*Type*: [DeploymentCircuitBreaker](aws-properties-ecs-service-deploymentcircuitbreaker.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumPercent`  <a name="cfn-ecs-service-deploymentconfiguration-maximumpercent"></a>
If a service is using the rolling update \(`ECS`\) deployment type, the `maximumPercent` parameter represents an upper limit on the number of your service's tasks that are allowed in the `RUNNING` or `PENDING` state during a deployment, as a percentage of the `desiredCount` \(rounded down to the nearest integer\)\. This parameter enables you to define the deployment batch size\. For example, if your service is using the `REPLICA` service scheduler and has a `desiredCount` of four tasks and a `maximumPercent` value of 200%, the scheduler may start four new tasks before stopping the four older tasks \(provided that the cluster resources required to do this are available\)\. The default `maximumPercent` value for a service using the `REPLICA` service scheduler is 200%\.  
If a service is using either the blue/green \(`CODE_DEPLOY`\) or `EXTERNAL` deployment types and tasks that use the EC2 launch type, the **maximum percent** value is set to the default value and is used to define the upper limit on the number of the tasks in the service that remain in the `RUNNING` state while the container instances are in the `DRAINING` state\. If the tasks in the service use the Fargate launch type, the maximum percent value is not used, although it is returned when describing your service\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumHealthyPercent`  <a name="cfn-ecs-service-deploymentconfiguration-minimumhealthypercent"></a>
If a service is using the rolling update \(`ECS`\) deployment type, the `minimumHealthyPercent` represents a lower limit on the number of your service's tasks that must remain in the `RUNNING` state during a deployment, as a percentage of the `desiredCount` \(rounded up to the nearest integer\)\. This parameter enables you to deploy without using additional cluster capacity\. For example, if your service has a `desiredCount` of four tasks and a `minimumHealthyPercent` of 50%, the service scheduler may stop two existing tasks to free up cluster capacity before starting two new tasks\.   
For services that *do not* use a load balancer, the following should be noted:  
+ A service is considered healthy if all essential containers within the tasks in the service pass their health checks\.
+ If a task has no essential containers with a health check defined, the service scheduler will wait for 40 seconds after a task reaches a `RUNNING` state before the task is counted towards the minimum healthy percent total\.
+ If a task has one or more essential containers with a health check defined, the service scheduler will wait for the task to reach a healthy status before counting it towards the minimum healthy percent total\. A task is considered healthy when all essential containers within the task have passed their health checks\. The amount of time the service scheduler can wait for is determined by the container health check settings\. 
For services are that *do* use a load balancer, the following should be noted:  
+ If a task has no essential containers with a health check defined, the service scheduler will wait for the load balancer target group health check to return a healthy status before counting the task towards the minimum healthy percent total\.
+ If a task has an essential container with a health check defined, the service scheduler will wait for both the task to reach a healthy status and the load balancer target group health check to return a healthy status before counting the task towards the minimum healthy percent total\.
If a service is using either the blue/green \(`CODE_DEPLOY`\) or `EXTERNAL` deployment types and is running tasks that use the EC2 launch type, the **minimum healthy percent** value is set to the default value and is used to define the lower limit on the number of the tasks in the service that remain in the `RUNNING` state while the container instances are in the `DRAINING` state\. If a service is using either the blue/green \(`CODE_DEPLOY`\) or `EXTERNAL` deployment types and is running tasks that use the Fargate launch type, the minimum healthy percent value is not used, although it is returned when describing your service\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
# AWS::ECS::TaskDefinition HealthCheck<a name="aws-properties-ecs-taskdefinition-healthcheck"></a>

The `HealthCheck` property specifies an object representing a container health check\. Health check parameters that are specified in a container definition override any Docker health checks that exist in the container image \(such as those specified in a parent image or from the image's Dockerfile\)\.

The following are notes about container health check support:
+ Container health checks require version 1\.17\.0 or greater of the Amazon ECS container agent\. For more information, see [Updating the Amazon ECS Container Agent](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-agent-update.html)\.
+ Container health checks are supported for Fargate tasks if you are using platform version 1\.1\.0 or greater\. For more information, see [AWS Fargate Platform Versions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/platform_versions.html)\.
+ Container health checks are not supported for tasks that are part of a service that is configured to use a Classic Load Balancer\.

## Syntax<a name="aws-properties-ecs-taskdefinition-healthcheck-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-healthcheck-syntax.json"></a>

```
{
  "[Command](#cfn-ecs-taskdefinition-healthcheck-command)" : [ String, ... ],
  "[Interval](#cfn-ecs-taskdefinition-healthcheck-interval)" : Integer,
  "[Retries](#cfn-ecs-taskdefinition-healthcheck-retries)" : Integer,
  "[StartPeriod](#cfn-ecs-taskdefinition-healthcheck-startperiod)" : Integer,
  "[Timeout](#cfn-ecs-taskdefinition-healthcheck-timeout)" : Integer
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-healthcheck-syntax.yaml"></a>

```
  [Command](#cfn-ecs-taskdefinition-healthcheck-command): 
    - String
  [Interval](#cfn-ecs-taskdefinition-healthcheck-interval): Integer
  [Retries](#cfn-ecs-taskdefinition-healthcheck-retries): Integer
  [StartPeriod](#cfn-ecs-taskdefinition-healthcheck-startperiod): Integer
  [Timeout](#cfn-ecs-taskdefinition-healthcheck-timeout): Integer
```

## Properties<a name="aws-properties-ecs-taskdefinition-healthcheck-properties"></a>

`Command`  <a name="cfn-ecs-taskdefinition-healthcheck-command"></a>
A string array representing the command that the container runs to determine if it is healthy\. The string array must start with `CMD` to execute the command arguments directly, or `CMD-SHELL` to run the command with the container's default shell\. For example:  
 `[ "CMD-SHELL", "curl -f http://localhost/ || exit 1" ]`   
An exit code of 0 indicates success, and non\-zero exit code indicates failure\. For more information, see `HealthCheck` in the [Create a container](https://docs.docker.com/engine/api/v1.35/#operation/ContainerCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Interval`  <a name="cfn-ecs-taskdefinition-healthcheck-interval"></a>
The time period in seconds between each health check execution\. You may specify between 5 and 300 seconds\. The default value is 30 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Retries`  <a name="cfn-ecs-taskdefinition-healthcheck-retries"></a>
The number of times to retry a failed health check before the container is considered unhealthy\. You may specify between 1 and 10 retries\. The default value is 3\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartPeriod`  <a name="cfn-ecs-taskdefinition-healthcheck-startperiod"></a>
The optional grace period within which to provide containers time to bootstrap before failed health checks count towards the maximum number of retries\. You may specify between 0 and 300 seconds\. The `startPeriod` is disabled by default\.  
If a health check succeeds within the `startPeriod`, then the container is considered healthy and any subsequent failures count toward the maximum number of retries\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Timeout`  <a name="cfn-ecs-taskdefinition-healthcheck-timeout"></a>
The time period in seconds to wait for a health check to succeed before it is considered a failure\. You may specify between 2 and 60 seconds\. The default value is 5\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
# AWS::ECS::Service DeploymentController<a name="aws-properties-ecs-service-deploymentcontroller"></a>

The deployment controller to use for the service\. For more information, see [Amazon ECS Deployment Types](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-types.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-service-deploymentcontroller-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-deploymentcontroller-syntax.json"></a>

```
{
  "[Type](#cfn-ecs-service-deploymentcontroller-type)" : String
}
```

### YAML<a name="aws-properties-ecs-service-deploymentcontroller-syntax.yaml"></a>

```
  [Type](#cfn-ecs-service-deploymentcontroller-type): String
```

## Properties<a name="aws-properties-ecs-service-deploymentcontroller-properties"></a>

`Type`  <a name="cfn-ecs-service-deploymentcontroller-type"></a>
The deployment controller type to use\.  
There are three deployment controller types available:    
ECS  
The rolling update \(`ECS`\) deployment type involves replacing the current running version of the container with the latest version\. The number of containers Amazon ECS adds or removes from the service during a rolling update is controlled by adjusting the minimum and maximum number of healthy tasks allowed during a service deployment, as specified in the [DeploymentConfiguration](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DeploymentConfiguration.html)\.  
CODE\_DEPLOY  
The blue/green \(`CODE_DEPLOY`\) deployment type uses the blue/green deployment model powered by AWS CodeDeploy, which allows you to verify a new deployment of a service before sending production traffic to it\.  
EXTERNAL  
The external \(`EXTERNAL`\) deployment type enables you to use any third\-party deployment controller for full control over the deployment process for an Amazon ECS service\.
*Allowed Values*: `ECS` \| `EXTERNAL`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
# AWS::ECS::Service DeploymentAlarms<a name="aws-properties-ecs-service-deploymentalarms"></a>

One of the methods which provide a way for you to quickly identify when a deployment has failed, and then to optionally roll back the failure to the last working deployment\.

When the alarms are generated, Amazon ECS sets the service deployment to failed\. Set the rollback parameter to have Amazon ECS to roll back your service to the last completed deployment after a failure\.

You can only use the `DeploymentAlarms` method to detect failures when the `DeploymentController` is set to `ECS` \(rolling update\)\.

For more information, see [Rolling update](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-type-ecs.html) in the * *Amazon Elastic Container Service Developer Guide* *\.

## Syntax<a name="aws-properties-ecs-service-deploymentalarms-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-deploymentalarms-syntax.json"></a>

```
{
  "[AlarmNames](#cfn-ecs-service-deploymentalarms-alarmnames)" : [ String, ... ],
  "[Enable](#cfn-ecs-service-deploymentalarms-enable)" : Boolean,
  "[Rollback](#cfn-ecs-service-deploymentalarms-rollback)" : Boolean
}
```

### YAML<a name="aws-properties-ecs-service-deploymentalarms-syntax.yaml"></a>

```
  [AlarmNames](#cfn-ecs-service-deploymentalarms-alarmnames): 
    - String
  [Enable](#cfn-ecs-service-deploymentalarms-enable): Boolean
  [Rollback](#cfn-ecs-service-deploymentalarms-rollback): Boolean
```

## Properties<a name="aws-properties-ecs-service-deploymentalarms-properties"></a>

`AlarmNames`  <a name="cfn-ecs-service-deploymentalarms-alarmnames"></a>
One or more CloudWatch alarm names\. Use a "," to separate the alarms\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enable`  <a name="cfn-ecs-service-deploymentalarms-enable"></a>
Determines whether to use the CloudWatch alarm option in the service deployment process\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rollback`  <a name="cfn-ecs-service-deploymentalarms-rollback"></a>
Determines whether to configure Amazon ECS to roll back the service if a service deployment fails\. If rollback is used, when a service deployment fails, the service is rolled back to the last deployment that completed successfully\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
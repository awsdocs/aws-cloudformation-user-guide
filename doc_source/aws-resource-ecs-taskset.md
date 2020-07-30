# AWS::ECS::TaskSet<a name="aws-resource-ecs-taskset"></a>

Create a task set in the specified cluster and service\. This is used when a service uses the `EXTERNAL` deployment controller type\. For more information, see [Amazon ECS Deployment Types](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-types.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-resource-ecs-taskset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-taskset-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::TaskSet",
  "Properties" : {
      "[Cluster](#cfn-ecs-taskset-cluster)" : String,
      "[ExternalId](#cfn-ecs-taskset-externalid)" : String,
      "[LaunchType](#cfn-ecs-taskset-launchtype)" : String,
      "[LoadBalancers](#cfn-ecs-taskset-loadbalancers)" : [ LoadBalancer, ... ],
      "[NetworkConfiguration](#cfn-ecs-taskset-networkconfiguration)" : NetworkConfiguration,
      "[PlatformVersion](#cfn-ecs-taskset-platformversion)" : String,
      "[Scale](#cfn-ecs-taskset-scale)" : Scale,
      "[Service](#cfn-ecs-taskset-service)" : String,
      "[ServiceRegistries](#cfn-ecs-taskset-serviceregistries)" : [ ServiceRegistry, ... ],
      "[TaskDefinition](#cfn-ecs-taskset-taskdefinition)" : String
    }
}
```

### YAML<a name="aws-resource-ecs-taskset-syntax.yaml"></a>

```
Type: AWS::ECS::TaskSet
Properties: 
  [Cluster](#cfn-ecs-taskset-cluster): String
  [ExternalId](#cfn-ecs-taskset-externalid): String
  [LaunchType](#cfn-ecs-taskset-launchtype): String
  [LoadBalancers](#cfn-ecs-taskset-loadbalancers): 
    - LoadBalancer
  [NetworkConfiguration](#cfn-ecs-taskset-networkconfiguration): 
    NetworkConfiguration
  [PlatformVersion](#cfn-ecs-taskset-platformversion): String
  [Scale](#cfn-ecs-taskset-scale): 
    Scale
  [Service](#cfn-ecs-taskset-service): String
  [ServiceRegistries](#cfn-ecs-taskset-serviceregistries): 
    - ServiceRegistry
  [TaskDefinition](#cfn-ecs-taskset-taskdefinition): String
```

## Properties<a name="aws-resource-ecs-taskset-properties"></a>

`Cluster`  <a name="cfn-ecs-taskset-cluster"></a>
The short name or full Amazon Resource Name \(ARN\) of the cluster that hosts the service to create the task set in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExternalId`  <a name="cfn-ecs-taskset-externalid"></a>
An optional non\-unique tag that identifies this task set in external systems\. If the task set is associated with a service discovery registry, the tasks in this task set will have the `ECS_TASK_SET_EXTERNAL_ID` AWS Cloud Map attribute set to the provided value\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchType`  <a name="cfn-ecs-taskset-launchtype"></a>
The launch type that new tasks in the task set will use\. For more information, see [Amazon ECS Launch Types](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/launch_types.html) in the *Amazon Elastic Container Service Developer Guide*\.  
If a `launchType` is specified, the `capacityProviderStrategy` parameter must be omitted\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EC2 | FARGATE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoadBalancers`  <a name="cfn-ecs-taskset-loadbalancers"></a>
A load balancer object representing the load balancer to use with the task set\. The supported load balancer types are either an Application Load Balancer or a Network Load Balancer\.  
*Required*: No  
*Type*: List of [LoadBalancer](aws-properties-ecs-taskset-loadbalancer.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkConfiguration`  <a name="cfn-ecs-taskset-networkconfiguration"></a>
The network configuration for the task set\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-ecs-taskset-networkconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlatformVersion`  <a name="cfn-ecs-taskset-platformversion"></a>
The platform version that the tasks in the task set should use\. A platform version is specified only for tasks using the Fargate launch type\. If one isn't specified, the `LATEST` platform version is used by default\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Scale`  <a name="cfn-ecs-taskset-scale"></a>
A floating\-point percentage of the desired number of tasks to place and keep running in the task set\.  
*Required*: No  
*Type*: [Scale](aws-properties-ecs-taskset-scale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Service`  <a name="cfn-ecs-taskset-service"></a>
The short name or full Amazon Resource Name \(ARN\) of the service to create the task set in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceRegistries`  <a name="cfn-ecs-taskset-serviceregistries"></a>
The details of the service discovery registries to assign to this task set\. For more information, see [Service Discovery](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-discovery.html)\.  
*Required*: No  
*Type*: List of [ServiceRegistry](aws-properties-ecs-taskset-serviceregistry.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TaskDefinition`  <a name="cfn-ecs-taskset-taskdefinition"></a>
The task definition for the tasks in the task set to use\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ecs-taskset-return-values"></a>

### Ref<a name="aws-resource-ecs-taskset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ecs-taskset-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ecs-taskset-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the task set\.
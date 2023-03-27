# AWS::ECS::TaskSet ServiceRegistry<a name="aws-properties-ecs-taskset-serviceregistry"></a>

The details for the service registry\.

Each service may be associated with one service registry\. Multiple service registries for each service are not supported\.

When you add, update, or remove the service registries configuration, Amazon ECS starts a new deployment\. New tasks are registered and deregistered to the updated service registry configuration\.

## Syntax<a name="aws-properties-ecs-taskset-serviceregistry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskset-serviceregistry-syntax.json"></a>

```
{
  "[ContainerName](#cfn-ecs-taskset-serviceregistry-containername)" : String,
  "[ContainerPort](#cfn-ecs-taskset-serviceregistry-containerport)" : Integer,
  "[Port](#cfn-ecs-taskset-serviceregistry-port)" : Integer,
  "[RegistryArn](#cfn-ecs-taskset-serviceregistry-registryarn)" : String
}
```

### YAML<a name="aws-properties-ecs-taskset-serviceregistry-syntax.yaml"></a>

```
  [ContainerName](#cfn-ecs-taskset-serviceregistry-containername): String
  [ContainerPort](#cfn-ecs-taskset-serviceregistry-containerport): Integer
  [Port](#cfn-ecs-taskset-serviceregistry-port): Integer
  [RegistryArn](#cfn-ecs-taskset-serviceregistry-registryarn): String
```

## Properties<a name="aws-properties-ecs-taskset-serviceregistry-properties"></a>

`ContainerName`  <a name="cfn-ecs-taskset-serviceregistry-containername"></a>
The container name value to be used for your service discovery service\. It's already specified in the task definition\. If the task definition that your service task specifies uses the `bridge` or `host` network mode, you must specify a `containerName` and `containerPort` combination from the task definition\. If the task definition that your service task specifies uses the `awsvpc` network mode and a type SRV DNS record is used, you must specify either a `containerName` and `containerPort` combination or a `port` value\. However, you can't specify both\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerPort`  <a name="cfn-ecs-taskset-serviceregistry-containerport"></a>
The port value to be used for your service discovery service\. It's already specified in the task definition\. If the task definition your service task specifies uses the `bridge` or `host` network mode, you must specify a `containerName` and `containerPort` combination from the task definition\. If the task definition your service task specifies uses the `awsvpc` network mode and a type SRV DNS record is used, you must specify either a `containerName` and `containerPort` combination or a `port` value\. However, you can't specify both\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-ecs-taskset-serviceregistry-port"></a>
The port value used if your service discovery service specified an SRV record\. This field might be used if both the `awsvpc` network mode and SRV records are used\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RegistryArn`  <a name="cfn-ecs-taskset-serviceregistry-registryarn"></a>
The Amazon Resource Name \(ARN\) of the service registry\. The currently supported service registry is AWS Cloud Map\. For more information, see [CreateService](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateService.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
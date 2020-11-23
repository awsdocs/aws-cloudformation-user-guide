# AWS::ECS::Service ServiceRegistry<a name="aws-properties-ecs-service-serviceregistry"></a>

The `ServiceRegistry` property specifies details of the service registry\. For more information, see [Service Discovery](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-discovery.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-service-serviceregistry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-serviceregistry-syntax.json"></a>

```
{
  "[ContainerName](#cfn-ecs-service-serviceregistry-containername)" : String,
  "[ContainerPort](#cfn-ecs-service-serviceregistry-containerport)" : Integer,
  "[Port](#cfn-ecs-service-serviceregistry-port)" : Integer,
  "[RegistryArn](#cfn-ecs-service-serviceregistry-registryarn)" : String
}
```

### YAML<a name="aws-properties-ecs-service-serviceregistry-syntax.yaml"></a>

```
  [ContainerName](#cfn-ecs-service-serviceregistry-containername): String
  [ContainerPort](#cfn-ecs-service-serviceregistry-containerport): Integer
  [Port](#cfn-ecs-service-serviceregistry-port): Integer
  [RegistryArn](#cfn-ecs-service-serviceregistry-registryarn): String
```

## Properties<a name="aws-properties-ecs-service-serviceregistry-properties"></a>

`ContainerName`  <a name="cfn-ecs-service-serviceregistry-containername"></a>
The container name value, already specified in the task definition, to be used for your service discovery service\. If the task definition that your service task specifies uses the `bridge` or `host` network mode, you must specify a `containerName` and `containerPort` combination from the task definition\. If the task definition that your service task specifies uses the `awsvpc` network mode and a type SRV DNS record is used, you must specify either a `containerName` and `containerPort` combination or a `port` value, but not both\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerPort`  <a name="cfn-ecs-service-serviceregistry-containerport"></a>
The port value, already specified in the task definition, to be used for your service discovery service\. If the task definition your service task specifies uses the `bridge` or `host` network mode, you must specify a `containerName` and `containerPort` combination from the task definition\. If the task definition your service task specifies uses the `awsvpc` network mode and a type SRV DNS record is used, you must specify either a `containerName` and `containerPort` combination or a `port` value, but not both\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-ecs-service-serviceregistry-port"></a>
The port value used if your service discovery service specified an SRV record\. This field may be used if both the `awsvpc` network mode and SRV records are used\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RegistryArn`  <a name="cfn-ecs-service-serviceregistry-registryarn"></a>
The Amazon Resource Name \(ARN\) of the service registry\. The currently supported service registry is AWS Cloud Map\. For more information, see [CreateService](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateService.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)
# Amazon Elastic Container Service Service ServiceRegistry<a name="aws-properties-ecs-service-serviceregistry"></a>

<a name="aws-properties-ecs-service-serviceregistry-description"></a>The `ServiceRegistry` property type specifies details of the service registry\.

<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-inheritance"></a> `ServiceRegistry` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource\.

## Syntax<a name="aws-properties-ecs-service-serviceregistry-syntax"></a>

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
The container name value, already specified in the task definition, to be used for your service discovery service\. If the task definition that your service task specifies uses the bridge or host network mode, you must specify a `containerName` and `containerPort` combination from the task definition\. If the task definition that your service task specifies uses the awsvpc network mode and a type SRV DNS record is used, you must specify either a `containerName` and `containerPort` combination or a `port` value, but not both\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ContainerPort`  <a name="cfn-ecs-service-serviceregistry-containerport"></a>
The port value, already specified in the task definition, to be used for your service discovery service\. If the task definition your service task specifies uses the bridge or host network mode, you must specify a `containerName` and `containerPort` combination from the task definition\. If the task definition your service task specifies uses the awsvpc network mode and a type SRV DNS record is used, you must specify either a `containerName` and `containerPort` combination or a `port` value, but not both\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Port`  <a name="cfn-ecs-service-serviceregistry-port"></a>
The port value used if your service discovery service specified an SRV record\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RegistryArn`  <a name="cfn-ecs-service-serviceregistry-registryarn"></a>
The Amazon Resource Name \(ARN\) of the service registry\. The currently supported service registry is Amazon Route 53 auto naming\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## See Also<a name="aws-properties-ecs-service-serviceregistry-seealso"></a>
+ [ServiceRegistry](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ServiceRegistry.html) in the *Amazon Elastic Container Service API Reference*
# Amazon Elastic Container Service TaskDefinition Volumes<a name="aws-properties-ecs-taskdefinition-volumes"></a>

`Volumes` is a property of the [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md) resource that specifies a list of data volumes, which your containers can then access\.

## Syntax<a name="aws-properties-ecs-taskdefinition-volumes-syntax"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-volumes-syntax.json"></a>

```
{
  "[DockerVolumeConfiguration](#cfn-ecs-taskdefinition-volume-dockervolumeconfiguration)" : DockerVolumeConfiguration,
  "[Host](#cfn-ecs-taskdefinition-volumes-host)" : Host,
  "[Name](#cfn-ecs-taskdefinition-volumes-name)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-volumes-syntax.yaml"></a>

```
[DockerVolumeConfiguration](#cfn-ecs-taskdefinition-volume-dockervolumeconfiguration):
  DockerVolumeConfiguration
[Host](#cfn-ecs-taskdefinition-volumes-host):
  Host
[Name](#cfn-ecs-taskdefinition-volumes-name): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-volumes-properties"></a>

For more information about each property, see [Task Definition Parameters](https://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`DockerVolumeConfiguration`  <a name="cfn-ecs-taskdefinition-volume-dockervolumeconfiguration"></a>
Specifies the configuration of a Docker volume\. This parameter is specified when using Docker volumes\. Docker volumes are only supported when using the EC2 launch type\. Windows containers only support the use of the `local` driver\. To use bind mounts, specify a `host` instead\.  
*Required*: No  
*Type*: [Amazon ECS TaskDefinition DockerVolumeConfiguration](aws-properties-ecs-taskdefinition-dockervolumeconfiguration.md)

`Host`  <a name="cfn-ecs-taskdefinition-volumes-host"></a>
Determines whether your data volume persists on the host container instance and at the location where it is stored\.  
*Required*: No  
*Type*: [Amazon Elastic Container Service TaskDefinition Volumes Host](aws-properties-ecs-taskdefinition-volumes-host.md)

`Name`  <a name="cfn-ecs-taskdefinition-volumes-name"></a>
The name of the volume\. To specify mount points in your container definitions, use the value of this property\.  
*Required*: Yes  
*Type*: String
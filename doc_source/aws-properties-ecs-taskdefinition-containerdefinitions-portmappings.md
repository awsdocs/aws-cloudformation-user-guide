# Amazon Elastic Container Service TaskDefinition PortMapping<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings"></a>

`PortMappings` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that maps a container port to a host port\.

## Syntax<a name="w3ab2c21c14d894b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings-syntax.json"></a>

```
{
  "[ContainerPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-containerport)" : Integer,
  "[HostPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-hostport)" : Integer,
  "[Protocol](#cfn-ecs-taskdefinition-containerdefinition-portmappings-protocol)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings-syntax.yaml"></a>

```
[ContainerPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-containerport): Integer
[HostPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-hostport): Integer
[Protocol](#cfn-ecs-taskdefinition-containerdefinition-portmappings-protocol): String
```

## Properties<a name="w3ab2c21c14d894b7"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`ContainerPort`  <a name="cfn-ecs-taskdefinition-containerdefinition-portmappings-containerport"></a>
The port number on the container bound to the host port\.  
*Required*: Yes  
*Type*: Integer

`HostPort`  <a name="cfn-ecs-taskdefinition-containerdefinition-portmappings-hostport"></a>
The host port number on the container instance that you want to reserve for your container\. You can specify a non\-reserved host port for your container port mapping, omit the host port, or set the host port to `0`\. If you specify a container port but no host port, your container host port is assigned automatically \.  
Don't specify a host port in the `49153` to `65535` port range; these ports are reserved for automatic assignment\. Other reserved ports include `22` for SSH, `2375` and `2376` for Docker, and `51678` for the Amazon Elastic Container Service container agent\. Don't specify a host port that is being used for a task—that port is reserved while the task is running\.  
*Required*: No  
*Type*: Integer

`Protocol`  <a name="cfn-ecs-taskdefinition-containerdefinition-portmappings-protocol"></a>
The protocol used for the port mapping\. For valid values, see the [http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) parameter in the *Amazon Elastic Container Service Developer Guide*\. By default, AWS CloudFormation specifies `tcp`\.  
*Required*: No  
*Type*: String
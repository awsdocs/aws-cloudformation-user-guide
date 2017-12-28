# Amazon Elastic Container Service TaskDefinition LinuxParameters<a name="aws-properties-ecs-taskdefinition-linuxparameters"></a>

<a name="aws-properties-ecs-taskdefinition-linuxparameters-description"></a>The `LinuxParameters` property type specifies Linux\-specific options to apply to an Amazon Elastic Container Service \(Amazon ECS\) container\.

<a name="aws-properties-ecs-taskdefinition-linuxparameters-inheritance"></a> `LinuxParameters` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property type\.

## Syntax<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-linuxparameters-capabilities)" : KernelCapabilities,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-linuxparameters-devices)" : [ Device, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-linuxparameters-initprocessenabled)" : Boolean
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-linuxparameters-capabilities): 
  KernelCapabilities
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-linuxparameters-devices): 
  - Device
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-linuxparameters-initprocessenabled): Boolean
```

## Properties<a name="aws-properties-ecs-taskdefinition-linuxparameters-properties"></a>

`Capabilities`  
The Linux capabilities for the container that are added to or dropped from the default configuration provided by Docker\.  
 *Required*: No  
 *Type*: [Amazon ECS TaskDefinition KernelCapabilities](aws-properties-ecs-taskdefinition-kernelcapabilities.md)  
 *Update requires*: Replacement 

`Devices`  
Any host devices to expose to the container\. This maps to `Devices` in the [ Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.27/#create-a-container) section of the *Docker Remote API* and the `--device` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
 *Required*: No  
 *Type*: List of [Amazon ECS TaskDefinition Device](aws-properties-ecs-taskdefinition-device.md) property types  
 *Update requires*: Replacement 

`InitProcessEnabled`  
Indicates whether to run an `init` process inside the container that forwards signals and reaps processes\. This maps to the `--init` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
This property requires at least version 1\.25 of the *Docker Remote API* on your container instance\. To check the API version on your container instance, log in to your container instance and run the following command: `sudo docker version | grep "Server API version"`  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: Replacement 

## See Also<a name="aws-properties-ecs-taskdefinition-linuxparameters-seealso"></a>

+ [LinuxParameters](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_LinuxParameters.html) in the *Amazon Elastic Container Service API Reference*